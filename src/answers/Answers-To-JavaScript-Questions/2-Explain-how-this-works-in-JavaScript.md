# Explain how `this` works in JavaScript.
`this` is the execution context of a function.

Example of `this` default behavior
```js
function getThis() {
  return this;
}
getThis() === window;    // true in browser
getThis() === global;    // true in Node.js, will be undefined in strict mode
```

Example of using `this` with `new` keyword
```js
function People(name) {
  this.name = name || 'unknown';
}
People.prototype.speak = function() {
  console.log('Hello, my name is ' + this.name);
};

var p = new People('Alice');
p.speak();
```

## Can you give an example of one of the ways that working with this has changed in ES6 ?
 - arrow function binds `this` automatically
 
 ```js
function Counter() {
  this.count = 0;

  // es5 - using bind this
  setTimeout(function() {
    console.log('count is ', this.count);
  }.bind(this), 0);
}

new Counter();
 ```
 
  ```js
function Counter() {
  this.count = 0;

  // es6 - using arrow function
  setTimeout(() => {
    console.log('count is ', this.count);
  }.bind(this), 0);
}

new Counter();
 ```
 
### References
 - https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Operators/this
 - http://2ality.com/2017/12/alternate-this.html
