# What is CSS selector specificity and how does it work ?
Specificity is a weight that decides how your CSS declaration overrides another.

 - `!important` - 1-0-0-0-0
 - Inline style - 1-0-0-0
 - Number of ID selector - x-0-0
 - Number of classes, attributes and pseudo-classes - 0-y-0
 - Number of elements and pesudo-elements - 0-0-z
 
```css
.meat {
  width: 100px;
  height: 20px;
}
.burger .meat {
  background-color: brown;
}
.burger .bun .meat {
  background-color: blue;
}
```
```html
<div class="burger">
  <div class="bun">
    <div class="meat">
    </div>
  </div>
</div>
```

Consider the CSS and HTML above, the background-color of meat will be blue.

Because declaration `.burger .bun .meat (0-3-0)` overrides `.burger .bun (0-2-0)`

[demo](https://codepen.io/kmsheng/pen/qvKjxg/)
 
### References:
  - https://www.smashingmagazine.com/2007/07/css-specificity-things-you-should-know/
  - http://cssspecificity.com/
  - https://specifishity.com/
  - https://specificity.keegan.st
