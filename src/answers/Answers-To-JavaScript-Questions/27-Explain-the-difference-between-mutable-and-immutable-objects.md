# Explain the difference between mutable and immutable objects.
- `mutable` objects can be changed after they're created.
- `immutable` objects create / return new object for every modification.

## What is an example of an immutable object in JavaScript ?
 - `Array.prototype.slice` is immutable, because it returns new copy of array every time.
 - [Immutable.js](https://github.com/immutable-js/immutable-js)

## What are the pros and cons of immutability ?
Pros
 - programs that are written with immutability are easier to refactor and easier to maintain.
 - Less side effect.
 
Cons
 - Sometimes writing immutability code can be complicated and tricky with pure JavaScript.
 - It needs dependency to make it right.
 - It's less performant than mutable approach.

## How can you achieve immutability in your own code ?
Use `Object.assign`, `spread operator` to achieve it.

### References
 - https://reactkungfu.com/2015/08/pros-and-cons-of-using-immutability-with-react-js/
