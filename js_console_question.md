### 1 ) Write a nested loop to print a 3x3 grid of numbers,
### 2 ) Use a for loop to reverse an array [1, 2, 3, 4]
### 3 ) Write a while loop that logs numbers from 1 to 100 divisible by 5.
### 4 ) Write a function to find the maximum of two numbers.
### 5 ) Create a function that takes a number and returns its factorial. using - loop and recursion
### 6 ) Write a function that accepts a string and returns its reverse.
### 7 ) Create a function to find the largest number in an array.
### 8 ) Write a function that converts a string to kebab—case
<details>
  <summary> <h3>  Why does .call() not work with the arrow function in this code? </h3>   </summary>
  <small>
    
```
const name = "John";
this.name = "Jane";
const printName = () => {
console.log(this.name);
}
printName.call({name: "Joe"});
  ```
 Arrow functions do not have their own this; they inherit it from their surrounding scope. Since printName is an arrow function, .call({ name: "Joe" }) does not change this, so it prints "Jane".
  </small>
 
</details>

<details>
  <summary> <h3>  Cut array length  </h3>   </summary>
  <small>
    
```
 const arr = [1, 345, 50, 20, 36, 7855, 59, 455, 5]
arr.length = 5
console.log('arr.length', arr)
  ``` 
  </small>
</details>


<details>
  <summary> <h3>  sum of array element -  </h3>   </summary>
  <small>
    
```
  const a = [1,2,3,4,5,6,7,8,9,10]
  const sum = a.reduce((a, b) => a + b ,0) // 0 is a initial value
  console.log('sum', sum)
  ``` 
  </small>
</details>

<details>
  <summary> <h3> remove duplicate values - </h3>   </summary>
  <small>
    
```
  const a = [1,1,1,2,2,2,3,4,5,6,6,7,8,9,9,10,10]
  const duplicate = [...new Set(a)]
  console.log('duplicate', duplicate)
  ``` 
  </small>
</details>




