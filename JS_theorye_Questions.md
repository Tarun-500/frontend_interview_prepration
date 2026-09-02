## 1) Lexical scoping - 


## 2) Dynamic Scoping - In dynamic scoping, the search for a variable is based on its name. If it's not found in the current block, then it goes up the chain of function calls until it finds a variable with that name. So, instead of looking at where the variable is defined, it looks at where the function that's currently running was called from.


## 3) Lexical VS Dynamic Scope :

   Dynamic scoping, when a function is called, looks for variables not where they are defined but where the function was called from. This is different from lexical scoping, where variables are searched for based on where they are written in the code. So, even though they're both ways to find variables, they work differently.


## 4) Block Scope - Block scope means variables can be used only within the particular block of code where they are defined, such as within a function or loop, and cannot be accessed outside of it.

function blockScope(){
    let a = 50 
    Console.log(a) //  Output: 50
}
console.log(a)  // ReferenceError: a is not defined

for (let i = 0; i < 5; i++) {
  console.log(i);
}

console.log(i); // This will throw an error because 'i' is not defined outside the loop

 
## 005) What is event Delegation? 
    Event Delegation is a JS technique where we attach a single event listener to a parent element instead of adding multiple event listeners to individual            child elements.

## 006) What is event handling?
      Event handling means making a webpage interactive whenever a user does any action like click, hover, drag, type, or other actions.

## 007) What is event loop?
    The Event Loop is not a part of our code; it is a JavaScript mechanism. Since JavaScript is a single-threaded language, it can only do one task at a time. The Event Loop sends time-taking requests to the background until the currently running tasks in the stack are completed, keeping the website interactive and working.  
      

## 6) This keyword used in JS  -  this in JavaScript refers to the current object or context. 

const person = {
  name: 'John',
  greet: function() {
    console.log('Hello, my name is ' + this.name);
  }
};

person.greet(); // Output: Hello, my name is John

## 7) Callback function - In JavaScript, a callback function is a function that is passed as an argument to another function and is executed later, typically after the completion of some operation or task. Callback functions are commonly used in asynchronous programming to handle tasks that depend on the completion of other tasks or events. They allow for flexible and efficient control flow by enabling actions to be executed asynchronously or in response to certain events.

A function that takes a callback as an argument
function greet(name, callback) {
  console.log("Hello, " + name + "!");
  // Execute the callback function after greeting
  callback();
}

// Callback function definition
function sayGoodbye() {
  console.log("Goodbye!");
}

// Calling the greet function with a callback
greet("Alice", sayGoodbye);

// Function that takes a callback as an argument
function greet(name, callback) {
  console.log("Hello, " + name + "!");
  // Execute the callback function after greeting
  callback();
}

// Callback function definition
function sayGoodbye() {
  console.log("Goodbye!");
}

// Calling the greet function with a callback
greet("Alice", sayGoodbye);


## 8) Recursion - Recursion in JavaScript is when a function calls itself to solve a problem. It's like a loop where the function repeats itself until it reaches a base case to stop. For example, a function to calculate factorial:

function factorial(n) {
  if (n === 0 || n === 1) {
    return 1; // Base case
  } else {
    return n * factorial(n - 1); // Recursive call
  }
}

console.log(factorial(5)); // Outputs: 120




## 9) closest() - is like finding the nearest family member who matches a certain description in a group.
const targetElement = document.querySelector('.target');
const parentElement = targetElement.closest('#parent');
console.log(parentElement); // Output: <div id="parent">...</div>


## 10) match()  - is like searching for a specific word or pattern in a book or text.
const sentence = "The quick brown fox jumps over the lazy dog";
const wordToFind = "fox";
const result = sentence.match(wordToFind);
console.log(result); // Output: ["fox"]



## 11) What is JavaScript? JavaScript is a programming language often used to make websites more interactive.



## 12) Primitive (pass by value)  Data Types - In JavaScript, there are six (numbers, strings, booleans, null, and undefined) primitive data types that cannot be manipulated by objects



