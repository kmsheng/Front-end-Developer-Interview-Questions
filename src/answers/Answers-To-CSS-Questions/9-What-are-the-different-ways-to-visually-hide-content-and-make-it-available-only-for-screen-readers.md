# What are the different ways to visually hide content (and make it available only for screen readers) ?
Add a `sr-only` class to hide things visually and screen readers are still able to read the tags with `sr-only` class

```css
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0
}
```

References:
 - https://getbootstrap.com/docs/4.3/getting-started/accessibility/#visually-hidden-content
