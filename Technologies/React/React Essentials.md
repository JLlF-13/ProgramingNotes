A collection of core concepts and tools that every React developer should understand. These notes are designed to be practical, clear, and ready to share — whether you're revisiting them yourself or handing them off to someone learning React.

## Hooks

Hooks are functions that let you “hook into” React features from functional components.

- `useState`: Manages local state.
- `useEffect`: Runs side effects (e.g., data fetching, event listeners).
- `useContext`: Shares state across components without prop drilling.
- `useReducer`: Handles complex state logic.
- `useRef`: Accesses DOM elements or stores mutable values.
[[Hooks]]

## Project Structure

Organize your React app for scalability and clarity.

- `src/components/`: Reusable UI blocks
- `src/pages/`: Route-based views
- `src/hooks/`: Custom hooks
- `src/services/`: API calls or business logic
- `src/assets/`: Images, fonts, etc.
[[Project Structure]]

## Routing

Use **React Router** to navigate between pages.

- Define routes with `<Route />` and `<BrowserRouter />`
- Use `useNavigate()` to programmatically change pages
- Support nested routes and layouts
[[Routing]]

## Styling

Choose your preferred styling method:

- **Tailwind CSS**: Utility-first classes
- **Styled Components**: CSS-in-JS
- **CSS Modules**: Scoped styles per component
[[Styling]]

## State Management

Beyond local state, manage global or shared state:

- **Context API**: Built-in, simple
- **Redux**: Powerful but verbose
- **Zustand**: Lightweight and intuitive
[[State Management]]

## Data Fetching

Get and manage external data:

- **Axios** or `fetch()` for HTTP requests
- **React Query** for caching, loading states, and retries
[[Data Fetching]]

## Testing

Ensure your app works as expected:

- **Jest**: Test runner
- **React Testing Library**: Test components from the user’s perspective
[[Testing]]

## Dev Tools

Improve your workflow:

- **ESLint**: Linting
- **Prettier**: Code formatting
- **React DevTools**: Inspect component trees
- **Vite / CRA**: Project bootstrapping
[[Dev tools]]

## Usefull NPM packages

This is the command to install a package:

```bash
npm install package-name
```

Enhance your React workflow with these essential tools: [[Usefull NPM packages]]
