## 1. Remove a Given Character from a String?
### Input:
  <small> My name is tarun jain </small>
```
const  arr = "My name is tarun jain"
function fun(arr, d){ 
    let word = arr.split(' ')
    let b = ""
    
     for(let i=0; i < word.length; i++){
        
       if(word[i] !== d){
            b += word[i]  + ' '
       } 
     }
    return b
}

console.log(fun(arr, "tarun"))
```

### Output :
 <small> My name is jain </small>

 ## 2. Reserve the given string :
### Input:

```
const arr = "Hello World";
function fun(arr) {
    let ans = "";
    for (let i = arr.length - 1; i >= 0; i--) {
        ans += arr[i]; // Appending characters one by one
    }
    return ans;
}
console.log(fun(arr)); // Output: "dlroW olleH"
 ``` 
```
const arr = "Hello World";
function reverseString(str) {
    return str.split("").reverse().join("");
}
console.log(reverseString("Hello World"));  
 ```
### Output :
 <small> dlroW olleH </small>

 ## 3. SUm of the given number :
 
```
const a  = 12345

function fun(a){

    let ans  =  0
 
    while(a > 0){
        ans  += a%10 
        a = Math.floor(a/10)
    }
    
    return ans
}

console.log(fun(a)) 
```


