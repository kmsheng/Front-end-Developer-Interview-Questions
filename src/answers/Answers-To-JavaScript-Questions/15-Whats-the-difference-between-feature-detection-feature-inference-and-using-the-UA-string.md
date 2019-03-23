# What's the difference between feature detection, feature inference, and using the UA string ?

- `Feature detection` is a block of code based on certain feature, if that feature does not exist in some browsers, it will degrade gracefully. Once the feature is available, the related block of code will be run.
```js
if (window.requestAnimationFrame) {
  // then do some animations
}
```

- `Feature inference` is when you have a feature and you assume this browser is modern enough to have other features also. This is typically bad.
```js
if (window.localStorage) {
  // localStorage exists, so I assume sessionStorage is also available, too ?
  let data = sessionStorage.getItem('key');
}
```

`UA string` is a string that browsers send and can be accessed via `navigator.userAgent` Do not use this to detect feature.
```js
if (navigator.userAgent.indexOf("MSIE 7") > -1) {
    // do something
}
```
