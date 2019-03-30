# Describe how you would create a simple slideshow page.
I would have the following HTML, a div wraps many images.

```html
<div class="slideshow">
  <img class="slide" src="url" alt="slide" />
  <img class="slide" src="url" alt="slide" />
  <img class="slide" src="url" alt="slide" />
</div>
```

And use `animation` with `animation-delay` to switch each slide.
```scss
$slides: 3;
$time-per-slide: 4;
$total-animation-time: $time-per-slide * $slides;

@keyframes switch {   
  25% {
    opacity: 1;
  }
  40% {
    opacity: 0;
  }
} 

.slideshow {
  position: relative;
}
.slide {
  position: absolute;
  animation: switch #{$total-animation-time}s infinite;
  opacity: 0;
}

@for $index from 1 to $slides + 1 {
  img:nth-child(#{$index}) {
    animation-delay: #{$total-animation-time - ($time-per-slide * $index)}s;
  }
}
```
