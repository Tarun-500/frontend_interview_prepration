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
  <summary> <h2>  What are the Key Features of TypeScript? </h2> </summary>

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

 
 
 ```
</details>
 
<details>
  <summary> <h2>  What is the Difference Between TypeScript and JavaScript? </h2></summary>

```ts
// 1. TypeScript is a Superset of JavaScript
// TypeScript extends JavaScript with additional features like static typing.

let message: string = "Hello"; // ✅ TypeScript
// let message = "Hello";      // ✅ JavaScript (No type enforcement)

// 2. Static Typing vs. Dynamic Typing
// JavaScript is dynamically typed, while TypeScript enforces static types.

let num: number = 10;  // ✅ TypeScript (Static Typing)
// let num = 10;       // ✅ JavaScript (Dynamic Typing)

// 3. Compilation
// TypeScript needs to be compiled to JavaScript before execution.

tsc index.ts   // ✅ Compiles TypeScript to JavaScript

// 4. Interfaces & Generics (TypeScript Only)
interface User {
  name: string;
  age: number;
}
function identity<T>(value: T): T { return value; }

// 5. Better Tooling & Error Handling
// TypeScript provides better IntelliSense, autocompletion, and early error detection.
 
```
</details>


 
<details>
  <summary> <h2> What are Interfaces in TypeScript and Why Use Them?</h2> </summary>

```ts
// 1. What is an Interface?
// An interface defines the structure of an object without implementing it.

interface User {
  name: string;
  age: number;
  isAdmin?: boolean; // Optional Property
}

// 2. Why Use Interfaces?
// - Helps enforce structure in objects
// - Improves code readability and maintainability
// - Enables better type-checking at compile-time

let user: User = { name: "Alice", age: 25 };

// 3. Interface with Functions
interface MathOperation {
  (a: number, b: number): number;
}

const add: MathOperation = (x, y) => x + y;

// 4. Extending Interfaces (Inheritance)
interface Employee extends User {
  salary: number;
}

let employee: Employee = { name: "Bob", age: 30, salary: 50000 };

// 5. Interface vs. Type Alias
// Interfaces are extendable, whereas Type Aliases are more flexible with unions.
type ID = string | number;
 ```
</details>



 
<details>
  <summary> <h2>  What are Generics in TypeScript and Why Use Them? </h2> </summary>

```ts
// 1. What are Generics?
// Generics allow us to write flexible and reusable code by using placeholders for types.

function identity<T>(value: T): T {
  return value;
}

console.log(identity<string>("Hello")); // Output: Hello
console.log(identity<number>(42));      // Output: 42

// 2. Why Use Generics?
// - Improves code reusability
// - Provides type safety without losing flexibility
// - Works with functions, classes, and interfaces

// 3. Generics with Arrays
function getFirstElement<T>(arr: T[]): T {
  return arr[0];
}

console.log(getFirstElement<string>(["A", "B", "C"])); // Output: A

// 4. Generics in Interfaces
interface Box<T> {
  value: T;
}

let numberBox: Box<number> = { value: 100 };
let stringBox: Box<string> = { value: "TypeScript" };

// 5. Generics in Classes
class DataStorage<T> {
  private data: T[] = [];
  addItem(item: T) {
    this.data.push(item);
  }
  getItems(): T[] {
    return this.data;
  }
}

let numberStorage = new DataStorage<number>();
numberStorage.addItem(10);
console.log(numberStorage.getItems()); // Output: [10]
 
 ```

</details>

 
<details>
  <summary> <h2> What is the Difference Between Type and Interface in TypeScript? </h2></summary>

```ts
// 1. Definition
// - Interface is used to define object structure.
// - Type can be used for objects, unions, primitives, etc.

interface User {
  name: string;
  age: number;
}

type Employee = {
  name: string;
  age: number;
  salary: number;
};

// 2. Extending (Interface vs Type)
interface Admin extends User {
  permissions: string[];
}

