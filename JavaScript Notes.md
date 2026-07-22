<!-- 
## JavaScript
### Explaination
 -->

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
String
Number
Boolean
Undefined
Null
Symbol
BigInt
- **Non-Primitive (Reference) Data Types:** 
Object
Array
Function
Map
.............etc

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

##

