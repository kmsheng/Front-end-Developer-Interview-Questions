# What is the difference between == and === ?
`===` will do the same thing as `==` but without type conversion, generally it's recommended to use strict equality comparison `===`.

```js
console.log(1 == '1');    // true
console.log(1 === '1');    // false, because types are different

// be careful with these
console.log(+0 === -0);    // true
console.log(NaN === NaN);    // false
```

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness
