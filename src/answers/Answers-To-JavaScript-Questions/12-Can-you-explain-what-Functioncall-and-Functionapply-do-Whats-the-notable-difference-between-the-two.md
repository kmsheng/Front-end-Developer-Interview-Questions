# Can you explain what `Function.call` and `Function.apply` do ? What's the notable difference between the two ?
`Function.call` and `Function.apply` can call a function and also specify its execution context ( `this` ).
The notable differnece is `Function.apply` takes second argument as an array, the other does not.

```js
Math.min.apply(null, [3, 1, 2]);
Math.min.call(null, 3, 1, 2);
```
