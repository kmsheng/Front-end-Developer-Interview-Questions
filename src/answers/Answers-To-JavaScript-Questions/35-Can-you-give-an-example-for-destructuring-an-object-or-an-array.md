# Can you give an example for destructuring an object or an array ?

```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const newArr = [...arr1, ...arr2];    // 1, 2, 3, 4

const obj = { name: 'First Object' }
const newObj = {...obj};    // assign properties to new object instance
```

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax
