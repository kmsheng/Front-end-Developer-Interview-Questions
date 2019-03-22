# What's the difference between a variable that is: null, undefined or undeclared ?
 - JavaScript variable can be declared using `var`, `let`, `const`.
 - Assign a value to an undeclared variable will create a global variable.

## How would you go about checking for any of these states ?

```js
v1; // v1 is not declared, calling it will get ReferenceError
let v2;
const v3 = null;

console.log(typeof v2);    // "undefined"
console.log(typeof null);    // "object", beware of this
console.log(v3 === null);  // true
```
