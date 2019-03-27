# What is the definition of a higher-order function ?
`higher-order function` is a function that takes function as argument or return a function.

```js
function greaterThan(n) {
  return m => m > n;
}
const greaterThanTen = greaterThan(10);
console.log(greaterThanTen(11));    // true
```

### References
 - https://eloquentjavascript.net/05_higher_order.html
