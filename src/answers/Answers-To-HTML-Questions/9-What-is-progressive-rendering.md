# What is progress rendering ?
`progress rendering` means to deliver the most meaningful content to users as soos as possible.

Here are some tips to speed up your first paint:
 - minify HTML
 - inline minified critical CSS into `<head></head>`
 - If custom font exists, preload it using `<link rel="preload" href="font.woff" as="font" crossorigin>`
 - lazyload images and videos
 - reduce blocking scripts, use `defer` or `async` attribute if possible
 
 
 ### References
  - https://developers.google.com/web/fundamentals/performance/critical-rendering-path/
  - https://developers.google.com/web/fundamentals/performance/lazy-loading-guidance/images-and-video/
  - https://hacks.mozilla.org/2017/09/building-the-dom-faster-speculative-parsing-async-defer-and-preload/
