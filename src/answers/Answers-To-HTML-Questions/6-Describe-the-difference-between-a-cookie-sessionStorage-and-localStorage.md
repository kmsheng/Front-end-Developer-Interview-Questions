# Describe the difference between a cookie, sessionStorage and localStorage.

| Name | Life Cycle | Max Size | Compatibility |
| --- | --- | --- | --- |
| cookie | Depends on the expiration time set on cookie | Usually limited to 4096 bytes | All browsers support |
| sessionStorage | Will be cleared after tab closing | [2 ~ 10MB, depends on browsers](https://www.html5rocks.com/en/tutorials/offline/quota-research/#toc-how_to_handle_going_over_quota) | [IE6, IE7 and Opera Mini does not support](https://caniuse.com/#search=sessionStorage) |
| localStorage | Never expire | [2 ~ 10MB, depends on browsers](https://www.html5rocks.com/en/tutorials/offline/quota-research/#toc-how_to_handle_going_over_quota) | [IE6, IE7 and Opera Mini does not support](https://caniuse.com/#search=localStorage) |

### References
 - https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage
 - https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
 - https://www.html5rocks.com/en/tutorials/offline/quota-research/#toc-how_to_handle_going_over_quota
