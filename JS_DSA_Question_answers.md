<details><summary> <strong> 001) Given an array <code> arr = [5, 7, 89, 45, 78, 2], </code> write a function to find and return the smallest number in the array. </strong>  </summary>
  
  <small>
     
    arr = [5, 7, 89, 45, 78, 2, 8]
    function fun(arr){
    let b  =  Infinity
    for(let d of arr){
         if(d < b){
             b = d
         }
    }
    
    return b
     }
    console.log(fun(arr))
  </small>
</details>


<details>
  <summary> <strong> 002) Given an array arr = [5, 7, 89, 45, 78, 2], write a function to find and return the largest number in the array. </strong> </summary>
</details>

<details>
  <summary><strong>003)</strong> Given an array <code>arr = [5, 7, 89, 45, 78, 2]</code>, write a function to calculate and return the sum of all numbers in the array.</summary>

```javascript
let arr = [5, 7, 89, 45, 78, 2];

function sumArray(arr) {
    let sum = 0;
    for (let num of arr) {
        sum += num;
    }
    return sum;
}

console.log(sumArray(arr)); // Output: 226
```
</details>  

<details>
  <summary> <strong> 004) Remove Adjacent Duplicates in an Array (Single Pass) Input:  [1, 2, 2, 3, 3, 3, 4, 4, 5] Output: [1, 2, 3, 4, 5]  </strong> </summary>
</details>
