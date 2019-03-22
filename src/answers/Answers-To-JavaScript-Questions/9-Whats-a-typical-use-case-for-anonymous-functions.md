# What's a typical use case for anonymous functions ?

For creating an isolated scope.
```js
let test = 'test';

(function() {
  // create local variable inside the anonymous function
  let test = 'blah';
  console.log('inner', test);    // blah
})();

console.log('outer', test);    // test
```

Or a simple map callback function.
```js
arr.map(function(x) {
  return x * x;
});

// es6 way
arr.map(x => x * x);
```
