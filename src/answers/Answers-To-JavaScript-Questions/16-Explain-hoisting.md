# Explain "hoisting".
`hoisting` is a special behavior of how JavaScript interpreter processes variables and functions.
JavaScript engine will register declarations to `variable object` during compilation phase.

<br>

In JavaScript, accessing an undefined variable will get a `ReferenceError`.

```js
console.log(a);    // ReferenceError: a is not defined.
```
<br>
Accessing variables which are declared later will not raise an error,

because declarations with `var` will be hoisted to the top of containing scope.
( Declarations were already parsed and stored in `variable object` )

```js
console.log(a);    // undefined
console.log(func);    // undefined

var a = 1;

var func = function() {
};
```
<br>
Named functions will be hoisted with their "implementation details".

```js
console.log(add.toString());    // function add(a, b) {
                                //   return a + b;
                                // }

function add(a, b) {
  return a + b;
}
```

### References
 - https://blog.techbridge.cc/2018/11/10/javascript-hoisting/
 - https://john-dugan.com/hoisting-in-javascript/
