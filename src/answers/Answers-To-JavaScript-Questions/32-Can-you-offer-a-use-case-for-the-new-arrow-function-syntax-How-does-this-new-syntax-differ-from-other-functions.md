# Can you offer a use case for the new arrow `=>` function syntax ? How does this new syntax differ from other functions ?

```js
const double = x => x * x;

const toObj = x => ({x});    // omits return keyword

const funcCreator = x => y => y;
```

- arrow function can omit the argument parentheses `()` when the argument is less than 2
- arrow function can skip return and function body block braces `{}` to make function cleaner
- high order function is possible to be written in one liner style.

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions
