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
