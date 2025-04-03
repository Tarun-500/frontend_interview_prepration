<details><summary> <h3> 001) Given an array <code> arr = [5, 7, 89, 45, 78, 2], </code> write a function to find and return the smallest number in the array. </h3>  </summary>
  
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
  <summary> <h3> 002) Given an array arr = [5, 7, 89, 45, 78, 2], write a function to find and return the largest number in the array. </h3> </summary>
</details>