type Manager = Employee & { department: string };

// 3. Type Supports Union, Interface Does Not
type ID = string | number;  // ✅ Valid
// interface ID = string | number; // ❌ Error

// 4. Type Can Use Computed Properties, Interface Cannot
type Colors = "red" | "green" | "blue";
type ColorMap = { [K in Colors]: string };

// 5. When to Use?
// ✅ Use Interface when defining object structures
// ✅ Use Type when working with primitives, unions, or function signatures
 ```
</details>

 
<details>
  <summary> <h2>  What are Access Modifiers in TypeScript?</h2></summary>

```ts
// 1. What are Access Modifiers?
// Access modifiers control the visibility of properties and methods in a class.
// - public: Accessible from anywhere
// - private: Accessible only within the class
// - protected: Accessible within the class and its subclasses

// 2. Example of Access Modifiers
class Person {
  public name: string;       // Can be accessed anywhere
  private age: number;       // Can only be accessed inside this class
  protected salary: number;  // Can be accessed in subclasses

  constructor(name: string, age: number, salary: number) {
    this.name = name;
    this.age = age;
    this.salary = salary;
  }

  public getDetails(): string {
    return `Name: ${this.name}, Age: ${this.age}`;
  }
}

let p = new Person("Alice", 30, 50000);
console.log(p.name);      // ✅ Works (public)
// console.log(p.age);    // ❌ Error (private)
// console.log(p.salary); // ❌ Error (protected)

// 3. Protected Modifier Example (Accessible in Subclass)
class Employee extends Person {
  constructor(name: string, age: number, salary: number) {
    super(name, age, salary);
  }

  getSalary(): number {
    return this.salary; // ✅ Works (protected can be accessed in subclass)
  }
}

let emp = new Employee("Bob", 28, 60000);
console.log(emp.getSalary()); // ✅ Works
```
</details>



 
<details>
  <summary> <h2>What is the Difference Between Abstract Class and Interface in TypeScript?</h2></summary>

```ts
// 1. Abstract Class vs. Interface Overview
// - Abstract class can have method implementations.
// - Interface only defines method signatures, no implementation.

abstract class Animal {
  abstract makeSound(): void; // Must be implemented by subclasses
  move(): void {
    console.log("Moving...");
  }
}

interface Bird {
  fly(): void;
}

// 2. Abstract Class Example
class Dog extends Animal {
  makeSound(): void {
    console.log("Bark!");
  }
}

let dog = new Dog();
dog.makeSound(); // Output: Bark!
dog.move(); // Output: Moving...

// 3. Interface Example
class Sparrow implements Bird {
  fly(): void {
    console.log("Flying...");
  }
}

let bird = new Sparrow();
bird.fly(); // Output: Flying...

// 4. Key Differences
// - Abstract classes can have constructors, interfaces cannot.
// - A class can implement multiple interfaces but can only extend one abstract class.
// - Interfaces are more flexible for defining structures, while abstract classes provide reusable behavior.

```
</details>



 
<details>
  <summary> <h2> What is Type Inference in TypeScript?</h2> </summary>

```ts
// 1. What is Type Inference?
// TypeScript automatically determines the type of a variable without explicit annotation.

let num = 10;   // TypeScript infers 'number'
let text = "Hi"; // TypeScript infers 'string'

// 2. Function Return Type Inference
function add(a: number, b: number) {
  return a + b; // TypeScript infers return type as 'number'
}

let result = add(5, 10); // 'result' is inferred as 'number'

// 3. Array Inference
let numbers = [1, 2, 3]; // TypeScript infers 'number[]'

```
</details>

 
<details>
  <summary> <h2> What are Union Types in TypeScript?</h2></summary>

```ts
// 1. What are Union Types?
// Union types allow a variable to have multiple types.

let value: string | number; // 'value' can be a string or a number

value = "Hello"; // ✅ Valid
value = 42;      // ✅ Valid
// value = true; // ❌ Error: 'boolean' is not allowed

// 2. Union Types in Functions
function display(id: string | number) {
  console.log("ID:", id);
}

display(101);    // ✅ Output: ID: 101
display("A102"); // ✅ Output: ID: A102

// 3. Using Union Types in Arrays
let data: (string | number)[] = [1, "Two", 3, "Four"];
console.log(data); // ✅ Output: [1, "Two", 3, "Four"]
```
</details>



 
<details>
  <summary> <h2> What are Optional Properties in TypeScript?</h2></summary>

```
// 1. What are Optional Properties?
// Optional properties in TypeScript allow object properties to be optional using '?'.

interface User {
  name: string;
  age?: number; // 'age' is optional
}

let user1: User = { name: "Alice" };      // ✅ Valid (age is missing)
let user2: User = { name: "Bob", age: 30 }; // ✅ Valid (age is provided)
```
</details>



<details> 
  <summary> <h2> What is the "any" Type in TypeScript?</h2></summary>
  
``` 
// 1. What is the 'any' Type?
// The 'any' type allows a variable to hold any value, disabling type checking.

let value: any = 10;
value = "Hello";  // ✅ No error
value = true;     // ✅ No error

// 2. Why Avoid 'any'?
// Using 'any' removes TypeScript’s type safety, leading to potential runtime errors.

function logMessage(message: any) {
  console.log(message);
}

logMessage(123);     // ✅ Works
logMessage("Hello"); // ✅ Works

