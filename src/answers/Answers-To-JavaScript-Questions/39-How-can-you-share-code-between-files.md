# How can you share code between files ?
- Use `import` statement with build tool like `webpack` to pack files together.
- Or consider using ES6 modules in Chrome

```html
<script type="module">
  import doSomething from './doSomething.js';
  doSomething();
</script>

// doSomething.js
export default function doSomething() {
  console.info('do something !!');
}
```

### References
 - https://medium.com/dev-channel/es6-modules-in-chrome-canary-m60-ba588dfb8ab7
