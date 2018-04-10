# ES2017-Tips

## LET & CONST
##### VAR
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; var can still be used but its not recommended.</p>

##### LET
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variables declared using let are mutable, you can change the value at any point </p>

##### CONST
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variables declared using let are immutable, you cannot change the value at any point and it will throw a TypeError. </p>

---

## Arrow Functions
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
