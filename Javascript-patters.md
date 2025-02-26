# JavaScript Hollow Square Pattern

## Code:

```js
function fun() {
  let b = "";
  for (let i = 1; i <= 10; i++) {
    for (let j = 1; j <= 10; j++) {
      if (i === 1 || i === 10 || j === 1 || j === 10) {  
        b += "* ";
      } else {
        b += "  "; // Empty space for hollow part
      }
    }
    b += "\n";
  }
  return b;
}

console.log(fun());
```js
## Output:
 
* * * * * * * * * * 
*                 * 
*                 * 
*                 * 
*                 * 
*                 * 
*                 * 
*                 * 
*                 * 
* * * * * * * * * * 
