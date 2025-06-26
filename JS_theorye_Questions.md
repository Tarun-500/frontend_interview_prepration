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

 


## 6) this keyword use in js  -  this in JavaScript refers to the current object or context. 

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



14) Event handling - in JavaScript involves responding to user interactions, like clicks or keystrokes, by defining functions (event handlers) that execute when those events occur. These functions are then attached to specific HTML elements using event listeners.



15 ) Enhanced Object Literals - mean that if you have a property named name and a variable with the same name, you can assign the variable directly without repeating the property name, like name instead of name: name."



17) Call bind apply - 


18) Hoisting -  in JavaScript, means you can use variables and functions before declaring them, because JavaScript moves their declarations to the top of the scope.


19) Currying, in JavaScript, is when a function takes one argument at a time and returns a new function for the next argument.

20) Generates - 

21) Iterators -

22) Temporal Dead Zone (TDZ) in JavaScript - 

23) automatic return - in JS, when we use an arrow function, if we are using a  single code, then we do not need to write "return" .

24) prefix and postfix

25) strict check

26) JavaScript is dynamically typed, not strictly typed. In typescript, strictly typed here, we have to give typeof to every declaration

27) Stack memory (Primitive) is copied, Heap memory (Non-Primitive) is not copied, it will give a reference

30) Prototype 

31) Singleton Pattern in JavaScript
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
52) Type casting in JavaScript - making any string into a number or number to a string is type casting or changing any type to another type is type casting

53) unary operator
54) threads
