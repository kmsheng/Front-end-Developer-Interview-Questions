# Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
 - User types website's URL and hits the enter key.
 - Browser tries to find a DNS record from browser cache for corresponding IP of URL.
 - If it does not exist in browser cache, it makes a system call to find OS cache.
 - If it does not exist in OS cache, it searches through router cache.
 - If it does not exist in router cache, it checks the ISP cache.
 - If it does not exist in ISP cache, ISP's dns server initiate a DNS query to find the IP of server that hosts the URL.
 - Once browser gets the IP, it initates a TCP connection with the server through `TCP/IP three-way handshake`.
 - Browser sends an HTTP request to server.
 - The server handles the request and send back a response.
 - Browser outputs the content based on response.
 
 ### References
  - https://medium.com/@maneesha.wijesinghe1/what-happens-when-you-type-an-url-in-the-browser-and-press-enter-bb0aa2449c1a
