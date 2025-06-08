
## 📚 JavaScript Methods Cheat Sheet (Explained)

This document contains a categorized and easy-to-understand list of the most commonly used JavaScript methods. Perfect for interview prep, revision, and daily coding tasks.

---

### 🔹 1. Array Methods

| Method        | Description                                          | Example                              |
|---------------|------------------------------------------------------|--------------------------------------|
| `push()`      | Adds an element at the end of the array              | `arr.push(4)`                        |
| `pop()`       | Removes the last element of the array                | `arr.pop()`                          |
| `shift()`     | Removes the first element of the array               | `arr.shift()`                        |
| `unshift()`   | Adds element(s) at the beginning                     | `arr.unshift(1)`                     |
| `concat()`    | Joins two or more arrays                            | `arr1.concat(arr2)`                  |
| `join()`      | Converts array to string                             | `arr.join('-')`                      |
| `slice()`     | Returns selected elements in a new array            | `arr.slice(1, 3)`                    |
| `splice()`    | Adds/removes elements at a position                 | `arr.splice(1, 2)`                   |
| `map()`       | Creates new array by applying a function            | `arr.map(x => x*2)`                  |
| `filter()`    | Returns items that match a condition                | `arr.filter(x => x > 5)`             |
| `reduce()`    | Reduces array to a single value                     | `arr.reduce((a,b) => a + b)`         |
| `forEach()`   | Runs function on each item (no return)              | `arr.forEach(x => console.log(x))`   |
| `find()`      | Returns the first element that matches              | `arr.find(x => x > 10)`              |
| `includes()`  | Checks if array contains an element                 | `arr.includes(5)`                    |
| `indexOf()`   | Returns index of first match                        | `arr.indexOf(10)`                    |
| `sort()`      | Sorts array (default is by string)                  | `arr.sort()`                         |
| `reverse()`   | Reverses the array order                            | `arr.reverse()`                      |
| `flat()`      | Flattens nested arrays                             | `[1, [2, 3]].flat()`                 |
| `every()`     | Returns true if all items match condition           | `arr.every(x => x > 0)`              |
| `some()`      | Returns true if any item matches condition          | `arr.some(x => x > 0)`               |

---

### 🔹 2. String Methods

| Method         | Description                                      | Example                                |
|----------------|--------------------------------------------------|----------------------------------------|
| `charAt()`     | Returns char at specified index                  | `'abc'.charAt(1)` → `'b'`              |
| `charCodeAt()` | Returns ASCII of character                       | `'A'.charCodeAt(0)`                    |
| `concat()`     | Combines two or more strings                     | `'a'.concat('b')`                      |
| `includes()`   | Checks if string contains a substring            | `'hello'.includes('ell')`              |
| `indexOf()`    | Index of first occurrence of substring           | `'hello'.indexOf('e')`                 |
| `lastIndexOf()`| Index of last occurrence                         | `'ababc'.lastIndexOf('b')`             |
| `slice()`      | Extracts a part of the string                    | `'hello'.slice(1, 3)`                  |
| `substring()`  | Similar to slice, cannot use negative indexes    | `'hello'.substring(1, 4)`              |
| `replace()`    | Replaces part of a string                        | `'hi'.replace('i', 'ello')`            |
| `toLowerCase()`| Converts to lowercase                            | `'HELLO'.toLowerCase()`                |
| `toUpperCase()`| Converts to uppercase                            | `'hello'.toUpperCase()`                |
| `trim()`       | Removes whitespace from both ends                | `' hello '.trim()`                     |
| `split()`      | Splits string into array                        | `'a,b'.split(',')`                     |
| `startsWith()` | Checks if string starts with substring           | `'apple'.startsWith('a')`              |
| `endsWith()`   | Checks if string ends with substring             | `'apple'.endsWith('e')`                |
| `padStart()`   | Pads beginning of string to a length             | `'5'.padStart(3, '0')` → `'005'`       |
| `padEnd()`     | Pads end of string to a length                   | `'5'.padEnd(3, '0')` → `'500'`         |
| `repeat()`     | Repeats the string                              | `'ha'.repeat(3)` → `'hahaha'`          |

---

### 🔹 3. Object Methods

| Method             | Description                            |
|--------------------|----------------------------------------|
| `Object.keys()`    | Returns array of keys                  |
| `Object.values()`  | Returns array of values                |
| `Object.entries()` | Returns array of [key, value] pairs   |
| `Object.assign()`  | Copies values from one or more objects|
| `Object.freeze()`  | Prevents modification                 |
| `Object.seal()`    | Prevents adding/removing keys         |
| `hasOwnProperty()` | Checks if object has a property       |

---

### 🔹 4. Math and Number Methods

| Method           | Description                          | Example               |
|------------------|--------------------------------------|-----------------------|
| `parseInt()`     | Converts string to integer           | `parseInt('10')`      |
| `parseFloat()`   | Converts string to float             | `parseFloat('10.5')`  |
| `toFixed()`      | Returns fixed decimal points         | `(2.456).toFixed(1)`  |
| `Math.floor()`   | Rounds down                         | `Math.floor(2.9)`     |
| `Math.ceil()`    | Rounds up                           | `Math.ceil(2.1)`      |
| `Math.round()`   | Rounds to nearest whole number       | `Math.round(2.5)`     |
| `Math.abs()`     | Absolute value                      | `Math.abs(-5)`        |
| `Math.max()`     | Returns highest number               | `Math.max(1, 2, 5)`   |
| `Math.min()`     | Returns lowest number                | `Math.min(1, 2, 5)`   |
| `Math.random()`  | Random number between 0–1           | `Math.random()`       |
| `Math.pow()`     | Exponentiation                      | `Math.pow(2, 3)`      |
| `Math.sqrt()`    | Square root                         | `Math.sqrt(9)`        |

---

### 🔹 5. Date Methods

| Method             | Description                          | Example                    |
|--------------------|--------------------------------------|----------------------------|
| `new Date()`       | Creates current date/time            | `new Date()`               |
| `getFullYear()`    | Gets year                            | `date.getFullYear()`       |
| `getMonth()`       | Gets month (0–11)                    | `date.getMonth()`          |
| `getDate()`        | Gets day of month                    | `date.getDate()`           |
| `getDay()`         | Gets day of week (0–6)               | `date.getDay()`            |
| `getHours()`       | Gets hour                            | `date.getHours()`          |
| `getMinutes()`     | Gets minutes                         | `date.getMinutes()`        |
| `getSeconds()`     | Gets seconds                         | `date.getSeconds()`        |
| `toISOString()`    | Converts date to ISO string          | `date.toISOString()`       |
| `toLocaleString()` | Converts date to local string        | `date.toLocaleString()`    |

---

### 🧠 Tip
Use these methods in practice by building mini projects, solving coding challenges, or preparing for interviews. These are the most asked and most used methods in day-to-day frontend and JavaScript work.

**Happy Coding! 🚀**
