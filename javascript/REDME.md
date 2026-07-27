# JavaScript Basics

## What is JavaScript?

JavaScript (JS) is a high-level, interpreted programming language used to make web pages interactive and dynamic. It is one of the core technologies of web development, alongside HTML and CSS.

- **HTML** → Structure of a webpage
- **CSS** → Styling of a webpage
- **JavaScript** → Functionality and interactivity

JavaScript runs directly in the browser and can also be used on the server side with Node.js.

---

## Features of JavaScript

- Lightweight and fast
- Interpreted language
- Object-oriented programming support
- Event-driven programming
- Cross-platform compatibility
- Supports asynchronous programming
- Can be used for both frontend and backend development

---

## How JavaScript Works

1. User opens a webpage.
2. Browser loads HTML and CSS.
3. JavaScript code is executed by the browser's JavaScript Engine.
4. JS interacts with the webpage using the DOM (Document Object Model).
5. The webpage responds to user actions such as clicks, typing, and scrolling.

---

## Adding JavaScript to HTML

### Internal JavaScript


<script>
  console.log("Hello World");
</script>

###External JavaScript

<script src="script.js"></script>


Variables :-

Variables are used to store data.

let name = "Pankaj";
const age = 20;
var city = "Dehradun";

Difference Between var, let, and const:-

| Keyword | Reassign | Redeclare | Scope    |
| ------- | -------- | --------- | -------- |
| var     | Yes      | Yes       | Function |
| let     | Yes      | No        | Block    |
| const   | No       | No        | Block    |


###Loops:-

1-For Loop

for(let i = 1; i <= 5; i++) {
  console.log(i);
}

2-While Loop

let i = 1;

while(i <= 5) {
  console.log(i);
  i++;
}

3-For...of Loop

let fruits = ["Apple", "Banana"];

for(let fruit of fruits) {
  console.log(fruit);
}



Summary

JavaScript is the programming language of the web. It enables dynamic content, user interaction, API communication, and modern web application development. Learning JavaScript is an important step toward becoming a Frontend or Full Stack Developer.