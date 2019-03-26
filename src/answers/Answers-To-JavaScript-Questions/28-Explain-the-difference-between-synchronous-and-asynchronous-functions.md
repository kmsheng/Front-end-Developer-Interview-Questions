# Explain the difference between synchronous and asynchronous functions.

`synchronous` function waits for each operation to complete, after that it only executes the next operation.
`asynchronous` function does not wait for each operation to complete, so the callbacks are not guaranteed to be in order.

```js
console.log('first');
console.log('second');

// The output should be:
// first
// second
// because console.log function is synchronous
```


```js
fetch('http://example.com/movies.json')
  .then(_ => console.log('first'));
  
fetch('https://jsonplaceholder.typicode.com/todos/1')
  .then(_ => console.log('second'));
  
// It's hard to tell which fetch will complete first
```

### References
 - https://rowanmanning.com/posts/javascript-for-beginners-async/
