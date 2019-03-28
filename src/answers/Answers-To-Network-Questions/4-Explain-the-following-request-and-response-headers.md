# Explain the following request and response headers

## Diff. between Expires, Date, Age and If-Modified-...
 - `Expires` response header indicates the expiration date.
 - `Date` response header is the date for which the message has been originated.
 - `Age` response header indicates the duration of a request in a proxy. Usually it's the proxy's current date minus the date from `Date` header.
 - `If-Modified-Since` request header makes the request conditional. If the data's modification date is laster than the date of `If-Modified-Since`, then respond the resource with status `200`, otherwise `304` without any body.

## Do Not Track
 - a.k.a `DNT` header that represents a user's tracking preference.

## Cache-Control

## Transfer-Encoding

## ETag

## X-Frame-Options

### References
 - https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
