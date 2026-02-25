
### `useState` – Manage Local State

**Purpose:** Allows you to store and update values within a component.

**Example:**

```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increase</button>
    </div>
  );
}
```

Example with a modal:

```jsx
import { useState } from 'react';

function ModalExample() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsOpen(true)}>Open Modal</button>

      {isOpen && (
        <div className="modal">
          <p>This is a modal!</p>
          <button onClick={() => setIsOpen(false)}>Close</button>
        </div>
      )}
    </div>
  );
}
```

Example with form:

```jsx
import { useState } from 'react';

function ContactForm() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [message, setMessage] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault();
    console.log('Form submitted:', { name, email, message });
    // Logic to send data to server
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Nom:
        <input
          type="text"
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
      </label>

      <label>
        Correu electrònic:
        <input
          type="email"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
        />
      </label>

      <label>
        Missatge:
        <textarea
          value={message}
          onChange={(e) => setMessage(e.target.value)}
        />
      </label>

      <button type="submit">Enviar</button>
    </form>
  );
}
```

---
### `useEffect` – Handle Side Effects

**Purpose:** Runs code after render (e.g., fetching data, setting up listeners).

 What does `[]` mean?
- The empty array `[]` tells React: “Run this effect **only once**, after the first render.”
    
- If you include variables inside the array (e.g. `[id]`), the effect will re-run **whenever those variables change**.

#### `[]` means: run once

When the app opens, you fetch **Pikachu** just once—like starting the game with your first Pokémon already by your side.

**Simple Example:**

```javascript
import { useEffect } from 'react';

function Logger() {
  useEffect(() => {
    console.log('Component mounted');
    return () => console.log('Component unmounted');
  }, []);
  return <p>Check the console</p>;
}
```

Example with API Call:

```javascript
import { useState, useEffect } from 'react';

function PokemonFetcher() {
  const [pokemon, setPokemon] = useState(null);

  useEffect(() => {
    fetch('https://pokeapi.co/api/v2/pokemon/ditto')
      .then(response => response.json())
      .then(data => setPokemon(data));
  }, []);

  return (
    <div>
      {pokemon ? (
        <p>{pokemon.name} has {pokemon.abilities.length} abilities.</p>
      ) : (
        <p>Loading...</p>
      )}
    </div>
  );
}
```

#### `[pokemon]` means: run when Pokémon changes

Every time the user picks a new main Pokémon (like Charmander or Squirtle), you fetch that one—like switching targets and tossing a new Pokéball.

Example with Changing Dependency:

```javascript
import { useState, useEffect } from 'react';

function CounterLogger() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log(`Count changed to: ${count}`);
  }, [count]); 

  return (
    <div>
      <p>Current count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

Example with Changing Dependency and API:

```javascript
import { useState, useEffect } from 'react';

function DynamicPokemon() {
  const [id, setId] = useState(1); 
  const [pokemon, setPokemon] = useState(null);

  useEffect(() => {
    setPokemon(null); 
    fetch(`https://pokeapi.co/api/v2/pokemon/${id}`)
      .then(res => res.json())
      .then(data => setPokemon(data));
  }, [id]); 

  const handleChange = (e) => {
    setId(e.target.value); 
  };

  return (
    <div>
      <form>
        <label>Enter Pokémon ID:</label>
        <input type="number" value={id} onChange={handleChange} />
      </form>

      {pokemon ? (
        <h2>{pokemon.name}</h2>
      ) : (
        <p>Loading...</p>
      )}
    </div>
  );
}
```


---
###  `useContext` – Share State Across Components

**Purpose:** Access shared values without passing props manually.

**Example:**

```javascript
import { useContext, createContext } from 'react';

const ThemeContext = createContext('light');

function ThemeDisplay() {
  const theme = useContext(ThemeContext);
  return <p>Current theme: {theme}</p>;
}
```

---
### `useReducer` – Manage Complex State Logic

**Purpose:** Useful for state that depends on actions or has multiple transitions.

**Example:**

```javascript
import { useReducer } from 'react';

function reducer(state, action) {
  switch (action.type) {
    case 'increment': return { count: state.count + 1 };
    case 'decrement': return { count: state.count - 1 };
    default: return state;
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });
  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={() => dispatch({ type: 'increment' })}>+</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>-</button>
    </div>
  );
}
```

---
### `useRef` – Access DOM or Store Mutable Values

**Purpose:** Keeps a reference to a DOM element or a value that doesn’t trigger re-renders.

**Example:**

```javascript
import { useRef, useEffect } from 'react';

function AutoFocusInput() {
  const inputRef = useRef(null);

  useEffect(() => {
    inputRef.current.focus();
  }, []);

  return <input ref={inputRef} placeholder="Type here" />;
}
```