# JavaScript Objects & Array Methods

## Introduction

Objects and Arrays are two of the most important data structures in JavaScript.

- **Objects** are used to store data in the form of **key-value pairs**.
- **Arrays** are used to store **multiple values in a single variable**.

Understanding these concepts is essential for working with JavaScript, React, APIs, and modern web development.

---

# JavaScript Objects

## What is an Object?

An object is a collection of properties.

Each property has:
- A key (property name)
- A value

### Syntax

```javascript
const person = {
  name: "Pankaj",
  age: 20,
  city: "Dehradun"
};
```

---

## Accessing Object Properties

### Dot Notation

```javascript
console.log(person.name);
console.log(person.age);
```

### Bracket Notation

```javascript
console.log(person["city"]);
```

Bracket notation is useful when the property name is stored in a variable.

```javascript
const key = "name";

console.log(person[key]);
```

---

## Adding Properties

```javascript
person.country = "India";

console.log(person);
```

---

## Updating Properties

```javascript
person.age = 21;

console.log(person);
```

---

## Deleting Properties

```javascript
delete person.city;

console.log(person);
```

---

## Nested Objects

```javascript
const student = {
  name: "Rahul",
  address: {
    city: "Delhi",
    state: "Delhi"
  }
};

console.log(student.address.city);
```

---

## Object Methods

Objects can also contain functions.

```javascript
const person = {
  name: "Pankaj",

  greet() {
    console.log("Hello!");
  }
};

person.greet();
```

---

## Object.keys()

Returns all property names.

```javascript
const person = {
  name: "Pankaj",
  age: 20
};

console.log(Object.keys(person));
```

Output

```javascript
["name", "age"]
```

---

## Object.values()

Returns all values.

```javascript
console.log(Object.values(person));
```

Output

```javascript
["Pankaj", 20]
```

---

## Object.entries()

Returns key-value pairs.

```javascript
console.log(Object.entries(person));
```

Output

```javascript
[
  ["name", "Pankaj"],
  ["age", 20]
]
```

---

## Object.assign()

Copies properties from one object to another.

```javascript
const obj1 = { a: 1 };
const obj2 = { b: 2 };

const result = Object.assign({}, obj1, obj2);

console.log(result);
```

Output

```javascript
{ a: 1, b: 2 }
```

---

## Spread Operator with Objects

```javascript
const person = {
  name: "Pankaj",
  age: 20
};

const updatedPerson = {
  ...person,
  city: "Dehradun"
};

console.log(updatedPerson);
```

---

# JavaScript Arrays

## What is an Array?

An array stores multiple values in one variable.

```javascript
const fruits = ["Apple", "Banana", "Mango"];
```

---

## Accessing Array Elements

```javascript
console.log(fruits[0]);
console.log(fruits[2]);
```

---

## Updating Array Elements

```javascript
fruits[1] = "Orange";
```

---

## Array Length

```javascript
console.log(fruits.length);
```

---

# Common Array Methods

---

## push()

Adds an element to the end.

```javascript
const numbers = [1, 2, 3];

numbers.push(4);

console.log(numbers);
```

Output

```javascript
[1, 2, 3, 4]
```

---

## pop()

Removes the last element.

```javascript
numbers.pop();

console.log(numbers);
```

Output

```javascript
[1, 2, 3]
```

---

## shift()

Removes the first element.

```javascript
numbers.shift();
```

---

## unshift()

Adds an element at the beginning.

```javascript
numbers.unshift(0);
```

---

## includes()

Checks if a value exists.

```javascript
const fruits = ["Apple", "Banana"];

console.log(fruits.includes("Apple"));
```

Output

```javascript
true
```

---

## indexOf()

Returns the index of an element.

```javascript
console.log(fruits.indexOf("Banana"));
```

Output

```javascript
1
```

---

## join()

Converts an array into a string.

```javascript
const fruits = ["Apple", "Banana", "Mango"];

console.log(fruits.join(", "));
```

Output

```javascript
Apple, Banana, Mango
```

---

## slice()

Returns a portion of an array.

Original array remains unchanged.

```javascript
const numbers = [1, 2, 3, 4, 5];

console.log(numbers.slice(1, 4));
```

Output

```javascript
[2, 3, 4]
```

---

## splice()

Adds, removes, or replaces elements.

```javascript
const numbers = [1, 2, 3, 4];

numbers.splice(1, 2);

console.log(numbers);
```

Output

```javascript
[1, 4]
```

---

## reverse()

```javascript
const numbers = [1, 2, 3];

numbers.reverse();

console.log(numbers);
```

Output

```javascript
[3, 2, 1]
```

---

## sort()

Sorts an array.

```javascript
const numbers = [4, 2, 1, 3];

numbers.sort();

console.log(numbers);
```

### Sorting Numbers Correctly

```javascript
numbers.sort((a, b) => a - b);
```

Descending Order

```javascript
numbers.sort((a, b) => b - a);
```

---

# Higher Order Array Methods

These methods are used frequently in React and modern JavaScript.

---

## forEach()

Loops through every element.

```javascript
const numbers = [1, 2, 3];

numbers.forEach((num) => {
  console.log(num);
});
```

---

## map()

Creates a new array.

```javascript
const numbers = [1, 2, 3];

const doubled = numbers.map((num) => num * 2);

console.log(doubled);
```

Output

```javascript
[2, 4, 6]
```

---

## filter()

Returns elements that satisfy a condition.

```javascript
const numbers = [10, 25, 30, 15];

const result = numbers.filter((num) => num > 20);

console.log(result);
```

Output

```javascript
[25, 30]
```

---

## find()

Returns the first matching element.

```javascript
const users = [
  { id: 1 },
  { id: 2 },
  { id: 3 }
];

const user = users.find((u) => u.id === 2);

console.log(user);
```

Output

```javascript
{ id: 2 }
```

---

## some()

Returns true if at least one element matches.

```javascript
const numbers = [2, 4, 5];

console.log(numbers.some((num) => num % 2 !== 0));
```

Output

```javascript
true
```

---

## every()

Returns true if all elements match.

```javascript
const numbers = [2, 4, 6];

console.log(numbers.every((num) => num % 2 === 0));
```

Output

```javascript
true
```

---

## reduce()

Reduces an array to a single value.

```javascript
const numbers = [1, 2, 3, 4];

const sum = numbers.reduce((total, current) => {
  return total + current;
}, 0);

console.log(sum);
```

Output

```javascript
10
```

---

## flat()

Flattens nested arrays.

```javascript
const arr = [1, [2, 3], [4, [5]]];

console.log(arr.flat());
```

Output

```javascript
[1, 2, 3, 4, [5]]
```

---

## flatMap()

Maps and flattens in one step.

```javascript
const numbers = [1, 2, 3];

const result = numbers.flatMap((num) => [num, num * 2]);

console.log(result);
```

Output

```javascript
[1, 2, 2, 4, 3, 6]
```

---

# Chaining Methods

You can combine multiple array methods together.

```javascript
const numbers = [10, 20, 30, 40];

const result = numbers
  .filter(num => num > 15)
  .map(num => num * 2);

console.log(result);
```

Output

```javascript
[40, 60, 80]
```

---

# When to Use Which Method

| Method | Purpose |
|---------|---------|
| push() | Add to end |
| pop() | Remove last element |
| shift() | Remove first element |
| unshift() | Add to beginning |
| slice() | Copy part of an array |
| splice() | Modify original array |
| map() | Transform data |
| filter() | Select matching data |
| find() | Find first matching item |
| forEach() | Iterate over elements |
| reduce() | Calculate a single value |
| some() | Check if any element matches |
| every() | Check if all elements match |
| sort() | Sort elements |
| reverse() | Reverse order |
| includes() | Check if value exists |
| indexOf() | Find index of value |
| join() | Convert array to string |

---

# Summary

- Objects store data as key-value pairs.
- Arrays store ordered collections of values.
- Objects are ideal for representing real-world entities.
- Arrays are ideal for storing lists of data.
- Methods like `map()`, `filter()`, `find()`, and `reduce()` are essential for modern JavaScript and React.
- Mastering Objects and Array Methods will make working with APIs, DOM manipulation, and React applications much easier.

---

