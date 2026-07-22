## JavaScript
"JavaScript is a single-threaded, high-level, prototype-based, and dynamically typed language. It executes code using the JavaScript engine, such as V8 in Chrome. Internally, JavaScript uses a Call Stack to execute synchronous code, while asynchronous tasks are managed by Event Loop.

JavaScript is non-blocking and highly efficient for building modern applications. Its flexibility and support across browsers and servers have made it one of the most widely used programming languages in the industry."

- **Single-threaded:** Executes one task at a time.
- **High-level:** Easy to write without manual memory management.
- **Prototype-based:** Objects inherit from other objects via prototypes.
- **Dynamically typed:** Variable types are determined and can change at runtime.

## Variables
"Variables are SIMPLE NAME of STORED LOCATION that can be accessed and manipulated throughout a program. In JavaScript, variables can be declared using var, let, and const.

- **var:** is function-scoped and can be redeclared and updated.
- **let:** is block-scoped and can be updated but not redeclared within the same scope.
- **const:** is block-scoped and cannot be reassigned after initialization.

In modern JavaScript development, let and const are preferred because they provide better scoping and help avoid issues related to hoisting and unintended variable modifications."

## Data Types
"Data types define the kind of value that a variable can hold. JavaScript is a dynamically typed language, which means the datatype is determined at runtime.

JavaScript has two categories of datatypes:

- **Primitive Data Types:** 
String, Number, Boolean, Undefined, Null, Symbol
- **Non-Primitive (Reference) Data Types:** 
Object, Array, Function, Map

Primitive datatypes are stored by value, whereas non-primitive datatypes are stored by reference."

## Functions
"A function is a reusable block of code designed to perform a specific task. Functions help improve code reusability, modularity, and maintainability.

In JavaScript, functions are first-class citizens, which means they can be assigned to variables, passed as arguments, and returned from other functions. JavaScript supports various types of functions, including function declarations, function expressions, arrow functions, and anonymous functions."

## Arrays
"An array is an ordered collection of elements used to store multiple values in a single variable. JavaScript arrays are dynamic, meaning they can grow or shrink at runtime and can store elements of different datatypes.

Internally, arrays are special types of objects that use numeric indices. Common array methods are `map()`, `filter()`, `reduce()`and `find()`, which are widely used in development.

In React applications, I frequently use arrays for rendering lists of components using the `map()` method.

### example of map() -
```jsx
const users = [
  { id: 1, name: "Alice" },
  { id: 2, name: "Bob" },
  { id: 3, name: "Charlie" }
];

function App() {
  return (
    <div>
      {users.map(user => (
        <h2 key={user.id}>{user.name}</h2>
      ))}
    </div>
  );
}
```

## Objects
"An object is a collection of key-value pairs used to represent real-world entities and complex data structures. Objects are reference types and are one of the fundamental building blocks of JavaScript.

They allow us to group related data and behavior together. Properties store data, while methods define behavior.

I commonly use objects to manage user information and application state."

## Loops
"Loops are control structures used to execute a block of code repeatedly until a specified condition is met. They help reduce code duplication and make programs more efficient.

JavaScript provides several types of loops, including `for`, `while`, `do-while`, `for...of`, and `for...in`.

> * `for` loop is commonly used when the number of iterations is known.
> * `while` loop is used when the number of iterations is unknown.
> * `for...of` is used for iterating over iterable objects like arrays.
> * `for...in` is used for iterating over object properties.

In frontend development, I frequently use loops for traversing arrays, processing API data, and dynamically rendering UI components."

## Conditions
"Conditional statements allow a program to make decisions based on specific conditions. They control the flow of execution by determining which block of code should be executed.

JavaScript supports several conditional constructs, including `if`, `if-else`, `else-if`, `switch`, and the ternary operator.

Conditions work by evaluating expressions that return either `true` or `false`.

> For example:
>
> * `if-else` is suitable for simple decision-making.
> * `switch` is useful when handling multiple cases.
> * The ternary operator provides a concise way to write simple conditional expressions.

> In my projects, I use conditional statements for form validation, role-based access control, conditional rendering in React, and handling different API response states such as loading, success, and error."

---

## Scope
"Scope defines the accessibility and lifetime of variables, functions, and objects within a program. In JavaScript, it determines where a variable can be accessed during execution.

