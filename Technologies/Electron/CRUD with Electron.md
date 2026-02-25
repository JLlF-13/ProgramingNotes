Here is a simple exaple project with react and electron

> This is the intended way to build a desktop app with a local backend. Alternatively, you could use an **external backend** (e.g., Express, PHP, etc.) and avoid managing local database logic inside Electron.

---
### Project Structure:

```
my-electron-react-app/
├── electron/
│   ├── main.cjs          # Main process (Electron backend)
│   ├── preload.js       # Secure API exposed to the frontend
│   ├── db.cjs            # SQLite database logic
├── src/
│   ├── App.jsx          # React user interface
│   ├── index.js         # React entry point
├── public/
│   └── index.html
├── package.json
```

---

### Create the project

Creating the project is straightforward. First, set up React, then install Electron and SQLite:

```bash
npx create-react-app my-electron-react-app
cd my-electron-react-app
npm install --save-dev electron
npm install sqlite3
```

> **This is an example using** `sqlite3`, which is easier to set up because it doesn't require native compilation. If you prefer better performance and synchronous queries, you can also use `better-sqlite3`, but it requires a proper build environment (e.g., Visual Studio Build Tools on Windows).

> `.cjs` **extensions are used** for backend files that rely on CommonJS syntax (`require`, `module.exports`). This ensures compatibility with Electron's main process, which typically runs in a Node.js environment that defaults to CommonJS.


---

### `db.cjs` – Database Logic

This file handles the creation of the `users` table and defines basic CRUD operations.

```javascript
const Database = require('sqlite3');
const path = require('path');

const db = new Database(path.join(__dirname, 'data.db'));
db.pragma('journal_mode = WAL');

db.run(`CREATE TABLE IF NOT EXISTS users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  username TEXT NOT NULL UNIQUE,
  password TEXT NOT NULL,
  email TEXT
)`);


function getUsers() {
  return new Promise((resolve, reject) => {
    db.all('SELECT id, username, email FROM users', (err, rows) => {
      if (err) reject(err);
      else resolve(rows);
    });
  });
}

function getUser(id) {
  return new Promise((resolve, reject) => {
    db.get('SELECT id, username, email FROM users WHERE id = ?', [id], (err, row) => {
      if (err) reject(err);
      else resolve(row);
    });
  });
}

function createUser({ username, password, email }) {
  return new Promise((resolve, reject) => {
    db.run('INSERT INTO users (username, password, email) VALUES (?, ?, ?)',
      [username, password, email],
      function (err) {
        if (err) reject(err);
        else resolve({ id: this.lastID });
      });
  });
}

function updateUser(id, { username, email }) {
  return new Promise((resolve, reject) => {
    db.run('UPDATE users SET username = ?, email = ? WHERE id = ?',
      [username, email, id],
      function (err) {
        if (err) reject(err);
        else resolve({ changes: this.changes });
      });
  });
}

function deleteUser(id) {
  return new Promise((resolve, reject) => {
    db.run('DELETE FROM users WHERE id = ?', [id], function (err) {
      if (err) reject(err);
      else resolve({ changes: this.changes });
    });
  });
}

module.exports = { getUsers, insertUser, updateUser, deleteUser };
```

### `main.cjs` – Electron Backend

This is the main file for Electron. It creates the application window and handles IPC communication between the frontend and backend.

```js
const { app, BrowserWindow, ipcMain } = require('electron');
const path = require('path');
const db = require('./db.cjs');

function createWindow() {
  const win = new BrowserWindow({
    width: 800,
    height: 600,
    webPreferences: {
      preload: path.join(__dirname, 'preload.js'),
      contextIsolation: true
    }
  });

  win.loadURL('http://localhost:5173');
}

app.whenReady().then(createWindow);

ipcMain.handle('get-users', async () => await db.getUsers());
ipcMain.handle('get-user', async (event, id) => await db.getUser(id));
ipcMain.handle('create-user', async (event, data) => await db.createUser(data));
ipcMain.handle('update-user', async (event, { id, data }) => await db.updateUser(id, data));
ipcMain.handle('delete-user', async (event, id) => await db.deleteUser(id));
```

