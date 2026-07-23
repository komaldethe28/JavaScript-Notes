## Hooks:
> "React Hooks were introduced to bring state and lifecycle features to functional components, making them more powerful and reducing the need for class components."

**useState**
> "The `useState` Hook is used to add state management to functional components. It allows components to store and update data that changes over time.
>
> `useState` returns an array containing the current state value and a setter function used to update that state.
>
> Whenever the state changes, React triggers a re-render and updates the UI accordingly.
>
> Common use cases include:
> * Form inputs
> * Counters
> * Toggle buttons
> * Managing API data
> * UI state management
>
> In my projects, I frequently use `useState` for managing form values, loading states, and user interactions."

### Example:

```jsx id="x5y1om"
const [count, setCount] = useState(0);
```

### One-Liner:
> "useState allows functional components to manage mutable state and automatically re-render the UI when the state changes."

---

**useEffect**
> "The `useEffect` Hook is used to perform side effects in functional components.
>
> Side effects include:
>
> * API calls
> * Event listeners
> * Timers
> * DOM manipulation
> * Subscriptions
>
> `useEffect` executes after the component has rendered.
>
> The behavior of `useEffect` depends on its dependency array:
>
> * No dependency array → Runs after every render.
> * Empty array `[]` → Runs only once after the initial render.
> * Dependencies `[value]` → Runs when the specified value changes.
>
> Additionally, `useEffect` supports cleanup functions, which are essential for preventing memory leaks."

### Example:

```jsx id="yuv42c"
useEffect(() => {
    fetchUsers();

    return () => {
        console.log("Cleanup");
    };
}, []);
```

### One-Liner:
> "useEffect is used to handle side effects and lifecycle-related logic in functional components."

---

**useContext**
> "The `useContext` Hook provides a way to access shared data across components without prop drilling.
>
> It works with the Context API and allows components to consume context values directly.
>
> Common use cases include:
>
> * Authentication
> * Theme management
> * Language preferences
> * User settings
>
> `useContext` improves code maintainability by eliminating the need to pass props through multiple component levels.
>
> In my projects, I have used `useContext` for managing themes and sharing authenticated user information across components."

### Example:

```jsx id="cobx1g"
const user = useContext(UserContext);
```

### One-Liner:
> "useContext provides direct access to shared state and helps eliminate prop drilling."

---

**useRef**
> "The `useRef` Hook is used to persist values across renders without causing a component to re-render.
>
> It is commonly used for:
>
> * Accessing DOM elements
> * Storing mutable values
> * Managing focus
> * Tracking previous values
> * Working with timers
>
> Unlike `useState`, updating a `useRef` value does not trigger a re-render.
>
> In React applications, `useRef` is frequently used to focus input fields and maintain references to DOM elements."

### Example:

```jsx id="ct8k4r"
const inputRef = useRef(null);

inputRef.current.focus();
```

### One-Liner:
> "useRef stores mutable values and DOM references without triggering component re-renders."

---

### High-Impact Comparison Table

| Hook         | Purpose                                 |
| ------------ | --------------------------------------- |
| `useState`   | Manage component state                  |
| `useEffect`  | Handle side effects                     |
| `useContext` | Share state globally                    |
| `useRef`     | Store mutable values and DOM references |

---

### Interviewer Question
> "What is the difference between `useState` and `useRef`?"

**Answer:**
> "`useState` triggers a component re-render whenever the state changes, whereas `useRef` stores mutable values without causing a re-render. Therefore, `useState` is used for UI-related data, while `useRef` is used for persisting values and interacting with DOM elements."

---

**useMemo**
> "The `useMemo` Hook is used to memoize the result of an expensive computation and recompute it only when its dependencies change.
>
> It helps improve performance by preventing unnecessary calculations during component re-renders.
>
> `useMemo` returns a memoized value and is commonly used when dealing with:
>
> * Expensive computations
> * Large datasets
> * Filtering and sorting operations
> * Derived state
>
> However, `useMemo` should be used only when there is a measurable performance benefit, as it also has a small memory overhead.
>
> In my projects, I have used `useMemo` to optimize filtering operations and prevent unnecessary recalculations in dashboards."

### Example:

