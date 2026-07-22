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
