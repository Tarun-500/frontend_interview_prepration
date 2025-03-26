### 1) Difference Between let, var, const
### 2) Rest parameter vs Spread operator 
### 3) Function Vs methods
### 4) Entry Control Loop Vs Exit Control Loop
### 5) slice Vs splice method <small>  (slice give always new array and splice changes the original array) </small>
### 6) Lexical VS Dynamic Scope
### 7) map VS foreach
### 8) async await VS promises 
### 9) Difference between debouncing and throttling.
### 10) Shallow Copy vs Deep Copy in JavaScript
### 11) Call by value VS call by reference
### 12) pass by value vs pass by refrence 
### 13) primitive vs non-primitive 
### 14) Immutable vs mutable  
<details>
<summary>  <h3> 15) Null vs undefined </h3>    </summary>
  <small>
<strong> Undefined: </strong>   It means a variable has been declared but hasn't been assigned a value yet. Essentially, it represents the absence of any value. It's like an empty container that hasn't been filled yet.
If you declare a variable x but don't assign any value, its value will be undefined.
    
```
let  x;  
console.log(x); // output : undefined
```
<strong>Null: </strong> It's explicitly assigned by a programmer to represent an empty or non-existent value. It's like saying, "there is nothing here on purpose."
For example:

If you assign null to a variable y, you're explicitly saying that y has no value.

 ```
let  y = null;
console.log(y); // output: null
```
  </small>
</details>



<details>
<summary>  <h3> 16) Event Bubbling vs Event Capturing </h3>    </summary>
  <small> 

### **Event Bubbling**
**Definition:**
The event starts from the target element (child) and moves up to the parent elements.

**Example:**
```javascript
// Event Bubbling Example
document.getElementById("child").addEventListener("click", function() {
  console.log("Child Clicked");
});

document.getElementById("parent").addEventListener("click", function() {
  console.log("Parent Clicked");
});
```
**Output (when clicking on child):**
```
Child Clicked
Parent Clicked
```

### **Event Capturing (Trickling)**
**Definition:**
The event starts at the top (root/parent elements) and moves down to the target (child element).

**Example:**
```javascript
// Event Capturing Example
document.getElementById("parent").addEventListener("click", function() {
  console.log("Parent Clicked");
}, true); // Capturing enabled

document.getElementById("child").addEventListener("click", function() {
  console.log("Child Clicked");
}, true);
```
**Output (when clicking on child):**
```
Parent Clicked
Child Clicked
```

## **Key Difference:**
- **Bubbling:** Event moves **upward** from child to parent.
- **Capturing:** Event moves **downward** from parent to child.
- `addEventListener(event, callback, true)` enables capturing mode.
- Default is **bubbling** when `false` is used (or omitted).

  </small>
</details>
