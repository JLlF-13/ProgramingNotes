Organize your React app for clarity and scalability. Here's what each folder is for (not all forders are initially created):
### `src/components/` – Reusable UI blocks

**Purpose:** Contains small, reusable pieces of UI. 
**Example:** A `<Button />`, `<Navbar />` or `<Footer />` component used across multiple pages.

### `src/pages/` – Route-based views

**Purpose:** Store logic that can be reused across components. 
**Example:** `useFetch()` to handle API data fetching.

### `src/hooks/` – Custom hooks

**Purpose:** Store logic that can be reused across components. 
**Example:** `useFetch()` to handle API data fetching.

### `src/services/` – API calls or business logic

**Purpose:** Centralize external requests and core logic. 
**Example:** `userService.js` with functions like `loginUser()` or `getUserData()`.

### `src/assets/` – Images, fonts, etc.

**Purpose:** Store static files used in the UI. 
**Example:** `logo.png`, `Roboto.ttf`, or `background.jpg`.