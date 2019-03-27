# Explain the differences on the usage of foo between function foo() {} and var foo = function() {}

`function foo() {}` can be used before declration, for example.

```js
foo();    // It's ok to call foo because of function hoisting.

function foo() {
}
```

```js
foo();    // This will throw error because function implementation is not hoisted.

var foo = function() {};
```
