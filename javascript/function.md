# JavaScript Functions

## Introduction

Functions are one of the most important concepts in JavaScript. A function is a reusable block of code designed to perform a specific task. Instead of writing the same code multiple times, you can place it inside a function and call it whenever needed.

Functions help make code:
- Reusable
- Readable
- Modular
- Easy to maintain
- Easy to debug

---

# What is a Function?

A function is a block of code that executes only when it is called.

### Syntax

```javascript
function functionName() {
  // Code to execute
}
```

### Example

```javascript
function greet() {
  console.log("Hello, World!");
}

greet();
```

Output

```
Hello, World!
```

---

# Function Declaration

A function declaration is the most common way to create a function.

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(5, 3));
```

Output

```
8
```

---

# Function Parameters and Arguments

### Parameters

Parameters are variables listed in the function definition.

```javascript
function greet(name) {
  console.log("Hello " + name);
}
```

Here, `name` is a parameter.

### Arguments

Arguments are the actual values passed to the function.

```javascript
greet("Pankaj");
```

Output

```
Hello Pankaj
```

---

# Return Statement

The `return` statement sends a value back to the caller.

```javascript
function multiply(a, b) {
  return a * b;
}

let result = multiply(4, 5);

console.log(result);
```

Output

```
20
```

---

# Function Expression

A function can also be stored inside a variable.

```javascript
const add = function(a, b) {
  return a + b;
};

console.log(add(10, 20));
```

Output

```
30
```

---

# Anonymous Function

A function without a name is called an anonymous function.

```javascript
const greet = function() {
  console.log("Hello!");
};

greet();
```

---

# Arrow Functions

Arrow functions provide a shorter syntax for writing functions.

### Syntax

```javascript
const functionName = () => {
  // Code
};
```

### Example

```javascript
const greet = () => {
  console.log("Hello!");
};

greet();
```

---

## Arrow Function with Parameters

```javascript
const square = (num) => {
  return num * num;
};

console.log(square(5));
```

Output

```
25
```

---

## Implicit Return

If there is only one expression, you can omit `return` and curly braces.

```javascript
const add = (a, b) => a + b;

console.log(add(5, 10));
```

Output

```
15
```

---

# Default Parameters

Default values are used when no argument is passed.

```javascript
function greet(name = "Guest") {
  console.log("Hello " + name);
}

greet();
greet("Pankaj");
```

Output

```
Hello Guest
Hello Pankaj
```

---

# Rest Parameters

Rest parameters allow a function to accept multiple values.

```javascript
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4, 5));
```

Output

```
15
```

---

# Callback Functions

A callback function is passed as an argument to another function.

```javascript
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}

function sayBye() {
  console.log("Goodbye!");
}

greet("Pankaj", sayBye);
```

Output

```
Hello Pankaj
Goodbye!
```

---

# Higher-Order Functions

A higher-order function is a function that accepts another function as an argument or returns a function.

Example:

```javascript
const numbers = [1, 2, 3, 4];

const doubled = numbers.map(num => num * 2);

console.log(doubled);
```

Output

```
[2, 4, 6, 8]
```

Examples of higher-order methods:
- map()
- filter()
- reduce()
- forEach()
- find()

---

# Recursive Functions

A recursive function calls itself until a condition is met.

### Example: Factorial

```javascript
function factorial(n) {
  if (n === 1)
    return 1;

  return n * factorial(n - 1);
}

console.log(factorial(5));
```

Output

```
120
```

---

# Immediately Invoked Function Expression (IIFE)

An IIFE runs immediately after it is created.

```javascript
(function () {
  console.log("Executed immediately");
})();
```

Output

```
Executed immediately
```

---

# Function Scope

Variables declared inside a function are only accessible within that function.

```javascript
function demo() {
  let message = "Hello";
  console.log(message);
}

demo();
```

Trying to access `message` outside the function will cause an error.

---

# Local Scope

```javascript
function test() {
  let age = 20;
  console.log(age);
}
```

`age` only exists inside the function.

---

# Global Scope

```javascript
let username = "Pankaj";

function display() {
  console.log(username);
}

display();
```

Global variables can be accessed from anywhere in the program.

---

# Hoisting

Function declarations are hoisted.

```javascript
greet();

function greet() {
  console.log("Hello");
}
```

Output

```
Hello
```

Function expressions are **not** hoisted.

```javascript
sayHi();

const sayHi = function () {
  console.log("Hi");
};
```

This will produce an error.

---

# The `this` Keyword

Inside an object method, `this` refers to the current object.

```javascript
const person = {
  name: "Pankaj",

  greet() {
    console.log(this.name);
  }
};

person.greet();
```

Output

```
Pankaj
```

---

# Pure Functions

A pure function:
- Always returns the same output for the same input.
- Does not modify external data.

```javascript
function add(a, b) {
  return a + b;
}
```

---

# Function vs Arrow Function

| Function | Arrow Function |
|----------|----------------|
| Uses `function` keyword | Uses `=>` syntax |
| Has its own `this` | Inherits `this` from parent scope |
| Can be hoisted (declaration) | Not hoisted like declarations |
| Best for object methods | Best for callbacks and short functions |

---

# Common Built-in Functions

```javascript
console.log()
```

Prints output to the console.

```javascript
parseInt("100")
```

Converts a string to an integer.

```javascript
parseFloat("10.5")
```

Converts a string to a floating-point number.

```javascript
isNaN("Hello")
```

Checks whether a value is Not-a-Number.

```javascript
Number("123")
```

Converts a value to a number.

```javascript
String(123)
```

Converts a value to a string.

---



# Summary

- Functions are reusable blocks of code.
- Parameters receive values, while arguments pass values.
- `return` sends data back to the caller.
- Arrow functions provide concise syntax.
- Callback and higher-order functions are widely used in modern JavaScript.
- Understanding functions is essential before learning asynchronous JavaScript, DOM manipulation, and React.

---

