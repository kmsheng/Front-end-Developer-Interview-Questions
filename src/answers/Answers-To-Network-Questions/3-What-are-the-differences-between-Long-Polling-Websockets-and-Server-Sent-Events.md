# What are the differences between Long-Polling, Websockets and Server-Sent Events ?

## Server-Sent Events
 - One-way communication ( server pushes to client )
 - Does not work on IE series.
 
## Long-Polling
 - Resource wasting, server needs to establish long connection
 - One-way communication ( client pulls from server )
 
## Websockets
 - Two-ways communication ( client to server and server to client )

### References
 - https://codeburst.io/polling-vs-sse-vs-websocket-how-to-choose-the-right-one-1859e4e13bd9
 - https://stackoverflow.com/questions/5195452/websockets-vs-server-sent-events-eventsource
