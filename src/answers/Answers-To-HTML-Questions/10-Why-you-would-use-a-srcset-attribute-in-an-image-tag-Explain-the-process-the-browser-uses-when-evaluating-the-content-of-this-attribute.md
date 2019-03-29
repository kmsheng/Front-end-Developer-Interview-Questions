# Why you would use a srcset attribute in an image tag ?
`srcset` helps you to serve different image sizes to different resolution which known as responsive images.

## Explain the process the browser uses when evaluating the content of this attribute.

```html
<img srcset="elva-fairy-320w.jpg,
             elva-fairy-480w.jpg 1.5x,
             elva-fairy-640w.jpg 2x"
     src="elva-fairy-640w.jpg" alt="Elva dressed as a fairy">
```

The browswer will only load the filename that matches the pixel density.

For example, iphone6 with `2x` density will load `elva-fairy-640w.jpg`

### References
 - https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images
 - https://bitsofco.de/the-srcset-and-sizes-attributes/
