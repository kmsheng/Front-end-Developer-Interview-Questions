# Explain `Function.prototype.bind`
`Function.prototype.bind` allows you to bind execution context and arguments to a function,

so a function can hold certain arguments first and then execute later.

```js
function add(first, second) {
  return first + second;
}

const addOne = add.bind(null, 1);
const addTwo = add.bind(null, 2);

console.log(addOne(1));    // 2
console.log(addTwo(1));    // 3
```