13) non-primitive (pass by reference) - data types include objects, arrays, and functions, which are more complex and can hold multiple values or operations.



14) Event handling in JavaScript involves responding to user interactions, like clicks or keystrokes, by defining functions (event handlers) that execute when those events occur. These functions are then attached to specific HTML elements using event listeners.



15 ) Enhanced Object Literals - mean that if you have a property named name and a variable with the same name, you can assign the variable directly without repeating the property name, like name instead of name: name."



17) Call bind apply - 


18) Hoisting -  in JavaScript, means you can use variables and functions before declaring them, because JavaScript moves their declarations to the top of the scope.


19) Currying, in JavaScript, is when a function takes one argument at a time and returns a new function for the next argument.

20) Generates - 

21) Iterators -

22) Temporal Dead Zone (TDZ) in JavaScript - 

23) automatic return - in JS, when we use an arrow function, if we are using a  single code, then we do not need to write "return".

24) prefix and postfix

25) strict check

26) JavaScript is dynamically typed, not strictly typed. In typescript, strictly typed here, we have to give typeof to every declaration

27) Stack memory (Primitive) is copied, Heap memory (Non-Primitive) is not copied, it will give a reference

30) Prototype 

31) Singleton Pattern in JavaScript - # Singleton Pattern in JavaScript

## 🚀 What is Singleton?
- **Singleton** means → only one object can exist from that pattern.  
- Even if you try to create it again, it will always **return the same instance**.  

---

## ✅ Example in JavaScript (Functional Way)

```js
const Singleton = (function () {
  let instance; // here we keep the single copy

  return function () {
    if (!instance) {
      instance = { name: "I am the only one" }; // create once
    }
    return instance; // always return the same
  };
})();

const a = Singleton();
const b = Singleton();

console.log(a === b); // true

```


32) Factory Pattern in JavaScript
33) Observer Pattern in JavaScript
34) Decorator Pattern in JavaScript
35) Command Pattern in JavaScript
36) Iterator Pattern in JavaScript
37) Strategy Pattern in JavaScript
38) Template Method Pattern in JavaScript
39) Adapter Pattern in JavaScript
40) Composite Pattern in JavaScript

41) Object Literal in JavaScript
42) Constructor in JavaScript
43) Prototype in JavaScript
44) Inheritance in JavaScript
45) Encapsulation in JavaScript
46) Abstraction in JavaScript
47) Polymorphism in JavaScript
48) `this` keyword in JavaScript
49) bind, call, apply in JavaScript
50) async/await in JavaScript
51) Type Conversion in JavaScript - using - * / with string like ("1" - 1) = 0
52) Type casting in JavaScript - making any string into a number or a number to a string is type casting, or changing any type to another type is type casting

53) unary operator
54) threads

What is a closure in JavaScript, and how does it allow an inner function to access outer scope variables?

How do you create private variables in JavaScript using closures?

What will for (var i = 0; i < 3; i++) { setTimeout(() => console.log(i), 1000); } output, and how do you fix it using a closure?

What is hoisting in JavaScript, and how does the engine handle variable vs. function declarations?

What is the Temporal Dead Zone (TDZ), and how does hoisting differ between var, let, and const?

What happens if you call a function expression before defining it compared to a function declaration?

How does prototypal inheritance work in JavaScript, and what is the difference between __proto__ and prototype?

When you access a property on an object, how exactly does JS traverse the prototype chain, and where does it end?

What is the difference between Object.create(null) and creating a standard object using {}?

What are the three states of a Promise, and how does it solve the issue of callback hell?

How do Promise.all(), Promise.allSettled(), Promise.race(), and Promise.any() differ?

How does the Event Loop handle Promise microtasks versus setTimeout macrotasks, and which executes first?

What is recursion, and why is a base case mandatory?

What causes a Maximum Call Stack Size Exceeded error, and how do you prevent it?

What is Tail Call Optimization (TCO), and how does call stack memory behave during deep recursion?
