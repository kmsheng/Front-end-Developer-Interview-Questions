# What are the pros and cons of extending built-in JavaScript objects ?

For example, add a remove function to Array.prototype
```js
Array.prototype.remove = function(member) {
  var index = this.indexOf(member);
  if (index > -1) {
    this.splice(index, 1);
  }
  return this;
};

['a', 'b', 'c'].remove('c');
```
It's pretty easy to use this remove function without the import statement,

but if future browser versions implement the function, your code will override the browser's native function.

### References
 - https://javascriptweblog.wordpress.com/2011/12/05/extending-javascript-natives/
