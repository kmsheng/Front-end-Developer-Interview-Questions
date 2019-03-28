# Describe the difference between `<script>`, `<script async>` and `<script defer>`.

## Normal Execution
 - Start parsing HTML.
 - Pause HTML parsing when script starts fetching and executing.
 - Resume HTML parsing after script execution done.
 
```html
<html>
<head></head>
<body>
    <script src="script.js"></script>
</body>
</html>
```
## With `async` Attribute
 - Start parsing HTML.
 - If there're script tags with async attribute, script fetching and HTML parsing can process at the same time.
 - Pause HTML parsing when script executes.
 - Resume HTML parsing when script execution completes.

```html
<html>
<head></head>
<body>
    <script async src="script.js"></script>
</body>
</html>
```

## With `defer` Attribute
`defer` is similar to `async`, but execute script when HTML parsing completes.

```html
<html>
<head></head>
<body>
    <script defer src="script.js"></script>
</body>
</html>
```

### References
 - https://bitsofco.de/async-vs-defer/
 - https://flaviocopes.com/javascript-async-defer/
 
