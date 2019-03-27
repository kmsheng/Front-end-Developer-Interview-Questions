# Can you give an example of a curry function and why this syntax offers an advantage ?

```js
function curry(func) {
  return (...args) => {
    if (args.length >= func.length) {
      return func(...args);
    }
    return curry(func.bind(null, ...args))
  };
}

function add(x, y, z) {
  return x + y + z;
}

const curriedAdd = curry(add);

console.log(add(1, 2, 3));

console.log(curriedAdd(1)(2)(3));
```

`curry` technique allows function to be composed easier.

```js
function compose(...fns) {
  return fns.reduce((f, g) => (...args) => f(g(...args)));
}
function toUpperCase(str) {
  return str.toUpperCase();
}
function addExclamationMark(str) {
  return `${str}!`;
}

const noisy = func => (...args) => {
  console.log(`Function: ${func.name}`);
  console.log(`Arguments: ${args}\n`)
  return func(...args);
};

const processStr = compose(noisy(toUpperCase), noisy(addExclamationMark));

console.log(processStr('hello'));

```

### References
 - https://medium.com/front-end-weekly/javascript-es6-curry-functions-with-practical-examples-6ba2ced003b1
 - https://blog.benestudio.co/currying-in-javascript-es6-540d2ad09400
