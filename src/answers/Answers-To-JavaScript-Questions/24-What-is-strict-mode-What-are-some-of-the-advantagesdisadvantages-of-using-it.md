# What is strict mode ? What are some of the advantages/disadvantages of using it ?

Advantages of strict mode are
 - Throw some JavaScript errors that were silent.
 - Fix mistakes that is difficult to JavaScript Engine, sometimes JavaScript runs faster in strict mode.
 - Prohibits some syntax that is likely to be defined in future version of ECMAScript.
 
 Disadvantages are
  - `IE 6-9` and some old browsers does not support it.
  - Some old JavaScript libraries might not support it.
 
 ```js
 'use strict';    // strict mode for entire script
 
 function test() {
   'use strict';    // strict mode for function block
 }
 ```
 
 Note that babel will add `use strict` for you by default.
 
 ### References
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode
