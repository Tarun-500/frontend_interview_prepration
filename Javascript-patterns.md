# JavaScript Pattern Questions

## Javascript Square pattern
### Code:

```
function fun() {
  let b = "";
  for (let i = 1; i <= 10; i++) {
    for (let j = 1; j <= 10; j++) {
      if (i === 1 || i === 10 || j === 1  || j === 10 ) {  
        b += "* ";
      } else {
        b += "  "; // space for the "C" shape
      }
    }
    b += "\n";
  }
  return b;
}
console.log(fun());
```
 
### Output:
| * | * | * | * | * | * | * | * | * | * |
|---|---|---|---|---|---|---|---|---|---|
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * |   |   |   |   |   |   |   |   | * |
| * | * | * | * | * | * | * | * | * | * |






## Javascript C - pattern
### Code:
```
function fun() {
  let b = "";
  for (let i = 1; i <= 10; i++) {
    for (let j = 1; j <= 10; j++) {
      if (i === 1 || i === 10 || j === 1   ) {  
        b += "* ";
      } else {
        b += "  "; // space for the "C" shape
      }
    }
    b += "\n";
  }
  return b;
}
console.log(fun());
```

### Output :
* * * * * * * * * * 
| * | * | * | * | * | * | * | * | * | * |
|---|---|---|---|---|---|---|---|---|---|
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * |   |   |   |   |   |   |   |   |   |
| * | * | * | * | * | * | * | * | * | * |


 

