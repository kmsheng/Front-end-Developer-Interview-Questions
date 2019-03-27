---
title: Coding Questions
layout: layouts/page.njk
permalink: /questions/coding-questions/index.html
---

* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```

```js
function duplicate(arr) {
  return arr.concat(arr);
}
```

* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`

```js
for (let i = 1; i <= 100; i++) {
  const isThreeMultiple = (i % 3) === 0;
  const isFiveMultiple = (i % 5) === 0;

  if (isThreeMultiple && isFiveMultiple) {
    console.log('fizzbuzz');
  }
  else if (isThreeMultiple) {
    console.log('fizz');
  }
  else if (isFiveMultiple) {
    console.log('buzz');
  }
}
```

Question: What is the value of `foo`?
```javascript
var foo = 10 + '20';
```
string `'1020'`, because the `+` sign will convert 10 to string.

Question: What will be the output of the code below?
```javascript
console.log(0.1 + 0.2 == 0.3);
```
false, because 0.1 + 0.2 will be 0.30000000000000004 due to the float precision problem of JavaScript.

Question: How would you make this work?
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

```
function curry(func) {
  return (...args) => {
    if (args.length >= func.length) {
      return func(...args);
    }
    return curry(func.bind(null, ...args));
  };
}
function addNumbers(a, b) {
  return a + b;
}
const add = curry(addNumbers);
```

Question: What value is returned from the following statement?
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
`"goh angasal a m'i"`

Question: What is the value of `window.foo`?
```javascript
( window.foo || ( window.foo = "bar" ) );
```

`"bar"`

Question: What is the outcome of the two alerts below?
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

alert with "Hello World" and get ReferenceError: bar is not defined


Question: What is the value of `foo.length`?
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

`2`

Question: What is the value of `foo.x`?
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

undefined, because JavaScript engine will evaluate all the left hand side expression before right hand expression.
The process of evaluating `foo.x = foo = {n: 2};`: 
- Evaluate left hand expression `({n: 1}).x = (foo = {n: 2})`
- Evaluate right hand expression, variable `foo` is assigned with `{n: 2}`
- Evaluate right hand expression, `({n: 1}).x` is assigned with `{n: 2}`
- Since variable `foo` has no property x, therefore the result of `foo.x` is undefined

Reference: http://es5.github.io/#x11.13.1

Question: What does the following code print?
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
Promise.resolve().then(function() {
  console.log('three');
})
console.log('four');
```

one, four, three, two
Note: call stack -> micro task queue ( promise ) -> task queue ( setTimeout )
Reference: https://github.com/dwqs/blog/issues/61

Question: What is the difference between these four promises?
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```

```javascript
doSomething().then(function () {
  return doSomethingElse();  // here's a return
});    // so it can chain with next function

doSomething().then(function () {
  doSomethingElse();  // no return
});    // cannot chain with next function

doSomething().then(doSomethingElse());  // doSomethingElse should return a function for then to call

doSomething().then(doSomethingElse);  // doSomethingElse itself should be a function
```
