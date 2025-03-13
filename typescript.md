# TypeScript Basics

  <details>
 <summary>  <h2>What is TypeScript and Why Was It Created? </h2>  </summary>
 <small>
    TypeScript is a **programming language developed by Microsoft in 2012**. It is a **superset of JavaScript** that adds **static typing** and better error handling. 
   It was created because JavaScript had **no type safety, debugging issues, and was hard to manage in big projects**. TypeScript helps by **catching errors early** and making code more reliable.
   It compiles to plain JavaScript and works in any browser or JavaScript environment.
 </small>
</details>



 
<details>
  <summary> <h2>  What are the Key Features of TypeScript?</h2> </summary>

```ts
// 1. Static Typing & Interfaces
let num: number = 10;
num = "Hello"; // ❌ Error

interface User { 
  name: string; 
  age: number; 
}
let user: User = { name: "Alice", age: 25 };

// 2. Classes & OOP Features
class Person {
  private name: string;
  constructor(name: string) { this.name = name; }
  greet() { return `Hello, my name is ${this.name}`; }
}

// 3. Type Inference
let count = 5;  // TypeScript infers `number`

// 4. Generics
function identity<T>(value: T): T { return value; }
console.log(identity<string>("Hello")); // Output: Hello

// 5. Enum (Custom Data Types)
enum Direction { Up, Down, Left, Right }
let move: Direction = Direction.Up;

// 6. Compiles to JavaScript
// TypeScript transpiles to plain JavaScript, making it work everywhere JS does.