### `preload.js` – Exposing the API

This file safely exposes backend functions to the React frontend using `contextBridge`.

```js
const { contextBridge, ipcRenderer } = require('electron');

contextBridge.exposeInMainWorld('api', {
  getUsers: () => ipcRenderer.invoke('get-users'),
  getUser: (id) => ipcRenderer.invoke('get-user', id),
  createUser: (data) => ipcRenderer.invoke('create-user', data),
  updateUser: (id, data) => ipcRenderer.invoke('update-user', { id, data }),
  deleteUser: (id) => ipcRenderer.invoke('delete-user', id)
});

```

### `App.jsx` – React User Interface

This component displays the list of users and allows adding, editing, and deleting them. You can later split this into smaller components for better structure.

```js
import React, { useEffect, useState } from 'react';

function App() {
  const [users, setUsers] = useState([]);
  const [form, setForm] = useState({ username: '', email: '', password: '' });
  const [editingId, setEditingId] = useState(null);

  useEffect(() => {
    loadUsers();
  }, []);

  const loadUsers = async () => {
    const data = await window.api.getUsers();
    setUsers(data);
  };

  const handleAddOrEdit = async () => {
    if (editingId) {
      await window.api.updateUser(editingId, {
        username: form.username,
        email: form.email
      });
      setEditingId(null);
    } else {
      await window.api.createUser(form);
    }
    setForm({ username: '', email: '', password: '' });
    loadUsers();
  };

  const handleEdit = (user) => {
    setForm({ username: user.username, email: user.email, password: '' });
    setEditingId(user.id);
  };

  const handleDelete = async (id) => {
    await window.api.deleteUser(id);
    loadUsers();
  };

  return (
    <div>
      <h1>User Manager</h1>
      <input
        placeholder="Username"
        value={form.username}
        onChange={e => setForm({ ...form, username: e.target.value })}
      />
      <input
        placeholder="Email"
        value={form.email}
        onChange={e => setForm({ ...form, email: e.target.value })}
      />
      <input
        placeholder="Password"
        type="password"
        value={form.password}
        onChange={e => setForm({ ...form, password: e.target.value })}
      />
      <button onClick={handleAddOrEdit}>
        {editingId ? 'Update' : 'Add'} User
      </button>
      <ul>
        {users.map(user => (
          <li key={user.id}>
            {user.username} ({user.email})
            <button onClick={() => handleEdit(user)}>Edit</button>
            <button onClick={() => handleDelete(user.id)}>Delete</button>
          </li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

## `package.json` Configuration

Update your `package.json` to define the Electron entry point and add scripts to run both React and Electron together.

```json
{
  "name": "my-electron-react-app",
  "version": "1.0.0",
  "main": "electron/main.cjs",
  "scripts": {
    "dev": "concurrently \"npm run vite\" \"npm run electron\"",
    "vite": "vite",
    "electron": "electron .",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "react": "^19.1.1",
    "react-dom": "^19.1.1",
    "sqlite3": "^5.1.7"
  },
  "devDependencies": {
    "electron": "^30.0.0",
    "concurrently": "^8.0.0",
    "vite": "^7.1.2",
    "@vitejs/plugin-react": "^5.0.0"
  }
}
```
### Running the Project

Once everything is set up, you can start both the React frontend and the Electron backend together using the following command:

```bash
npm run dev
```

This command does two things at once:

- Starts the **React development server** (`npm run vite)
    
- Launches **Electron** and opens the desktop window (`npm run electron`)
    

> Make sure the React app is running on `http://localhost:5173`, as defined in `main.js`.

If you only want to run Electron (without React), you can use:

```bash
npm run electron
```

And if you only want to run React in the browser:

```bash
npm start
```