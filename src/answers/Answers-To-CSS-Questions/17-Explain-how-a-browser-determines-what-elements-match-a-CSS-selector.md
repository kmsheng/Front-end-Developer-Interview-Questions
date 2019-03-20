# Explain how a browser determines what elements match a CSS selector.

Browser reads css selector from right to left. For example selector `div > ul > li`, it will check `li` first, then `ul` and then `div`
For jQuery users, this approach might be seen counter-intuitive, this is because the browser is trying to apply many rules to many nodes.
Not like using one selector to find among many nodes.

Instead of solving which node should be matched, find out the ones which are not matched is faster. 

### References
 - https://stackoverflow.com/questions/5797014/why-do-browsers-match-css-selectors-from-right-to-left/5813672#5813672
