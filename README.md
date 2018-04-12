# ES2017-Tips

## Table of contents
1. [Let & Const](#1)
2. [Arrow Functions](#2)
3. [Export & Import](#3)
4. [Classes](#4)
5. [Spread & Rest Operator](#5)

## Let & Const <a name="1"/>
##### VAR
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var can still be used but its not recommended.</p>

##### LET
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variables declared using let are mutable, you can change the value at any point </p>

##### CONST
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variables declared using let are immutable, you cannot change the value at any point and it will throw a TypeError. </p>

---

## Arrow Functions <a name="2"/>
##### Older functions used to be like
```javascript
function functionName() {
  ...
}
```
##### Newer Arrow Functions FTW!
```javascript
const functionName = () => {
  ...
}
```
<p>Now we don't have to worry about the <i>this</i> keyword. As the function has the <i>this</i> scope always applied.</p>

We don't have to speicfy the attributes within () when there is only one attribute to be passed to the function, we can just write name and it would work like in the example below! Also this will work only when one attribute needs to be passed in, not when there are multiple attributes or no attributes.
```javascript
const namePrinter = name => {
  console.log(name);
}
namePrinter('Niranjan');
```
Try out in JSBIN --> https://jsbin.com/vatatuq/1/edit?js,console

If we are returning a value with a single attribute being passed to the function, we don't need the return keyword!
```javascript
const multiplierOf2 = number => number * 2;
console.log(multiplierOf2(3));
```
Try out in JSBIN --> https://jsbin.com/jalexig/3/edit?js,console

---
## Export & Import <a name="3"/>
![Image1](https://github.com/nchandar/ES2017-Tips/blob/master/exports1.jpeg)

Some more tips using exports and imports!
![Image2](https://github.com/nchandar/ES2017-Tips/blob/master/exports2.jpeg)

---
## Classes <a name="4"/>
##### Classes are essentially blue-prints for objects (eg : using one blue print we can create multiple houses.)
```javascript
class People {
    let name = 'max';  // PROPERTY --> variables in a class
    call = () => {...}  // METHOD --> functions attached to class
}
```

```javascript
class firstName {
  constructor() {
      this.fname = 'Niranjan';
  }
  
  printFName() {
      console.log("My First Name is : " + this.fname);
  }
}

class lastName extends firstName{
    constructor() {
      super(); // We need this super keyword when trying to access a extended classes variable.
      this.lname = "Chandarraj";
      // this.fname = "Ninja"; //This will override the fname from th eextended function.
    }
  
    printLastName() {
      console.log(this.lname);
      console.log(this.fname);
    }
  
    superMethod() {
      // Super can we used to call method from the extended class. 
      super.printFName();
    }
}

const name = new lastName();
name.printLastName();
name.superMethod();
```
Link to JSBIN --> https://jsbin.com/wevasov/edit?js,console

---

## Spread & Rest Operator <a name="5"/>
##### Both the spread and the rest operator are indicated by these 3 dots ...
##### Spread Operator --> It is used to spilt up all the elements in an array or all the properties in an object.
```javascript
//Splitting up all the elements in an array.
const num = [1, 2, 3, 4];
const newNum = [...num, 1000];

console.log(newNum);  //Ans is ==> [1, 2, 3, 4, 1000]
```
Link to JSBIN -->  https://jsbin.com/kubujuy/1/edit?js,console

```javascript
//Splitting up all the properties in an object.
const obj = {
  name : 'Niranjan',
  Phone : '12345678'
}

const newObj = {
  ...obj,
  address : 'xyz'
}

console.log(newObj); 
//The result is 
//{
//   address: "xyz",
//   name: "Niranjan",
//   Phone: "12345678"
// }
```
Link to JSBIN --> https://jsbin.com/wucubef/1/edit?js,console

##### Rest Operator --> It is used to combine all the arguments/parameters passed into a function into an array. 
```javascript
const newFunc = (...args) => {
  console.log(args);
}

newFunc(1, 2, 3, 4); //output --> [1, 2, 3, 4]

```
Link to JSBIN --> https://jsbin.com/kosaxub/2/edit?js,console

---