```jsx id="7gdz8s"
const filteredUsers = useMemo(() => {
    return users.filter(user => user.active);
}, [users]);
```

### One-Liner:
> "useMemo memoizes computed values to improve performance by avoiding unnecessary recalculations."

---

**useCallback**
> "The `useCallback` Hook is used to memoize functions and prevent them from being recreated on every render.
>
> This is particularly useful when passing callback functions to child components that are wrapped with `React.memo()`.
>
> Without `useCallback`, a new function instance is created on every render, which can cause unnecessary child component re-renders.
>
> Common use cases include:
> * Event handlers
> * Passing callbacks to child components
> * Performance optimization

### Example:

```jsx id="2lm6ce"
const handleClick = useCallback(() => {
    console.log("Clicked");
}, []);
```

### One-Liner:
> "useCallback memoizes functions to prevent unnecessary re-creations during re-renders."

---

### useMemo vs useCallback

| useMemo                | useCallback         |
| ---------------------- | ------------------- |
| Memoizes Values        | Memoizes Functions  |
| Returns Result         | Returns Function    |
| Optimizes Computations | Optimizes Callbacks |

### High-Impact Statement:
> "Internally, `useCallback(fn, deps)` is equivalent to `useMemo(() => fn, deps)`."

---

**useReducer**
> "The `useReducer` Hook is an alternative to `useState` for managing complex state logic in React components.
>
> It follows the reducer pattern, where state transitions are handled through actions and a reducer function.
>
> `useReducer` is particularly useful when:
>
> * State has multiple sub-values.
> * State transitions are complex.
> * Multiple actions need to update state.
>
> It returns the current state and a `dispatch` function used to trigger state updates.
>
> The reducer function receives the current state and an action, then returns the updated state.
>
> In large applications, `useReducer` provides a predictable and scalable approach to state management and is conceptually similar to Redux."

### Example:

```jsx id="67v6mb"
const [state, dispatch] = useReducer(reducer, initialState);
```

### One-Liner:
> "useReducer manages complex state transitions using actions and a reducer function."

---

### useState vs useReducer

| useState         | useReducer                  |
| ---------------- | --------------------------- |
| Simple State     | Complex State               |
| Easy to Use      | Better for Multiple Updates |
| Direct Setter    | Uses Dispatch               |
| Small Components | Large Components            |

---

### Interviewer Question
> "When would you use `useReducer` over `useState`?"

**Answer:**
> "I would use `useState` for simple state management, such as toggles and form inputs. However, when state becomes complex, involves multiple related values, or requires predictable state transitions, I prefer `useReducer` because it centralizes state logic and improves maintainability."

---

### Golden Interview Statement
> "For performance optimization in React, I use `useMemo` to memoize expensive computations, `useCallback` to memoize functions, and `useReducer` to manage complex state logic."

This single sentence connects:
* Performance Optimization
* Hooks
* State Management
* React Best Practices

**useLayoutEffect**
> "The `useLayoutEffect` Hook is similar to `useEffect`, but it executes synchronously after the DOM has been updated and before the browser paints the screen.
>
> This makes it useful for performing DOM measurements and synchronously applying changes to avoid visual inconsistencies or flickering.
>
> Common use cases include:
>
> * Measuring element dimensions
> * Adjusting scroll positions
> * Performing animations
> * Updating the DOM before the user sees it
>
> Since `useLayoutEffect` blocks the browser from painting, it should be used sparingly. For most side effects, `useEffect` is the preferred choice."

### Example:

```jsx id="2kq9xp"
useLayoutEffect(() => {
    console.log(divRef.current.getBoundingClientRect());
}, []);
```

### One-Liner:
> "useLayoutEffect runs synchronously after DOM updates but before the browser paints the screen."

---

### `useEffect` vs `useLayoutEffect`
| useEffect                       | useLayoutEffect                              |
| ------------------------------- | -------------------------------------------- |
| Runs asynchronously             | Runs synchronously                           |
| After browser paint             | Before browser paint                         |
| Preferred for most side effects | Used for DOM measurements and visual updates |

---

