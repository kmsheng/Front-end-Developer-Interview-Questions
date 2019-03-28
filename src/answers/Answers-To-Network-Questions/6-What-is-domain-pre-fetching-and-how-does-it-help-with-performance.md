# What is domain pre-fetching and how does it help with performance ?
Domain pre-fetching is a technique that allows browser to do dns lookup on certain domains before actually entering a page, thus makes users feel faster when they navigate to the page.

There are two ways to do dns prefetch:
 - Render `X-DNS-Prefetch-Control` by header
 - Set `<link ref="dns-prefetch" href="url" />` in html
 
 ### References
  - https://www.keycdn.com/support/prefetching
  - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-DNS-Prefetch-Control
