React Router helps your app switch between pages without reloading.

Installation:

```bash
npm install react-router-dom
```

---

### Define routes with `<Route />` and `<BrowserRouter />`

**Purpose:** Set up which component shows for each URL. 
**Example:**
```jsx
<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
  </Routes>
</BrowserRouter>
```


---

### Use `useNavigate()` to programmatically change pages

**Purpose:** Navigate between pages using code (not just links). 
**Example:**
```jsx
const navigate = useNavigate();
navigate("/profile"); // Takes user to /profile
```


---

### Support nested routes and layouts

**Purpose:** Show child components inside a parent layout. 
**Example:**
```jsx
<Route path="/dashboard" element={<DashboardLayout />}>
  <Route path="stats" element={<Stats />} />
  <Route path="settings" element={<Settings />} />
</Route>
```
This means `/dashboard/stats` and `/dashboard/settings` will be shown inside the `DashboardLayout`.


---

## Linking Between Pages in React Router

To create clickable links that navigate between routes, use the `<Link />` component from React Router.
**Example**:
```jsx
import { Link } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
    </nav>
  );
}
```
This creates navigation links that change the URL and render the correct component—without reloading the page.

### Why Use `<Link />` Instead of `<a>`?

- `<Link />` uses React Router’s internal navigation system
    
- Prevents full page reloads
    
- Keeps your app fast and smooth

### Bonus: Active Links

You can use `<NavLink />` to style the active link:

```jsx
import { NavLink } from 'react-router-dom';

<NavLink to="/about" className={({ isActive }) => isActive ? "active" : ""}>
  About
</NavLink>
```