**useImperativeHandle**
> "The `useImperativeHandle` Hook allows a child component to expose specific methods or values to its parent component when used with `forwardRef`.
>
> Normally, React promotes a declarative programming model. However, `useImperativeHandle` provides a controlled way to expose imperative functionality.
>
> Common use cases include:
>
> * Exposing focus methods
> * Triggering child component actions
> * Controlling modals
> * Managing custom input components
>
> It is often used in reusable component libraries where parent components need limited access to child behavior."

### Example:

```jsx id="cqtz5q"
useImperativeHandle(ref, () => ({
    focus: () => {
        inputRef.current.focus();
    }
}));
```

### One-Liner:
> "useImperativeHandle customizes the instance value exposed to parent components through refs."

---

**useDebugValue**
> "The `useDebugValue` Hook is primarily used for debugging custom hooks in React Developer Tools.
>
> It allows developers to display custom labels or values for hooks, making debugging easier during development.
>
> `useDebugValue` has no effect in production builds and is intended solely to improve the developer experience.
>
> It is commonly used when creating reusable custom hooks that may be shared across an application or library."

### Example:

```jsx id="abc"
useDebugValue(isOnline ? "Online" : "Offline");
```

### One-Liner:
> "useDebugValue adds custom labels to custom hooks in React Developer Tools for easier debugging."

---

### High-Impact Interview Statement
> "These Hooks are less commonly used in day-to-day development but demonstrate React's flexibility:
>
> * `useLayoutEffect` handles DOM-related side effects before painting.
> * `useImperativeHandle` exposes controlled imperative APIs to parent components.
> * `useDebugValue` improves the debugging experience for custom hooks."

---

### Pro-Fresher Tip
> "Have you used `useImperativeHandle` or `useDebugValue` in production?"

A good answer is:
> "I haven't used them extensively in production projects yet, but I understand their purpose and have implemented them in practice projects. `useImperativeHandle` is useful for reusable component libraries, while `useDebugValue` helps improve the developer experience when building custom hooks."

---

**Custom Hooks**
> "Custom Hooks are JavaScript functions that allow us to extract and reuse stateful logic across multiple React components.
>
> They always follow React's Hook naming convention, which means their names must start with `use`, such as `useFetch`, `useAuth`, or `useLocalStorage`.
>
> Custom Hooks do not introduce new React features; instead, they provide a way to share logic between components while keeping the code clean, reusable, and maintainable.
>
> Common use cases include:
> * API fetching
> * Authentication
> * Form handling
> * Local Storage management
> * Theme management
> * Window resize detection
>
> By using Custom Hooks, we can avoid code duplication and improve the separation of concerns in React applications.
>
> In my projects, I have created Custom Hooks for API calls and managing local storage values, which helped make components more reusable and easier to maintain."

---

### Example

```jsx id="2q8cz1"
import { useState, useEffect } from "react";

function useFetch(url) {
    const [data, setData] = useState(null);

    useEffect(() => {
        fetch(url)
            .then((res) => res.json())
            .then((data) => setData(data));
    }, [url]);

    return data;
}
```

Usage:

```jsx id="ezc5tu"
const users = useFetch(
    "https://jsonplaceholder.typicode.com/users"
);
```

---

### Benefits of Custom Hooks
* Reusability
* Cleaner Components
* Better Separation of Concerns
* Easier Testing
* Improved Maintainability

---

### One-Liner
> "Custom Hooks are reusable functions that encapsulate and share stateful logic across React components."

---

### Do Custom Hooks share state between components?**
**Answer:**
> "No, Custom Hooks do not share state. Each component that calls a Custom Hook gets its own independent instance of state and effects. Custom Hooks only share the logic, not the data itself."

---

### Q: Why do Custom Hooks start with `use`?**
**Answer:**
> "React uses the `use` prefix to identify Hooks and enforce the Rules of Hooks, ensuring that Hooks are called only at the top level of React function components or other Custom Hooks."

---

### High-Impact Interview Statement
> "Custom Hooks are one of the most powerful features of React because they allow us to abstract complex logic into reusable units. They improve code organization, reduce duplication, and make applications more scalable."

---

### Interviewer Question:
> "Have you used Custom Hooks?"

> "Yes, I have created Custom Hooks like `useFetch`, `useLocalStorage`, and `useDebounce` in my practice projects. They helped me centralize reusable logic and keep my components focused on rendering UI rather than managing implementation details."
