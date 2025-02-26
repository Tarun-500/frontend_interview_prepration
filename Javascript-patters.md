# JavaScript Hollow Square Pattern

This code generates a hollow square pattern using JavaScript.

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

### Explanation:
- The **```js** syntax highlights the JavaScript code properly.
- The **```** before and after output preserves the formatting.
- The **How to Run** section helps users execute the code easily.

Now, just commit this `.md` file to your GitHub repository, and users can copy and run the code directly from GitHub. 🚀



# JavaScript C  Pattern

## Code:

```js

function fun(){
    
let b = ""
for(let i=1; i <= 10; i++){
   for(let j=1; j <= 10; j++){
       if(i === 1 || i===10 ||  j ===1 || i ===5){  
       b+= "* "
       }else{
           
       }
   }
    
    b+= "\n"
}
return b
}

console.log(fun())

### output :
* * * * * * * * * * 
* 
* 
* 
* * * * * * * * * * 
* 
* 
* 
* 
* * * * * * * * * * 