JavaScript primarily supports three types of scope:

- **Global Scope** – Variables declared outside any function or block can be accessed throughout the application.
- **Function Scope** – Variables declared using `var` inside a function are accessible only within that function.
- **Block Scope** – Variables declared using `let` and `const` inside a block (`{}`) are accessible only within that block.

## Hoisting
"Hoisting is JavaScript's default behavior of allocating memory for variable and function declarations during the creation phase of the execution context before the code is executed.
However, only declarations are hoisted—not initializations.

 * Variables declared with `var` are hoisted and initialized with `undefined`.
 * Variables declared with `let` and `const` are hoisted but remain in the Temporal Dead Zone until they are initialized.
 * Function declarations are completely hoisted, which means they can be invoked before their declaration in the code.

Hoisting does not physically move code to the top; rather, the JavaScript engine handles it internally during memory allocation.

### One-Liners
* **Scope:**
> "Scope determines where a variable is accessible within a program."

* **Hoisting:**
 > "Hoisting is the JavaScript engine's process of allocating memory for declarations before execution begins."

## Closures
"A closure is formed when an inner function retains access to variables from its lexical scope even after the outer function has completed execution.

In JavaScript, functions remember the environment in which they were created. This behavior enables data encapsulation and state preservation.

Closures are widely used for:
 * Data hiding
 * Private variables
 * Memoization
 * Debouncing
 * React Hooks
 * Module patterns

## Callbacks
"A callback is a function that is passed as an argument to another function and is executed after a particular task has been completed.

Callbacks are extensively used in JavaScript to handle asynchronous operations such as API requests, timers, and event handling.

For example, functions like `setTimeout()`, `addEventListener()`, and array methods such as `map()` and `forEach()` utilize callbacks.

While callbacks provide flexibility, excessive nesting can lead to 'Callback Hell,' which reduces code readability and maintainability.

Modern JavaScript addresses this issue through Promises and Async/Await."

## Promises
"A Promise is an object that represents the eventual completion or failure of an asynchronous operation.

 A Promise has three states:
 1. Pending – Initial state.
 2. Fulfilled – Operation completed successfully.
 3. Rejected – Operation failed.

Promises provide a cleaner and more structured way to handle asynchronous code compared to callbacks. They support methods such as `.then()`, `.catch()`, and `.finally()`.

Modern JavaScript applications heavily rely on Promises, and `async/await` is essentially syntactic sugar built on top of Promises.

In my projects, I have used Promises and `async/await` for API integrations, data fetching, and managing asynchronous workflows."

### One-Liners
* **Closure:**
  > "A closure is a function that remembers its lexical scope even after the outer function has finished execution."

* **Callback:**
  > "A callback is a function passed to another function to be executed later."

* **Promise:**
  > "A Promise is an object that represents the future result of an asynchronous operation."

> "Closures explain how React Hooks work, callbacks are the foundation of asynchronous programming, and Promises provide a scalable way to manage async operations."

**Async/Await**
"Async/Await is a modern syntax introduced in ES2017 for handling asynchronous operations in a more readable and synchronous-looking manner.

The `async` keyword makes a function return a Promise implicitly, while the `await` keyword pauses the execution of that function until the Promise is resolved or rejected.

Internally, Async/Await is built on top of Promises and does not introduce a new asynchronous mechanism. It simply provides cleaner syntax and improves code readability and maintainability.

In my projects, I have used Async/Await extensively for API calls, data fetching, and handling asynchronous workflows because it makes error handling with `try...catch` much simpler."

## Event Loop

"JavaScript is a single-threaded language that executes code using a Call Stack. However, it can handle asynchronous operations through the Event Loop.

When asynchronous tasks such as `setTimeout()`, API calls, or event listeners are encountered, they are delegated to Web APIs provided by the browser. Once completed, their callbacks are placed in either the Callback Queue or the Microtask Queue.

The Event Loop continuously monitors the Call Stack. When the Call Stack becomes empty, it gives priority to the Microtask Queue and then processes tasks from the Callback Queue.

This mechanism enables JavaScript to remain non-blocking and responsive despite being single-threaded.

Understanding the Event Loop is important because it explains the behavior of Promises, Async/Await, and asynchronous execution in JavaScript."

