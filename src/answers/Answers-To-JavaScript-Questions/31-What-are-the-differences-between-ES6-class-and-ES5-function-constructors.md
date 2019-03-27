# What are the differences between ES6 class and ES5 function constructors ?
Using ES6 class avoids manually setting the prototype and `instanceof` checking.

```js
function People() {
  if (! (this instanceof People)) {
    return new People();
  }
}
```

### References
 - https://medium.com/javascript-scene/javascript-factory-functions-vs-constructor-functions-vs-classes-2f22ceddf33e
