# Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
By calculating the box size.

```css
div {
  width: 50px;
  padding: 10px;
  border: 1px solid #000;
}
```
```html
<div></div>
```

For default box-sizing `content-box`, the width of div should be `72px` ( 50px + 20px padding + 2px border )

If it's `border-box`, the width should be `50px`
