# ![JS](../images/js.png "I'm Popular") JavaScript 

## What is JavaScript?

* It is a dynamic type variable. It makes interactive web pages.
* In JavaScript everything is an Object.

### Two categories:
  * [Primitive](#Primitive) (Copy by Value)
      * String : Characters.
      * Number : Numeric Value.
      * Boolean : True or False.
      * Undefined : It is value and type also.
      * Null : Null value.
      * Symbol
  
  * [Non-primitive](#Non-primitive) (Cody by Reference)
      * Object : All JavaScript values except primitives are objects.
      * Array : List


---
## **Primitive**
---

Value       |   typeof
:---:       |   :---:
"Hello"     |   string
9           |   number
true/false  |   boolean
undefined   |   undefined
null        |   null object

---

`string :`
```JavaScript
var a ="Hello,";

var b = "world!";

c= a+b
console.log(c);
console.log(typeof c);
```
`Output :`

Hello,world!

string

___

`number :`
```JavaScript
var num1 =10;

var num2 = 12;

num = num1 + num2
console.log(num);
console.log(typeof num);
```
`Output:`

22

number

___

Examples :

```JavaScript
var num =10;
undefined
var num2 = "12";
undefined
num + num2
"1012"
```

```JavaScript
var num =10;
undefined
var num2 = Number"12";
undefined
num + num2
"22"
```

`boolean &&  and ||`

```JavaScript
if(-45 && 0 && 10 && 200){console.log("True")} else{console.log("False")}
False
undefined
if(-45 && 20 && 10 && 200){console.log("True")} else{console.log("False")}
True
```
```JavaScript
if(-45 || 0 || 10 || 200){console.log("True")} else{console.log("False")}
True
undefined
if(-45 || 20 || 10 || 200){console.log("True")} else{console.log("False")}
True
```

## **Non-primitive**
### `Array :` 

```JavaScript
var arr=[2];

console.log(arr.length);
```
`Output :`

1

```JavaScript
var arr=[2,3,7,null,[],{}];

console.log(arr);
console.log(arr.length);
```
`Output :`    
(6) [2, 3, 7, null, Array(0), {…}]    
6

>**Adding in array**
```JavaScript
var names = ["Sup","nin","chi"];

names[11] = "nu";

console.log(names.lenght)
console.log(names)
```
`Output :`

12    
['Sup','nin','chi',<8 empty items>,'nu']

>**Push in array** : It will add in last of the array.
```JavaScript
var names = ["Sup","nin","chi"];

names.push["nu","ali"];

console.log(names)
```
`Output :`
   
['Sup','nin','chi','nu','ali']

>**Pop in array** : It will remove from last of the array.
```JavaScript
var names = ["Sup","nin","chi","nik"];

names.pop();

console.log(names)
```
`Output :`
   
['Sup','nin','chi']

>**indexOf in array** : indexOf() method returns index of the object. 

```JavaScript
var names = ["Sup","nin","chi","nik"];

var index = names.indexOf("chi");
console.log(index)
```
`Output :`
   
2

>To avoid -1 return value if not found we can use <!== -1> condition.
```JavaScript
var names = ["Sup","nin","chi","nik"];

if(names.indexOf("chi") !== -1){
    console.log("Item found");
}else{
    console.log("Item is not present")
}
```
`Output :`
   
Item found

>We can also use includes to check in ES6.
```JavaScript
var names = ["Sup","nin","chi","nik"];

if(names.includes("chi")){
    console.log("Item found");
}else{
    console.log("Item is not present")
}
```
`Output :`
   
Item found

---

## **Lexical scope** 

First if variables in ES6, it will check first in lexical scope, then, parents lexical scope, then function scope, and lastly parents.    
>Lexical scope stays Within the { }. 

```JavaScript
let a= 4;
var b=30;

if(a) {
  let b=9;
  let a=9;
  console.log(a+b);
  b=a+b;
}

function hello(){
  if(a){
    b=20;
    console.log(a+b);
  }else{
    let b;
  }
  var b=5;
  console.log(b);
}

hello();
console.log(b);

```
```
> Ouput:
18
24
5
30
```
 
## **Global scope**
> Any var declared outside a function is Global.
> All object and function can access it.

## **Function scope**
> Function scope can be accessed only within the function, if var is not there it will call the nearest parent function.

---
##  **var let and const**

---
|**Keyword**       | **var**              |    **const**    |      **let**
---           | ---              |    ---    |      ---
Version           | ES5              |    ES6      |      ES6
Scoped         | Global           |    Block    |      Block
Variables      | can be updated as well as re-declared | can be updated but cannot re-declared | cannot be updated or re-declared
Initialization | undefined        | not initialized | not initialized
---



<!-- reference -->

