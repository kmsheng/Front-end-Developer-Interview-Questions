# What are the benefits of using spread syntax and how is it different from rest syntax ?

```js
const oldObj = {first: 1, second: 2};

const obj = {...oldObj};

// spread syntax is shorter than using Object.assign
// const obj = Object.assign({}, oldObj);
```

```js
function(firstArg, ...rest) {
}

const obj = {
  first: 'first',
  second: 'second',
  third: 'third'
};

const {first, ...rest} = obj;
console.log(rest);    // {second, third}
```

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters
