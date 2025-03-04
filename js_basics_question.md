## 1) What are functions? 
<small>
  A function is a block of code that performs a specific task and can be called anywhere in the program.
  
  ```
  function greet() {
  console.log("Hello!");
}
greet(); // Output: Hello!
 ```
</small>

## 2) What are methods? 
<small>
A method is a function that belongs to an object. It is called using the object.

  ```
const person = {
  name: "Rahul",
  sayHello: function() {
    console.log("Hello, " + this.name);
  }
};
person.sayHello(); // Output: Hello, Rahul

```
</small>