<script>

   let x=10;
 x = (x++, x) //output 11
 x = (x++, 5) //output 5  //its take 2nd or last value
  y = 50
   x = (x++, y) // output 50
  x = (x+=20) // output 30
  console.warn(x);

  // 6) Convert this string into an array -
  // let str = "Hello, My Self Tarun shah"
  // let arr = str.split(" ") // split in words
  // let arr = str.split("") // split in single character
  // let arr = [...str] // split in single character
  // console.log('arr', arr)

  // 7) Remove a from this string -
  //   let str = "Hello, My Self Tarun shah"
  //   str = str.replace("a", "") // remove only first a
  //   str = str.replace(/a/g, "") // remove all a
  //   console.log('str -', str)

  //   // 8) show only tarun from this string -
  //   let str = "Hello, My Self Tarun shah";
  //   str = str.substring(15, 21);
  //   console.log("str -", str);

  //   // 9) show only Tarun Shah from this string -
  //   let str = "Hello, My Self Tarun shah";
  //   str = str.split(" ");
  //   str = str.slice(3);
  //   str = str.join(" ");
  //   console.log("str -", str);

    // // 11) show only tarun from this string -
  // let str = "Hello, My Self Tarun shah";
  // str = str.split(" ");
  // str = str.filter((item) => item == "Tarun")
  // console.log('str', str)

  
  // //10) reverse this str -
  // let str = "Hello, My Self Tarun shah";
  // str = str.split('').reverse().join("")
  //     console.log('Str - ', str)  // output - hahs nuraT fleS yM ,olleH

  // // Reverse Using loop
  // let a = ""
  //   for (let i = str.length -1; i >= 0; i--) {
  //     a = a + str[i]
  //   }
  // console.log(a)


  //   //   12) remove extra spaces from this string -
  //   let str = "         Hello            ";
  //   str = str.trim();
  //   console.log("str", str);

  // 13) multiply by using array form
  // let arr = [1,2,3,4,5]
  // arr = Array.from(arr, item=> item*2)
  // console.log('arr', arr)

  // // 14) create arr using Array form
  // let arr = [1,2,3,4,5]
  // // arr = Array.from({length:5}, (item, index)=> index*2) // for sum
  // arr = Array.from({length:5}, (item, index)=> index*2 + 1) // for odd
  // console.log('arr', arr)

  // // 15)
  // const a ="string"
  // console.log(a()) // output a is not a function

  // // 16)
  // let a = false || {} || null
  // console.log('a', a)

  // // 17)
  // let a = null || false || ''
  // console.log('a', a)

  // 18)
  // console.log('promise.resolve("Tarun")', Promise.resolve("Tarun"))

  // 19)
  // let a= 20;
  // function foo(){
  //   console.log(a);
  //   let a = 10;
  // }
  // foo() //output if var then ans. - undefined and if let then ans. a can not assigned before initialize

  // // 20)
  // let name = "This is paragraph";
  // console.log(!typeof name == "object"); // output false
  // console.log(!typeof name == "string");// output false
  // console.log(typeof name === "string");// output true
  // console.log(!typeof name === false);// output true

  // // 21)
  // let a = "Tarun"
  // let b = 100 ;
  // console.log('a', isNaN(a)) //output true
  // console.log('b', isNaN(b)) // output false

  // // 22)
  // let a = {name: 'Tarun'}
  // Object.seal(a)  // seal will not add other key here can change only current key value
  // a.age = 20
  // a.name = 20
  // console.log('a', a)

  //23) remove first element
  // let a = [1,2,3,4,5]
  //   a.shift()
  // console.log('a', a)
  //// remove last element
  // a.pop()
  // console.log('a', a)


  // 24) check value odd or even
  // let a = 50
  // console.log('a%2 ==0', a%2 ==0)

  // //25)
  // let a = 50
  // setTimeout(() => {
  //   console.log(a)
  // }, 100);
  //  a = 100  //output 100 //reason because js memory stack run api timeout function in last

  //26)
  // var a =50
  // var A=100
  // console.log('A', A)  //output 100

  // //27)
  // let a =5
  // let b =4
  // console.log(--a === b) //output true

  //28)
  // let a =1
  // let b=1
  // let c =2
  // console.log(a===b === --c) //  false
  // console.log(a== b == --c) //  true

  //29)
  // console.log('3*3', 3*3)
  // console.log('3**3', 3**3)
  // // console.log('3***3', 3***3)

  //30)
  // console.log('[[[[[[]]]]]]', [[[[[[]]]]]])

  // //31)
  // var for = 50
  // console.log('for', for) //reserved keyword

  // 32) Reserved keyword in js -
  // abstract,arguments,await,boolean,break,byte,case,catch,char,class,const,continue,debugger,default,delete,do,double,else,enum,eval,export,extends,false,final,finally,float,for,function,goto,if,implements,import,in,instanceof,int,interface,let,long,native,new,null,package,private,protected,public,return,short,static,super,switch,synchronized,this,throw,throws,transient,true,try,typeof,var,void,volatile,while,with,yield

  // //33)
  // for (var a = 0; a < 5; a++) {
  //   setTimeout(() => console.log("a", a));
  // } //output 5,5,5,5.5
  // for (let a = 0; a < 5; a++) {
  //   setTimeout(() => console.log("a", a));
  // } //output 0,1,2,3,4

  // //34)
  // console.log('+true', +true) // 1
  // console.log('typeof +true', typeof +true) // number  //reason - + sing covert string to numeric

  // //35)
  // console.log('!("tarun")', !("tarun"))
  // console.log('typeof ("tarun")', typeof ("tarun"))

  // //36)
  // let data = "size" ;
  // const bird ={
  //   size: "small",
  // }
  // console.log(bird[data]);
  // console.log(bird["size"]);
  // console.log(bird.size);
  // console.log(bird.data);

  // //37)
  // let a = { name: "Tarun" };
  // let b;
  // // a = b;
  // b=a
  // b.name = "Shah";
  // console.log("a.name", a.name); // reason - in object when copy object their location will copy not a data

  // //38)
  // let a =50
  // let b =new Number(50)
  // console.log('a == b', a ==b)
  // console.log('a === b', a ===b)

  // //39)
  // function Person(){
  //   console.log("Tarun")
  // }
  // Person.name ="Shah"
  // Person();

  //40)
  // function foo(){
  //   // 'use strict'
  //   a ="Tarun"
  //   console.log(a)
  // }
  // foo();

  // // 41)
  // console.log(eval("10*10*10"))

  //   // 42)
  // let a = {1:"One"}
  // console.log(a.hasOwnProperty("1"))
  // console.log(a.hasOwnProperty(1))

  // //43)
  // for(let a =1; a<5; a++){
  //   if(a === 3)continue
  //   console.log('a', a)
  // }

  //   //44)
  // const a ={name:"Tarun"}
  // function foo(age){return(`${this.name} ${age}`)
  // }

  // console.log(foo.call(a,25))
  // console.log(foo.bind(a,25)) // bind function need call again();

  // //45)
  // function foo(){
  //   return (()=>0)()
  // }
  // console.log('typeof foo()', typeof foo())

  // //46)
  // console.log('typeof typeof 1', typeof typeof 1)

  // //47)
  // function foo(){
  //   return ()=>0
  // }
  // console.log(typeof foo()()) // double function it will in chaining so thats by run inside function and its number

  // //48)
  // const a =[1,2,3]
  // a[6] =7
  // console.log('a', a)

  // //49)
  // console.log('!!null', !!null)
  // console.log('!!', !!'')
  // console.log('!!1', !!1)

  // //50)
  // console.log([..."Tarun"])

  // //51)
  // const pro = new Promise((res, rej)=>{
  //   setTimeout(res, 500 , "First");
  // })

  // const fro = new Promise((res, rej)=>{
  //   setTimeout(res, 100 , "Second");
  // })
  // Promise.race([pro, fro]).then(res=>console.log(res))

  // // 52)

  // let a ={name:"Tarun"}
  // let b = [a]
  // a=null
  // console.log('a', a) // output  null
  // console.log('b', b)  // [{name:"Tarun"}]

  // // 53)
  // const a = { name: "Tarun", age: "25" };
  // for (let item in a) {
  //   console.log("item", item);
  // }   // this will print their keys

  // // 54)
  // let a = 5 + 5 + "5";
  // console.log(typeof a);  //output string
  // console.log(typeof 3 + 5 + "5"); //output number55
  // console.log(typeof (3 + 5 + + "5")); //output number

  // //55)
  // console.log('[] == []', [] == []) //output false //reason - memory location can not same of array

  // //   //56)
  //   (()=>{
  // let x = (y=10)
  //   })()
  //   console.log("x", typeof x)

  // (() => {
  //   let x = y = 10;
  // })();
  // console.log(typeof y); //output number // here y is var because hee did not write here assign property

  // // //57)
  // let x = 50;
  // (() => {
  //   var x = 100;
  // })();
  // console.log("x", x);

  // //58)
  // console.log(!true - true) //output -1
  // console.log( true + + "10") //output 11
</script>



<script>
  document.addEventListener("DOMContentLoaded", (event) => {
    document.body.style.backgroundColor = "black";
  });

  //   //_______   1). # Swapping without using a third variable

  // let a = 20;
  // let b = 50;

  //   a = a + b; // a = 20 + 50 = 70
  //   b = a - b; // b = 70 - 50 = 20
  //   a = a - b; //  a = 70 - 20 = 50

  //   console.log("After swapping:");
  //   console.log("a =", a); // Output: a = 50
  //   console.log("b =", b); // Output: b = 20

  // _____ or it can be done using distruing
  //  [a, b] = [b ,a]
  //  console.log("a =", a); // Output: a = 50
  // console.log("b =", b); // Output: b = 20

  //   //_______ 2).

  //   console.log(1 == "1"); // Output: true
  //   console.log(1 === "1"); // Output: false

  // // _______ 3).

  // var a = 5;
  // console.log(a++ + a++); //output 11

  // // _______ 4).
  // var a = 5;
  // console.log(a++); //output 5

  // // _______ 5).
  // function aa() {
  //   let a = 0;
  //   a++;
  //   console.log(a);
  // }
  // aa(); // output 1
  // aa(); // output 1
  // aa(); // output 1

  // //_______ 6).
  // function aa() {
  //   let a = 0;
  //   console.log(a);
  //   a++;
  // }
  // aa(); // output 0
  // aa(); // output 0
  // aa(); // output 0

  // //_______ 7).
  // let a = 0;
  // function aa() {
  //   console.log(a);
  //   a++;
  // }
  // aa(); // output 0
  // aa(); // output 1
  // aa(); // output 2

  // //_______ 08).
  // console.log(1 < 2 < 3 < 4 <script 5);
  // console.log(5 > 4 > 3 > 2);

  // //_______ 09).
  // // remove spaces and replace with hyphens and replace hyphens with space.
  // let name = "My name is - Tarun";
  // name = name.replace(/\s+/g, "-").replace(/-/g, " ");
  // console.log(name);

  //  //_______ 10).
  //   let name = "My name is - Tarun";
  // name = name.replace(/[\s-]+/g, '-');
  // console.log(name);

  //  //_______ 11).
  // var a = 20;
  // function foo() {
  //   console.log(a);
  //   var a = 10;
  // }
  // foo();

  //  //_______ 12).
  // let a = 1 + 5 + "3" + 7 + 9;
  // console.log("a", a);
  // let b = "4" + 4 + 6 + 0;
  // console.log("b", b);

  //  //_______ 13).

  // let a = [1,2,3]
  // let b = [4,5,6]
  // let c = [...a, ...b]
  // console.log('c', c)

  //   // ________ 14).
  //   let a = []
  // let b = []
  // console.log(a == b)// output false  //reason - when array compare that time their memory location compare and location can not be same
  // console.log(a === b) // output false

  // // ___________ 15).
  // let a = [];
  // let b = a;
  // console.log('a == b', a == b) // output true  // reason - here location is same thats by its true
  // console.log('a === b', a === b) // output true

  // // ________ 16).
  // let a= [50]
  // let b= [50]
  // console.log('a[0] == b[0]', a[0] == b[0]) //output true // reason - here compare element value its 20 = 20
  // console.log('a[0] === b[0]', a[0] === b[0]) // output true

  // // ______ 17).
  // console.log(typeof NaN) //output number

  // // ________ 18).
  // console.log('10 - - 10', 10 - - 10) //output 20

  // //_______ 19)
  // let a = {name: "Tarun"}
  // console.log('a', a) // output {name: "Tarun"}
  // console.log(delete a.name) //output true
  // console.log('a', a) // output {}

  // //__________ 20)
  //  let a = ["One", "Two", "Three"]
  //  let [z] = a
  //  console.log('[z]', [z]) // output One //
  //  console.log('[z]', [,z]) // output empty Two //

  //  _________ 21)

  // for (let i = 1; i <= 5; i++) {
  //   let c = "";
  //   for (let a = 1; a <= i; a++) {
  //     c += "*";
  //   }
  //   console.log('c', c)
  // }

  // for (let a = 1; a <= 10; a++) {
  //   let b = "";

  //   for (let d = 10 - a; d > 0; d--) {
  //     b += " ";
  //   }
  //   for (let c = 1; c <= a; c++) {
  //     b += "* ";
  //   }
  //   console.log("b", b.trimEnd());
  // }

  // ________ 22).
  // const num = 5;
  // var fact = 1;
  // var i = 1;

  // while (i <= num) {
  //   fact = fact * i;
  //   i++;
  //   console.log('i', i)
  // }

  // __________ 23).
  // let a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  // let arr = [];
  // for (let i = 0; i < a.length; i += 2) {
  //   arr.push(a.slice(i, i + 2));
  //   console.log("a", arr);
  // }
  // console.log('arr', arr)

  // // ________24).
  // // ___ FIND NTH HIGHEST NO. FORM THE ARRAY
  // const a = [1, 2, 5, 87, 65, 72, 45, 21, 21, 36, 55];

  // function nthHighest(n) {
  //   let set = [...new Set(a)];
  //   let sort = set.sort((a, b) => b - a);
  //   if (n > sort.length) {
  //     return "Give Input Between 1 TO 10";
  //   }
  //   let nthHigh = sort[n - 1];
  //   return nthHigh;
  // }
  // console.log("nthHighest()", nthHighest(5));

  // //______________25.) Find a largest string from this array

  //   let a  = ['Tarun', "Shah", "Jain"]

  //  console.log(a.reduce((a, b)=> {
  //      return b.length > a.length ? b : a;
  //  },""))

  // let a = ['Tarun', "Shah", "Jain"]

  // function findLongestString(arr) {
  //     let longest = "";
  //     for (let i = 0; i < arr.length; i++) {
  //         if (arr[i].length > longest.length) {
  //             longest = arr[i];
  //         }
  //     }
  //     return longest;
  // }

  // console.log(findLongestString(a)); // Output: "Tarun"

  // // ___________ 27.) make a pyramid of these numbers
  // const a = [
  //   1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
  // ];
  // function pyramid(n) {
  //   let ans = [];
  //   let start = 0
  //   for(let i = 1; start < n.length; i++) {
  //     let level = []
  //     for(let j=0; j < i && start < n.length; j++ ){
  //       level.push(n[start])
  //       start ++
  //     }
  //     ans.push(level)
  //   }
  //   return ans
  // }

  // console.log(pyramid(a));

  // // ___________ 28.) get all sum numbers
  // const a = [
  //1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20,
  // ];

  // function getSum(a) {
  //   let sum = [];
  //   for (let i = 0; i < a.length; i++) {
  //     if (i % 2) {
  //       sum.push(a[i]);
  //     }
  //   }
  //   return sum;
  // }
  // console.log(getSum(a));

  // // using filter

  // const getSum = a.filter((v) => v % 2 == 0 );

  // console.log(getSum);

  /////// _______29). find how many vowels in this array

  const a = "This is Tarun Jain";
  function countVowels(a) {
    const b = ["a", "e", "i", "o", "u"];
   let count = 0;
     a.toLowerCase()
      .split("")
     .forEach((arr) => {
         b.includes(arr) && count++;
       });
     return count;
  // }


  // //  using filter
   function countVowels(a) {
     const b = ["a", "e", "i", "o", "u"];
   return a.toLowerCase()
       .split("")
      .filter((ch) => 
         b.includes(ch) ).length;
   }

  console.log(countVowels(a));



let num  = 8 
let res = 4 + num++; 
console.log(res);  // output: 12
console.log(num);  // output: 9

  

const arr  =  ["My", " Name", " is", " Tarun"]
const  str =  arr[0] + arr[1] +  arr[2] + arr[3]
console.log(str) // output: My Name is Tarun



const a = 100;
 if(true){
  const a = 500;
 }
 console.log(a) // output: 100



let count = 1 
let list = ["T", "A", "R", "U", "N"]
console.log(list[count++]) // output: A
console.log(list[++count]) // output: R


let n = 1 
n = n++ + ++n + n++;
console.log(n)


let num  = [1,2,3,4]
num[num.length - 1]++
console.log(num)



 let name = "tarun"
 
 if(name == "tarun"){
     name == "jain"
 } 
 console.log(name)
</script>
