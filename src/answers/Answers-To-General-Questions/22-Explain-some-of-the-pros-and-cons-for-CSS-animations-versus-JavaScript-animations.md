# Explain some of the pros and cons for CSS animations versus JavaScript animations.

## CSS animations
PROS
 - Handled on compositor thread, main thread ( styling, layout, painting, and JavaScript ) will not be interrupted.
 - Provides many timing functions by default.
 - Run on GPU, frame rates are much higher than JavaScript animations.
 - Able to animate without reflows and repaints.

 CONS
  - Unable to control significantly.
  - Need to be careful with the properties that you are going to animate. In other words, to avoid layout triggering possibly.
  
  
  ## JavaScript animations
  PROS
   - Able to control animation significantly.
  
  CONS
   - Wrose frame rates.
   - More complicated than writing CSS animations.
   
   
   ### References
    - https://developers.google.com/web/fundamentals/design-and-ux/animations/css-vs-javascript
    - https://developers.google.com/web/fundamentals/design-and-ux/animations/animations-and-performance#css-vs-javascript-performance
