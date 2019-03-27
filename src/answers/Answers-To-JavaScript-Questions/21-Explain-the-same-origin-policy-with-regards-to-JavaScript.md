# Explain the same-origin policy with regards to JavaScript.

- `same-origin` is a policy to restrict script or document being loaded by one origin.
- same-origin requires protocol, host and port must be the same, [except for IE](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy#Exceptions_in_Internet_Explorer).
- Cross domain writes are typecally allowed, so use a CSRF token to check whether a request is valid.
- Cross domain resource sharing can be enabled by configuring the server headers.


### References
 - https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy
 - https://lucybain.com/blog/2014/same-origin-policy/
