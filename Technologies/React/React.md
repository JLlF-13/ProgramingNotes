
React is a JavaScript library for building user interfaces. It’s **component-based**, **declarative**, and designed for building fast, interactive web applications. It’s primarily used for **frontend development**, allowing developers to create reusable UI components and manage complex application states efficiently.

### Installation

To run React on your computer, you need to install Node.js and a package manager like npm or yarn.

Link to install --> [Here](https://nodejs.org)

---
### How it works

React works by creating a **virtual DOM**, which is a lightweight copy of the real DOM. When the state of a component changes, React updates only the parts of the DOM that need to change, making it highly efficient.

The **DOM (Document Object Model)** is a tree-like structure that represents the content of a webpage. It lets JavaScript access and change elements like text, images, and styles dynamically.

React uses a **virtual DOM** to compare changes efficiently and update only what’s needed, making your app faster.

### Key Concepts:

- **Components**: Reusable building blocks of UI
    
- **JSX**: Syntax extension that lets you write HTML inside JavaScript
    
- **Props**: Data passed from parent to child components
    
- **State**: Internal data that changes over time
    
- **Lifecycle**: Hooks like `useEffect` let you run code at specific points


---
### Create a project

To create a project in React you have 2 options

Optiona A, Create a React App:

```bash
npx create-react-app project-name
cd project-name
npm start
```
This sets up a full React environment with sensible defaults. The app will run at `http://localhost:3000`.

Option B, Vite (Recomended):

```bash
npm create vite@latest project-name --template react
cd project-name
npm install
npm run dev
```
> The `--template react` is not mandatory

Vite is faster and more lightweight. The app usually runs at `http://localhost:5173`.

Once the project is created and opened in your **IDE**, you'll see a basic folder structure like this:
```
src/
├── App.jsx          # Main component of your app
├── main.jsx         # Entry point that renders <App />
├── assets/          # Folder for images, fonts, etc.
├── components/      # Reusable UI components
```

---
### [[React Essentials]]

This section will dive deeper into hooks, project structure, libraries, and best practices to build scalable React apps.

---

## Vite vs Create React App (CRA)

|Feature|Create React App (CRA)|Vite|
|---|---|---|
|Setup|Uses `react-scripts`|Uses `vite`|
|Development Speed|Slower startup (Webpack-based)|Instant startup (ESBuild-based)|
|Hot Module Replacement|Acceptable|Extremely fast|
|Build Tool|Webpack|ESBuild (dev) + Rollup (build)|
|Configuration|Hidden by default|Exposed and customizable|
|TypeScript Support|Optional|Built-in|
|Plugin Ecosystem|Limited|Modern and extensible|
|Electron Compatibility|Requires adjustments|Works seamlessly|
|Eject Option|Required for manual config|Not needed; config is accessible|

**CRA** uses `react-scripts` and runs on port `3000`. **Vite** uses `vite` and runs on port `5173`.

For Electron apps, Vite is faster, simpler, and better suited for local backends like SQLite.