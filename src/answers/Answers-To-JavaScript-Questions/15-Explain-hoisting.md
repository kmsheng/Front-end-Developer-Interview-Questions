# Explain "hoisting".
 - `hoisting` is a special behavior of how JavaScript interpreter processes variables and functions.
 - JavaScript engine stores declarations to `variable object` during compilation phase and then process them in execution phase.

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

<br>

Named functions have higher hoisting priority than variables.

```js
console.log(a);    // function() {}

function a() {
}
var a = 1;
```

<br>

Re-declaration might be a little weird this way

```js
var a = 1;
var a;
console.log(a);    // a is 1, not undefined
```

Above example can be treated as

```js
var a;
var a;
a = 1;
console.log(a);
```

Because variable declaration and assignment are processed separately in different phases.

### References
 - https://blog.techbridge.cc/2018/11/10/javascript-hoisting/
 - https://john-dugan.com/hoisting-in-javascript/
 - https://blog.crimx.com/2015/03/29/javascript-hoist-under-the-hood/
