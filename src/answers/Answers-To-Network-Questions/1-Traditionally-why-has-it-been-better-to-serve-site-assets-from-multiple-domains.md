# Traditionally, why has it been better to serve site assets from multiple domains ?
 - `parallelization`, rather than sending and getting data from one server, doing it with multiple servers will be faster.
 - `reduce header overhead`, the header of primary domain is usally large, each request with the same server will make the total transmitted data even larger.

### References
 - https://travishorn.com/why-it-is-better-to-serve-site-assets-from-multiple-domains-972a2bf69d71
