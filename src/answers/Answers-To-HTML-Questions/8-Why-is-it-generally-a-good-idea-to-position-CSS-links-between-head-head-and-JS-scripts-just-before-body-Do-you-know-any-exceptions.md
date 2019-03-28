# Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
 - The reason to put `<link>` between `<head></head>` is to prevent flash of unstyled content.
 - Script tag can block HTML rendering, so put it before `</body>` to make sure that HTML is rendered properly.
 - Script `async` and `defer` attributes are both able to render HTML faster.

### References
 - https://neal.codes/blog/front-end-interview-questions-html/