## Execution Context
"An Execution Context is the environment in which JavaScript code is evaluated and executed. It contains information about variables, functions, and the value of `this`.

JavaScript creates an Execution Context in two phases:

1. Memory Creation Phase:
    * Memory is allocated for variables and functions.
    * Variables declared with `var` are initialized with `undefined`.
    * Function declarations are stored entirely in memory.
2. Execution Phase:
    * Code is executed line by line.
    * Variable values are assigned.
    * Function calls create new Execution Contexts and are pushed onto the Call Stack.

There are three types of Execution Contexts:
* Global Execution Context
* Function Execution Context
* Eval Execution Context

Understanding Execution Context is fundamental because concepts like Hoisting, Scope, and Closures are built upon it."

### One-Liners
* **Async/Await:**
  > "Async/Await is syntactic sugar over Promises that makes asynchronous code look synchronous."
* **Event Loop:**
  > "The Event Loop enables JavaScript to handle asynchronous operations without blocking the main thread."

### Prototypal Inheritance

"JavaScript follows a prototypal inheritance model rather than classical inheritance.

Every JavaScript object has an internal reference to another object called its prototype. When a property or method is accessed on an object, JavaScript first looks for it on the object itself. If it is not found, JavaScript traverses the prototype chain until the property is found or the chain ends.

This mechanism is known as Prototype Chaining and enables objects to inherit properties and methods from other objects.

Prototypal inheritance improves code reusability and forms the foundation of JavaScript's object-oriented programming model."

## **`this` Keyword**

"The `this` keyword refers to the object that is currently executing the function. Its value is determined at runtime and depends on how the function is invoked.

 * In the global context, `this` refers to the global object (`window` in browsers).
 * Inside an object method, `this` refers to the object itself.
 * Inside a constructor function, `this` refers to the newly created instance.
 * In arrow functions, `this` is lexically inherited from the surrounding scope.

Understanding `this` is crucial because incorrect usage can lead to unexpected behavior, especially when working with callbacks, event handlers, and React components."

### High-Impact Statement:
"The value of `this` is not determined by where the function is defined; it is determined by how the function is called."

## Arrow Functions

"Arrow functions were introduced in ES6 to provide a shorter syntax for writing functions.

Unlike regular functions, arrow functions do not have their own `this`, `arguments`, `super`, or `new.target`. Instead, they inherit `this` from their lexical scope.

Arrow functions are commonly used in modern JavaScript because they improve readability and simplify callback-based code.

However, arrow functions should not be used as object methods or constructor functions because they do not create their own execution context for `this`."

### Example:

```javascript
const greet = () => {
    console.log("Hello World");
};
```
### High-Impact One-Liners
* **Execution Context:**
  > "Execution Context is the environment in which JavaScript code is executed."

* **Prototypal Inheritance:**
  > "JavaScript objects inherit properties and methods through the prototype chain."

* **`this` Keyword:**
  > "The value of `this` depends on how a function is invoked."

* **Arrow Functions:**
  > "Arrow functions provide concise syntax and inherit `this` from their surrounding scope."

### Interview Question:
> "What is the difference between a regular function and an arrow function?"
Answer:
> "The major difference is that regular functions create their own `this`, whereas arrow functions inherit `this` from their lexical scope. Additionally, arrow functions cannot be used as constructors and do not have their own `arguments` object."

---
## Debouncing
"Debouncing is a technique used to delay the execution of a function until a specified amount of time has passed since the last event was triggered.

It helps improve application performance by preventing unnecessary function calls during high-frequency events.

Common use cases include:
 * Search suggestions
 * Form validation
 * Auto-save functionality
 * Window resizing

For example, in a search bar, instead of making an API call on every keystroke, debouncing ensures the API request is made only after the user stops typing for a specified duration.

In frontend development, debouncing helps reduce API calls and improves user experience."

### One-Liner:
"Debouncing executes a function only after the user stops triggering an event."

## Throttling
"Throttling is a technique that limits the execution of a function to a fixed interval, regardless of how many times the event is triggered.

Unlike debouncing, throttling guarantees that the function will execute periodically.

Common use cases include:

 * Infinite scrolling
 * Mouse movement tracking
 * Window scrolling
 * Game controls

