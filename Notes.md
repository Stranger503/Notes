# Web Server From Scratch(Ruslans Blog)

1. First TCP Connection must be established between __Client - Server__.

# How ?

* Through __Sockets__ we can establish TCP connection.
* Ex: In our practice we use python to esablish a webserver using sockets library. and Instead of browser we listened to that port using __Telnet__.
* Now a TCP Connection is established. First Python Script(Server) then Telent(Client). The Python script have the __Responses__ for __Requests__.
* Now we can __Sent__ and __Recieve__ (HTTP Request and Responses).

## Note

* The basic model of how a Web server works. To sum it up: The Web server creates a listening socket and starts accepting new connections in a loop. The client initiates a TCP connection and, after successfully establishing it, the client sends an HTTP request to the server and the server responds with an HTTP response that gets displayed to the user. To establish a TCP connection both clients and serves use sockets.
