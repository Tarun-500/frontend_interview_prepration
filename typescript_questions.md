1) TypeScript - is a superset (all features of JavaScript and adds additional features new syntax) of JavaScript that adds optional static typing, allowing developers to catch errors early, improve code quality, and enhance tooling support while still compiling down to plain JavaScript for execution in web browsers or Node.js environments.




2) Tuple - in TypeScript is like an array but with fixed types for each element. It allows you to specify the type of each element in a specific order. For example:

let person: [string, number] = ['John', 30];



3) Enums - there are two types of enums first is string and 2nd number and an enum in TypeScript is a way to define a set of named constants, providing more readable and descriptive names for numeric values.

Enums:- Enums is used to group constants ,Enums comes into two types string and
enum Direction {
  Up,
  Down,
  Left,
  Right,
}

Number:- Numeric enums are auto incremented, means if we assign the first value it will auto increment rest of the values.
 Example: enum Direction {Up = 1,Down,Left,Right,}  (then down will be 2 , left 3 and right will be 4)



4) Decorators - are a powerful feature in TypeScript that allows you to add additional functionality to classes, methods, properties, and other parts of your code without directly modifying the original code. They act like annotations that provide metadata about a piece of code. decorators inspired form the python , TO use decorators, we have to set
the compiler option in the tsconfigjson file.


5) Generics - in TypeScript allow you to create reusable components that work with a variety of types rather than a single one. They enable you to define functions, classes, or interfaces that can work with any data type while still maintaining type safety.

function getFirstElement<T>(arr: T[]): T | undefined {
  return arr.length > 0 ? arr[0] : undefined;
}

const numbers = [1, 2, 3, 4, 5];
const strings = ['apple', 'banana', 'cherry'];

console.log(getFirstElement(numbers)); // Output: 1
console.log(getFirstElement(strings)); // Output: 'apple'



6) Conditional types - in TypeScript are like questions for types. Depending on the answer to the question (the condition), TypeScript gives you a different type. For example, you can ask TypeScript if a type is an array, and based on the answer, you get a type that represents whether it's true or false.

 type IsArray<T> = T extends any[] ? true : false;

// Usage examples:
type Result1 = IsArray<number[]>;   // true
type Result2 = IsArray<string[]>;   // true
type Result3 = IsArray<number>;     // false
In this example, IsArray is a conditional type that checks if T is an array (T extends any[]). If it is, the result is true; otherwise, it's false.


7) Type aliases - in TypeScript allow you to create custom names for existing types or combinations of types. They provide a way to give more meaningful names to types, making your code easier to understand and maintain.

type Age = number;
type Name = string;

type Person = {
  name: Name;
  age: Age;
};

const data: Person = {
  name: 'John',
  age: 30,
};


8) Namespaces - By using namespaces, we can prevent naming conflicts because a namespace provides a container in which we can organize functions, variables, or classes into a group. Each namespace has its own scope, which separates it from other namespaces, allowing us to use different identifiers in different namespaces without any conflicts. This enhances code readability and maintainability and also allows us to adhere to naming conventions.

namespace Geometry {
  export const PI = 3.14;

  export function calculateArea(radius: number): number {
    return PI * radius * radius;
  }
}

const circleArea = Geometry.calculateArea(5);
console.log(circleArea); // Output: 78.5


9) Advantage of ts - 
Static typing:- TypeScript introduces static typing for JavaScript, catching type-related errors early.
Readability:- Type annotations make code self-documenting and easier to understand.
Early error detection:- TypeScript detects many common bugs at compile time.
Tooling support:- TypeScript integrates well with modern tools, enhancing developer productivity.
Compatibility:- TypeScript is a superset of JavaScript, allowing gradual adoption and leveraging of features.
Modern language features:- TypeScript supports ECMAScript features along with additional syntax and features.
Strong community:- TypeScript has a vibrant community and ecosystem, facilitating support and knowledge sharing.





10) ts vs js  -
Static Typing:- TypeScript has static typing for catching errors early; JavaScript doesn't.
Tooling:- TypeScript offers better tooling support than JavaScript.
Compatibility:- TypeScript is a superset of JavaScript, meaning JavaScript code works in TypeScript.
Readability:- TypeScript code is more readable due to type annotations; JavaScript might need more documentation.
Type Safety:- TypeScript provides more type safety than JavaScript.
Community:- JavaScript has a larger community and more resources than TypeScript.
Learning Curve:- TypeScript has a slight learning curve compared to JavaScript.
Object-Oriented Programming (OOP):- TypeScript supports OOP features like classes, interfaces, inheritance, encapsulation, and polymorphism, while JavaScript's OOP support is more limited.


11) tsconfig.json - file is used to configure TypeScript projects, specifying compiler options, file inclusion/exclusion rules, and other settings. It allows developers to customize how TypeScript code is compiled and processed.


12) data types in ts- 

Number: Represents numeric values, including integers and floating-point numbers.
String: Represents textual data, such as words, sentences, or characters.
Boolean: Represents a logical value, either true or false.
Array: Represents a collection of elements of the same type, which can be accessed using index positions.
Tuple: Represents an array-like structure where the type of each element is known and fixed.
Enum: Represents a set of named constants, providing more readable and descriptive names for numeric values.
Any: Represents any type of value, providing maximum flexibility but sacrificing type safety.
Void: Represents the absence of a value, typically used as the return type of functions that don't return anything.
Null and Undefined: Represents the absence of a value or an uninitialized value, respectively.
Unknown: Represents values of an unknown type, providing stricter type checking compared to any.



13) modules in ts - 
Modules in TypeScript allow you to organize code into reusable and maintainable units. They prevent naming conflicts by encapsulating functionality within a local scope. By defining interfaces and functions within modules, you can access them in other files without global conflicts, ensuring better code organization and readability.


14) Interface - 
In TypeScript, an interface is like a blueprint that defines the structure of an object, specifying what properties and methods it should have. It helps ensure consistency and type safety in your code.
 
interface Person {
  name: string;
  age: number;
  greet(): void;
}
 
const person: Person = {
  name: "Alice",
  age: 30,
  greet() {
    console.log(`Hello, my name is ${this.name} and I'm ${this.age} years old.`);
  }
}; 

person.greet();




15) 
Access modifiers - in TypeScript are keywords that control the visibility and accessibility of class members (properties and methods). They determine whether a member can be accessed from within the class itself, from outside the class, or from subclasses.

In TypeScript, there are three main access modifiers that control the visibility of class members:

Public (default): Members are accessible from anywhere, both within the class and from outside the class.
Protected: Members are accessible within the class where they are defined and within subclasses (inheritance), but not accessible from outside the class.
Private: Members are only accessible within the class where they are defined. They are not accessible from outside the class or from subclasses.
These modifiers help in encapsulating the internal implementation details of a class, promoting data encapsulation and improving code maintainability and security.



16) DOM manipulation in ts - In a TypeScript we can do DOM manipulation like in JavaScript, but there is some
difference in syntax, let's see the examples:
Example: Select element by ID
var btn=<HTMLElement>document,getElementByld('btn')
Example: Select element by Class
let smallimg: = document.getElementsByClassName('smallimg');