For example, while scrolling a page, throttling ensures that the scroll handler executes once every few milliseconds instead of firing continuously.

Throttling is primarily used for performance optimization in applications that deal with frequent events."

### One-Liner:
"Throttling ensures a function executes at regular intervals during continuous events."

### Difference

| Debouncing                | Throttling                 |
| ------------------------- | -------------------------- |
| Waits for inactivity      | Executes at intervals      |
| Best for search bars      | Best for scrolling         |
| Reduces unnecessary calls | Limits execution frequency |

## Currying
"Currying is a functional programming technique in which a function with multiple arguments is transformed into a sequence of functions, each accepting a single argument.

This improves code reusability, readability, and allows partial application of functions.

Currying is commonly used in libraries such as React, Redux, and Lodash.

It is particularly useful when creating configurable and reusable functions."

### Example:

```javascript id="w1j6qb"
function add(a) {
    return function (b) {
        return a + b;
    };
}

add(5)(10); // 15
```

### One-Liner:
"Currying transforms a function with multiple parameters into a chain of functions that each accept one parameter."

## Polyfills
"A polyfill is a piece of code that provides modern JavaScript functionality in environments or browsers that do not natively support it.

Polyfills help maintain compatibility across different browser versions by implementing missing features.

Examples include:
 * `Promise`
 * `Array.prototype.map`
 * `Array.prototype.includes`
 * `fetch`

In real-world applications, Babel and core-js are commonly used to automatically add polyfills during the build process.

Understanding polyfills is important because they ensure applications work consistently across multiple environments."

### One-Liner:
"A polyfill is code that implements modern JavaScript features in older environments that do not support them."

### Interviewer Follow-Up Question:
"Can you implement a debounce function?"

```javascript id="r4qllm"
function debounce(fn, delay) {
    let timer;

    return function (...args) {
        clearTimeout(timer);

        timer = setTimeout(() => {
            fn.apply(this, args);
        }, delay);
    };
}
```
## Memoization
"Memoization is an optimization technique used to improve performance by storing the results of expensive function calls and returning the cached result when the same inputs occur again.

Instead of recalculating the result every time, JavaScript retrieves it from memory, reducing computation time.

Memoization is particularly useful for:

 * Expensive calculations
 * Recursive functions
 * API response caching
 * React performance optimization (`useMemo`)

In React applications, I have used `useMemo` to avoid unnecessary recalculations during component re-renders."

### One-Liner:
"Memoization caches function results to avoid repeated computations."

## Generators
"Generators are special functions introduced in ES6 that can pause and resume their execution.

They are defined using the `function*` syntax and use the `yield` keyword to return values one at a time.

Unlike regular functions, generators do not execute completely when called. Instead, they return a Generator object that controls the execution flow.

Generators are useful for:
 * Lazy evaluation
 * Infinite sequences
 * State management
 * Custom iterators

They provide a memory-efficient way to work with large datasets."

### Example:
```javascript id="3u59jl"
function* numbers() {
    yield 1;
    yield 2;
    yield 3;
}
```

### One-Liner:
"Generators are functions that can pause and resume execution using the `yield` keyword."

## Iterators
"An Iterator is an object that enables sequential access to elements of a collection.

It follows the Iterator Protocol, which requires implementing a `next()` method that returns an object containing:
 * `value`
 * `done`

JavaScript's built-in data structures such as Arrays, Strings, Maps, and Sets are iterable by default.

Iterators are the foundation of `for...of` loops and work closely with generators."

### Example:
```javascript id="vjlwmv"
const arr = [1, 2, 3];
const iterator = arr[Symbol.iterator]();

iterator.next();
```

### One-Liner:
"Iterators provide a standardized way to traverse collections one element at a time."

## Event Delegation
"Event Delegation is a technique where a single event listener is attached to a parent element instead of multiple child elements.

It works because of JavaScript's event bubbling mechanism, where events propagate from the target element up through its ancestors.

Event Delegation provides several benefits:

 * Better performance
 * Reduced memory usage
 * Easier handling of dynamically added elements

In frontend applications, it is commonly used in tables, lists, and dynamically generated components."

### Example:
```javascript id="vdj8bn"
document
    .getElementById("parent")
    .addEventListener("click", (event) => {
        console.log(event.target);
    });
```