```
</details>



# 🔥 100 Most Common TypeScript Interview Questions 🚀  

## 📌 **Basic TypeScript Questions**  
1. What is TypeScript, and how is it different from JavaScript?  
2. How do you install and set up TypeScript?  
3. How do you compile a TypeScript file into JavaScript?  
4. What are the key features of TypeScript?  
5. What is static typing in TypeScript?  
6. What is Type Inference in TypeScript?  
7. What are Union Types in TypeScript?  
8. What is an Interface in TypeScript, and why use it?  
9. What is a Type Alias in TypeScript?  
10. What is the difference between Type Alias and Interface?  

## 📌 **Types and Variables**  
11. What are the basic data types in TypeScript?  
12. What are optional properties in TypeScript?  
13. What is the "any" type in TypeScript, and when should you use it?  
14. What is the "unknown" type in TypeScript?  
15. What is the difference between "any" and "unknown" in TypeScript?  
16. What is the "never" type in TypeScript?  
17. What is the difference between "let", "const", and "var" in TypeScript?  
18. What is the "readonly" modifier in TypeScript?  
19. What are Tuple types in TypeScript?  
20. What are Enum types in TypeScript?  

## 📌 **Functions in TypeScript**  
21. How do you define a function in TypeScript?  
22. What are function parameter types in TypeScript?  
23. What is a default parameter in TypeScript?  
24. What is a rest parameter in TypeScript?  
25. What is function overloading in TypeScript?  
26. How does TypeScript handle function return types?  
27. What is an arrow function in TypeScript?  
28. What are optional parameters in TypeScript functions?  
29. How do you specify a function type in TypeScript?  
30. How do you use the "this" keyword in TypeScript functions?  

## 📌 **Object-Oriented Programming in TypeScript**  
31. What are classes in TypeScript?  
32. What are access modifiers (`public`, `private`, `protected`) in TypeScript?  
33. What is an abstract class in TypeScript?  
34. What is the difference between an abstract class and an interface?  
35. How do you extend a class in TypeScript?  
36. How do you implement an interface in TypeScript?  
37. What is method overriding in TypeScript?  
38. What is the "super" keyword in TypeScript?  
39. How do you create a singleton class in TypeScript?  
40. How do you use static properties and methods in TypeScript?  

## 📌 **Advanced TypeScript Concepts**  
41. What are Generics in TypeScript?  
42. How do you create a generic function in TypeScript?  
43. What are generic constraints in TypeScript?  
44. What are generic classes in TypeScript?  
45. What are mapped types in TypeScript?  
46. What are conditional types in TypeScript?  
47. What are template literal types in TypeScript?  
48. What is a utility type in TypeScript?  
49. How does TypeScript support type casting?  
50. What is the difference between type assertion and type casting?  

## 📌 **Modules and Namespaces**  
51. What are ES6 modules in TypeScript?  
52. How do you export and import a module in TypeScript?  
53. What are TypeScript namespaces?  
54. How do you declare and use a namespace in TypeScript?  
55. What is the difference between namespaces and modules?  
56. How do you create a module in TypeScript?  
57. What is a declaration file in TypeScript (`.d.ts`)?  
58. How do you use third-party libraries in TypeScript?  
59. How do you configure module resolution in TypeScript?  
60. What is a TypeScript triple-slash directive?  

## 📌 **TypeScript Configuration and Compilation**  
61. What is the `tsconfig.json` file in TypeScript?  
62. How do you enable strict mode in TypeScript?  
63. What are TypeScript compiler options?  
64. What is "noImplicitAny" in TypeScript?  
65. What does "strictNullChecks" do in TypeScript?  
66. How do you compile TypeScript code for different module formats?  
67. How does TypeScript support decorators?  
68. What are experimental decorators in TypeScript?  
69. How do you use path mapping in TypeScript?  
70. What is the difference between `include` and `exclude` in `tsconfig.json`?  

## 📌 **Error Handling and Debugging**  
71. What is TypeScript’s error handling mechanism?  
72. How do you catch errors in TypeScript?  
73. What is the difference between compile-time and runtime errors in TypeScript?  
74. How does TypeScript help with debugging?  
75. What is the "strictPropertyInitialization" option in TypeScript?  
76. How do you use Type Guards in TypeScript?  
77. What are assertion functions in TypeScript?  
78. How do you debug TypeScript code in VS Code?  
79. How do you handle async/await errors in TypeScript?  
80. What is the difference between `try-catch` and `error boundaries` in TypeScript?  

## 📌 **TypeScript Best Practices**  
81. What are some best practices for writing TypeScript code?  
82. How do you enforce code style in TypeScript?  
83. How do you improve TypeScript performance?  
84. What are some common TypeScript pitfalls?  
85. How do you document TypeScript code?  
86. How do you handle large-scale TypeScript projects?  
87. What are the benefits of using TypeScript in React?  
88. How do you use TypeScript with Redux?  
89. How do you migrate a JavaScript project to TypeScript?  
90. What is the role of TypeScript in modern front-end development?  

## 📌 **Miscellaneous TypeScript Questions**  
91. How does TypeScript compare to Flow?  
92. What are TypeScript decorators, and how do they work?  
93. How does TypeScript support functional programming?  
94. What are discriminated unions in TypeScript?  
95. How do you implement dependency injection in TypeScript?  
96. What is the role of TypeScript in back-end development?  
97. How does TypeScript improve security in applications?  
98. What are advanced types in TypeScript?  
99. How do you optimize TypeScript build times?  
100. What’s new in the latest TypeScript version?  





# 🔥 100 More Advanced TypeScript Interview Questions 🚀  

## 📌 **Basic TypeScript Concepts**  
1. What are the disadvantages of TypeScript?  
2. What are the benefits of using TypeScript over JavaScript?  
3. Can TypeScript run directly in a browser? Why or why not?  
4. What is the role of Babel in TypeScript projects?  
5. What is Duck Typing in TypeScript?  
6. How does TypeScript handle implicit and explicit types?  
7. How does TypeScript handle `null` and `undefined`?  
8. What is the difference between `null` and `undefined` in TypeScript?  
9. What are intersection types in TypeScript?  
10. How does TypeScript handle multiple types for the same variable?  

## 📌 **TypeScript Data Types**  
11. What is a Hybrid Type in TypeScript?  
12. What is a Literal Type in TypeScript?  
13. How does TypeScript handle Boolean values?  
14. What are Indexable Types in TypeScript?  
15. What are Callable Types in TypeScript?  
16. What is the difference between an array and a tuple in TypeScript?  
17. What is an indexed signature in TypeScript?  
18. What is the difference between structural typing and nominal typing in TypeScript?  
19. What are Recursive Types in TypeScript?  
20. What are Branded Types in TypeScript?  

## 📌 **Functions & Methods in TypeScript**  
21. What is the difference between an anonymous function and a named function in TypeScript?  
22. How do you define a function signature in TypeScript?  
23. How does TypeScript handle function currying?  
24. Can you have an optional return type in TypeScript?  
25. What is a function expression in TypeScript?  
26. How do you enforce a function to always return a value?  
27. What is a Polymorphic Function in TypeScript?  
28. What are Predicate Functions in TypeScript?  
29. How does TypeScript handle function context (`this`)?  
30. How does TypeScript handle variadic functions?  

## 📌 **Classes & Object-Oriented Programming (OOP)**  
31. What is the difference between a private method and a protected method in TypeScript?  
32. What is the difference between a static and an instance method?  
33. How do you define a read-only property in a TypeScript class?  
34. What is the difference between a setter and a constructor in TypeScript?  
35. Can TypeScript interfaces extend multiple interfaces?  
36. How do you override a method in TypeScript?  
37. What are mixins in TypeScript?  
38. How do you implement a Singleton pattern in TypeScript?  
39. What is Dependency Injection in TypeScript?  
40. What is the difference between "shallow copy" and "deep copy" in TypeScript objects?  

## 📌 **Advanced TypeScript Features**  
41. What is a Partial Type in TypeScript?  
42. What are Readonly Types in TypeScript?  
43. How do you use "keyof" in TypeScript?  
44. What is the use of "infer" in TypeScript?  
45. What is a Conditional Type in TypeScript?  
46. What are Intersection and Union Types in TypeScript?  
47. How does TypeScript handle object merging?  
48. What is a Distributive Conditional Type?  
49. How do you use `as const` in TypeScript?  
50. How do you ensure immutability in TypeScript?  

## 📌 **Modules & Namespaces in TypeScript**  
51. What is the difference between `export default` and named exports in TypeScript?  
52. How do you import a JSON file in TypeScript?  
53. How do you resolve module conflicts in TypeScript?  
54. What is the use of `import type` in TypeScript?  
55. How does TypeScript support dynamic imports?  
56. What are Barrel Modules in TypeScript?  
57. How do you create a custom module in TypeScript?  
58. What is the difference between a module and a namespace in TypeScript?  
59. How does TypeScript handle circular dependencies?  
60. How do you load environment variables in a TypeScript project?  

## 📌 **Error Handling & Debugging**  
61. How do you enable strict mode in TypeScript?  
62. What is TypeScript’s `strictFunctionTypes` option?  
63. What is the `noImplicitReturns` compiler option in TypeScript?  
64. What are Assertion Functions in TypeScript?  
65. How does TypeScript handle exception handling?  
66. How does TypeScript prevent runtime errors?  
67. What is a Type Guard in TypeScript?  
68. What are Assertion Signatures in TypeScript?  
69. What is the difference between `throw` and `assert` in TypeScript?  
70. What is a Type Predicate in TypeScript?  

## 📌 **TypeScript with Frontend Frameworks**  
71. How do you use TypeScript with React?  
72. What is the difference between `React.FC` and function components in TypeScript?  
73. How do you define props in a React TypeScript component?  
74. How do you define state in a React TypeScript component?  
75. How do you use TypeScript with Redux?  
76. How do you handle async actions with TypeScript and Redux?  
77. How do you define custom hooks in TypeScript?  
78. How do you use TypeScript with Next.js?  
79. How do you integrate TypeScript with Vue.js?  
80. How do you use TypeScript with Angular?  

## 📌 **TypeScript with Backend Development**  
81. How do you use TypeScript with Node.js?  
82. What is the best way to structure a TypeScript Node.js project?  
83. How do you use TypeScript with Express.js?  
84. How do you validate request bodies in TypeScript?  
85. What is the best way to handle TypeScript errors in a backend app?  
86. How do you use TypeScript with GraphQL?  
87. How do you use TypeScript with Sequelize?  
88. How do you use TypeScript with Mongoose?  
89. What is the difference between TypeORM and Prisma in TypeScript?  
90. How do you create a REST API with TypeScript?  

## 📌 **Miscellaneous TypeScript Questions**  
91. How does TypeScript handle Date objects?  
92. How do you define global variables in TypeScript?  
93. How do you enforce immutability in TypeScript?  
94. How do you use TypeScript with Jest for testing?  
95. How do you write an ESLint rule for TypeScript?  
96. How do you optimize TypeScript performance?  
97. What is the `@ts-ignore` directive, and when should you use it?  
98. What are the latest features in the newest TypeScript version?  
99. How does TypeScript handle destructuring?  
100. What are some common mistakes developers make in TypeScript?





# 🔥 100 TypeScript Coding Interview Questions 🚀  

## 📌 **Basic TypeScript Coding Questions**  
1. Write a TypeScript function to check if a number is even or odd.  
2. Write a TypeScript function to reverse a string.  
3. Implement a function that finds the largest number in an array.  
4. Write a function that calculates the factorial of a number using recursion.  
5. Write a TypeScript function that returns the Fibonacci sequence up to `n` terms.  
6. Implement a function to check if a string is a palindrome.  
7. Write a function to find the sum of all elements in an array.  
8. Implement a function that removes duplicate values from an array.  
9. Write a function to find the second largest number in an array.  
10. Write a function to check if two arrays are equal.  

## 📌 **Functions & TypeScript Features**  
11. Implement a function using function overloading in TypeScript.  
12. Write a function with optional parameters in TypeScript.  
13. Create a function that takes a union type as an argument.  
14. Write a function that accepts a callback and executes it.  
15. Implement a function that uses generics for type safety.  
16. Write a function that takes a tuple as an argument.  
17. Create a function that swaps two values using generics.  
18. Write a function that converts a given string to title case.  
19. Implement a function that finds the intersection of two arrays.  
20. Write a function that flattens a nested array.  

## 📌 **Object-Oriented Programming (OOP) in TypeScript**  
21. Create a TypeScript class for a `Person` with name and age properties.  
22. Implement a class that has private and public properties.  
23. Create a class that has a static method.  
24. Implement inheritance in TypeScript with a `Car` class and a `Tesla` subclass.  
25. Write a TypeScript class with a constructor and getter/setter methods.  
26. Implement method overriding in TypeScript.  
27. Write a class that implements an interface in TypeScript.  
28. Implement an abstract class and a subclass in TypeScript.  
29. Create a class that contains a read-only property.  
30. Implement a singleton class in TypeScript.  

## 📌 **Advanced TypeScript Concepts**  
31. Write a TypeScript function that uses mapped types.  
32. Implement a function that converts an object’s keys to uppercase.  
33. Write a function that deep clones an object in TypeScript.  
34. Implement a utility type that makes all properties optional.  
35. Write a function that merges two objects while preserving type safety.  
36. Implement a conditional type that checks if a type is a string.  
37. Write a function that converts an object’s keys to a tuple.  
38. Implement a generic function that filters an array based on a condition.  
39. Write a function that extracts keys from an object that have a specific type.  
40. Implement a function that capitalizes the first letter of each word in a string.  

## 📌 **Array & String Manipulation**  
41. Write a function that counts the occurrences of each character in a string.  
42. Implement a function that finds the longest word in a sentence.  
43. Write a function that sorts an array of numbers in ascending order.  
44. Implement a function that returns a random element from an array.  
45. Write a function that finds the most frequently occurring element in an array.  
46. Implement a function that rotates an array `n` times.  
47. Write a function that splits a string into words without using `.split()`.  
48. Implement a function that reverses words in a sentence.  
49. Write a function that removes falsy values from an array.  
50. Implement a function that converts a camelCase string to snake_case.  

## 📌 **Data Structures & Algorithms in TypeScript**  
51. Implement a Stack using a class in TypeScript.  
52. Implement a Queue using a class in TypeScript.  
53. Write a function to find the maximum subarray sum (Kadane’s Algorithm).  
54. Implement a function that finds the longest common prefix in an array of strings.  
55. Write a function that finds the missing number in an array of 1 to N.  
56. Implement a function to check if a given string has balanced parentheses.  
57. Write a function that finds the shortest path in a grid (BFS).  
58. Implement a function that finds the largest rectangle in a histogram.  
59. Write a function that detects a cycle in a linked list.  
60. Implement a Trie (prefix tree) in TypeScript.  

## 📌 **Asynchronous Programming in TypeScript**  
61. Write a function that simulates a delay using `setTimeout()`.  
62. Implement a function that fetches data from an API using `fetch()`.  
63. Write a function that uses `Promise.all()` to execute multiple async operations.  
64. Implement a function that retries a failed API call up to `n` times.  
65. Write a function that limits the number of concurrent API requests.  
66. Implement a function that resolves a promise after a random delay.  
67. Write an async function that reads a file in TypeScript (Node.js).  
68. Implement an async function that writes data to a file in TypeScript.  
69. Write a function that measures the execution time of an async function.  
70. Implement an async function that processes an array sequentially.  

## 📌 **TypeScript with React & Frontend Development**  
71. Create a React component with TypeScript props and state.  
72. Implement a custom React hook in TypeScript.  
73. Write a TypeScript function that fetches and displays data in React.  
74. Create a React component with TypeScript Context API.  
75. Implement a React component that handles form validation using TypeScript.  
76. Write a TypeScript function that uses `useEffect` with a dependency array.  
77. Implement lazy loading in a TypeScript React app.  
78. Write a TypeScript function that caches API responses in local storage.  
79. Implement a function that debounces an input field in TypeScript.  
80. Write a function that paginates API results in a React component.  

## 📌 **Node.js & Backend Development in TypeScript**  
81. Create a simple Express server in TypeScript.  
82. Implement a function that hashes a password using bcrypt in TypeScript.  
83. Write a function that validates JWT tokens in TypeScript.  
84. Implement a function that connects to a PostgreSQL database using TypeORM.  
85. Write a function that creates and validates cookies in TypeScript.  
86. Implement a REST API endpoint that fetches data from a database.  
87. Write a function that logs requests and responses in an Express server.  
88. Implement a function that handles errors globally in an Express app.  
89. Write a function that queues tasks using Redis in TypeScript.  
90. Implement a function that streams large files in a Node.js server.  

## 📌 **Miscellaneous TypeScript Coding Questions**  
91. Write a function that memoizes the results of a function in TypeScript.  
92. Implement a function that compresses a string using run-length encoding.  
93. Write a function that generates a unique identifier (UUID) in TypeScript.  
94. Implement a function that performs deep equality check of two objects.  
95. Write a function that validates email addresses using TypeScript.  
96. Implement a function that converts CSV data to JSON in TypeScript.  
97. Write a function that calculates the Levenshtein distance between two strings.  
98. Implement a function that finds all anagrams of a word in a list.  
99. Write a function that extracts all unique words from a large text file.  
100. Implement a function that schedules recurring tasks in TypeScript.  

