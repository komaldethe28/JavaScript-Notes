## React

**JSX**
> "JSX stands for JavaScript XML. It is a syntax extension for JavaScript that allows developers to write HTML-like code inside JavaScript.
>
> JSX makes React components more readable and easier to maintain by combining UI structure and logic in a single place.
>
> Although JSX looks like HTML, it is not understood directly by browsers. During the build process, tools like Babel transpile JSX into `React.createElement()` calls, which ultimately create JavaScript objects representing the Virtual DOM.
>
> JSX supports:
> * JavaScript expressions using `{}`
> * Conditional rendering
> * Rendering lists
> * Passing props

> In my React projects, I use JSX extensively to build reusable and dynamic user interfaces."

### Example:
```jsx id="2pxvkt"
const element = <h1>Hello, World!</h1>;
```

Internally, Babel converts it to:

```javascript id="74jrf0"
React.createElement("h1", null, "Hello, World!");
```

### One-Liner:
> "JSX is a syntax extension that allows us to write HTML-like code in JavaScript, which is transpiled into `React.createElement()` calls."

---

**Components**
> "Components are the fundamental building blocks of React applications. A component is an independent and reusable piece of UI that encapsulates its own structure, logic, and behavior.
>
> React follows a component-based architecture, which improves code reusability, maintainability, and scalability.
>
> There are two types of components:
> 1. Functional Components
> 2. Class Components
>
> Today, Functional Components are preferred because they support React Hooks and provide a simpler and more modern development experience.
>
> Components can communicate with each other using Props and manage their own data using State.
>
> In my projects, I use components to create reusable elements such as buttons, forms, cards, navigation bars, and dashboards."

### Example:

```jsx id="u6j2ir"
function Welcome() {
    return <h1>Welcome to React!</h1>;
}
```

### Benefits of Components:
* Reusability
* Maintainability
* Scalability
* Separation of Concerns
* Easier Testing

### One-Liner:
> "Components are reusable, independent units of UI that form the foundation of React applications."

---

**Props**
> "Props are used to pass data from a parent component to a child component in React.
>
> Props are immutable, which means a child component cannot modify the props it receives. They help establish a unidirectional data flow, making React applications more predictable and easier to debug.
>
> Props can be used to pass:
> * Strings
> * Numbers
> * Objects
> * Arrays
> * Functions
> * Components

### Example:

```jsx id="abc"
function User(props) {
    return <h1>Hello, {props.name}</h1>;
}

<User name="Komal" />
```

### One-Liner:
> "Props are read-only data passed from a parent component to a child component."

---

**State**
> "State is a built-in React object used to manage data that changes over time within a component.
>
> Unlike props, state is mutable and managed internally by the component. Whenever the state changes, React re-renders the component to reflect the updated UI.
>
> State is commonly used for:
> * Form inputs
> * Toggle buttons
> * API responses
> * Loading indicators
> * User interactions
>
> In modern React, state is managed using the `useState` Hook in functional components."

### Example:

```jsx id="abc"
const [count, setCount] = useState(0);
```

### One-Liner:
> "State is mutable data managed by a component that determines how the UI behaves and updates."

---

### Props vs State
| Props                  | State                 |
| ---------------------- | --------------------- |
| Immutable              | Mutable               |
| Passed by Parent       | Managed by Component  |
| Used for Communication | Used for Dynamic Data |
| Cannot be Modified     | Can be Updated        |
| External Data          | Internal Data         |

---

### Interview Answer
> "What is the difference between Props and State?"

Answer:
> "Props are used to pass read-only data from parent to child components, whereas State is used to manage mutable data within a component. Props help with component communication, while State controls the component's behavior and rendering. Together, they form the foundation of React's unidirectional data flow architecture."
>
> "Whenever State changes, React's reconciliation process compares the previous and current Virtual DOM and updates only the necessary parts of the Real DOM."

---

**Events**
> "Events in React are actions or occurrences that happen in the browser, such as button clicks, form submissions, mouse movements, and keyboard interactions this al are Events.
>
> React uses a Synthetic Event system, which is a wrapper around the browser's native event system. This provides a consistent API across different browsers and improves performance.
>
> Event handlers in React are typically written using camelCase naming conventions, such as `onClick`, `onChange`, and `onSubmit`.
>
> In my projects, I frequently use events for handling user interactions like form submissions, button clicks, search inputs, and navigation."

### Example:

```jsx id="6uc5x0"
function App() {
    const handleClick = () => {
        console.log("Button Clicked!");
    };

    return <button onClick={handleClick}>Click Me</button>;
}
```

### One-Liner:
> "Events allow React applications to respond to user interactions using the Synthetic Event system."

### React's Synthetic Event system 
> It is a wrapper around the browser's native events that provides a consistent interface across all browsers.
>
> Why React Uses Synthetic Events: Different browsers may implement events slightly differently. React normalizes them so your code behaves the same everywhere.

---

**Conditional Rendering**
> "Conditional Rendering is the process of displaying different UI elements based on specific conditions.
>
> React allows developers to render components conditionally using:
> * `if-else`
> * Ternary Operator (`? :`)
> * Logical AND (`&&`)
> * Switch Statements
>
> Conditional rendering is commonly used for:
> * Authentication
> * Loading states
> * Error handling
> * Role-based access control
> * Showing or hiding UI elements

### Example:

```jsx id="abc"
{
    isLoggedIn ? <Dashboard /> : <Login />;
}
```

### One-Liner:
> "Conditional Rendering allows React to display different UI elements based on application state or conditions."

---

**Lists**
> "Lists are used in React to render multiple elements dynamically from an array of data.
>
> React commonly uses the `map()` method to transform arrays into collections of JSX elements.
>
> When rendering lists, React requires a unique `key` prop for each element. Keys help React identify changes efficiently during the reconciliation process.
>
> Using proper keys improves rendering performance and prevents unexpected UI behavior.

### Example:

```jsx id="abc"
const users = ["Komal", "Siddhi", "Samarth"];

return (
    <ul>
        {users.map((user, index) => (
            <li key={index}>{user}</li>
        ))}
    </ul>
);
```

### Better Practice:

```jsx id="bh5rr2"
<li key={user.id}>{user.name}</li>
```

### One-Liner:
> "Lists enable React to render dynamic collections of data efficiently using the `map()` method and unique keys."

---

###  Interview Statement
> "React applications are fundamentally driven by events, state, and data. Events capture user interactions, conditional rendering controls what is displayed, and lists enable dynamic rendering of collections. Together, these concepts are essential for building interactive and scalable user interfaces."

---