### One-Liner:
"Event Delegation uses event bubbling to handle events efficiently using a single parent listener."

## Modules
"Modules are reusable units of code that encapsulate variables, functions, and classes into separate files.
ES6 introduced native module support using the `import` and `export` keywords.

 Modules provide:
 * Better code organization
 * Reusability
 * Encapsulation
 * Maintainability

There are two types of exports:
 * Named Exports
 * Default Exports

Modern frontend frameworks like React heavily rely on modules to structure applications."

### Example:
```javascript id="a0r7tu"
// export
export const add = (a, b) => a + b;

// import
import { add } from "./math.js";
```

### One-Liner:
"Modules help organize and encapsulate code, making applications more scalable and maintainable."

### If an interviewer asks:
"Which of these concepts have you used in your projects?"
You can confidently answer:
* **Memoization:** `useMemo` in React.
* **Generators:** Used for learning and understanding lazy evaluation.
* **Iterators:** Used indirectly through `for...of` loops.
* **Event Delegation:** Used for handling clicks in dynamic lists.
* **Modules:** Used daily with `import` and `export` in React applications.

## Memory Leaks
"A memory leak occurs when memory that is no longer needed by an application is not released because references to it still exist.

Over time, memory leaks can lead to increased memory consumption, degraded performance, and even application crashes.

Common causes of memory leaks in JavaScript include:

 * Unremoved event listeners
 * Global variables
 * Timers (`setInterval`)
 * Closures holding unnecessary references
 * Detached DOM elements

In React applications, memory leaks often occur when asynchronous operations continue after a component has unmounted.

To prevent memory leaks, I ensure proper cleanup using `useEffect` cleanup functions, remove event listeners, and clear timers when they are no longer needed."

### One-Liner:
"A memory leak occurs when memory remains allocated because references to unused objects still exist."

## Garbage Collection
"Garbage Collection is JavaScript's automatic memory management mechanism that identifies and removes objects that are no longer reachable in memory.

JavaScript engines such as V8 primarily use the Mark-and-Sweep algorithm:
 1. Start from root objects (Global Object).
 2. Mark all reachable objects.
 3. Remove unmarked objects from memory.

This process helps developers focus on application logic instead of manual memory management.

However, garbage collection cannot reclaim memory if references to objects are still maintained, which is why memory leaks can still occur.

Understanding Garbage Collection is important for building performant and memory-efficient applications."

### One-Liner:
"Garbage Collection automatically frees memory occupied by objects that are no longer reachable."

## Shallow Copy vs Deep Copy
"Copying objects and arrays in JavaScript can be categorized into Shallow Copy and Deep Copy.

A Shallow Copy creates a new object but copies only the top-level properties. Nested objects continue to share the same references.

A Deep Copy creates a completely independent copy, including all nested objects and arrays."

### Shallow Copy Example:
```javascript id="8kqj3l"
const obj1 = {
    name: "Komal",
    address: {
        city: "Pune"
    }
};

const obj2 = { ...obj1 };
```

"In this case, `address` is still shared between both objects."

### Deep Copy Example:

```javascript id="0mns4u"
const obj2 = structuredClone(obj1);
```
Other methods:

* `JSON.parse(JSON.stringify())` (limitations)
* `structuredClone()`
* Lodash `cloneDeep()`

### Comparison Table
| Shallow Copy             | Deep Copy                  |
| ------------------------ | -------------------------- |
| Copies first level only  | Copies all levels          |
| Shares nested references | Creates independent copies |
| Faster                   | More expensive             |
| Uses Spread Operator     | Uses `structuredClone()`   |

### One-Liners
* **Memory Leak:**
  > "Memory leaks occur when unused objects remain in memory due to active references."

* **Garbage Collection:**
  > "Garbage Collection automatically removes unreachable objects from memory."

* **Shallow Copy:**
  > "A shallow copy copies only the first level of an object."

* **Deep Copy:**
  > "A deep copy creates a completely independent clone of an object, including all nested structures."

### High-Impact Interview Statement

> "Memory leaks and Garbage Collection are closely related. JavaScript's Garbage Collector can only free memory if objects become unreachable. If references are unintentionally retained through closures, event listeners, or global variables, memory leaks occur."
