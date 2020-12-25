# Read: Class 13 - Message Queues

## Review, Research, and Discussion

1. What does it mean that web sockets are bidirectional? Why is this useful?
2. Does socket.io use HTTP? Why? Yes, because it has more than one functionality - it's not just for web sockets. [src](https://stackoverflow.com/questions/37836130/socket-io-why-does-it-need-an-http-server)
3. What happens when a client emits an event? the server listens, assumign the client is using a channel that emits just to the server.
4. What happens when a server emits an event? all of the clients listen, unless the server is talking specifically to one client only.
5. What happens if a client “misses” an event? client won't acknowledge receiving the event, so server can know to resend it at some point.
6. How can we mitigate this? the server places it in a queue and when the client returns it can get all its missed messages.

## Vocabulary Terms

* Socket - an endpoint of 2-way communication link between two programs. Bound to a port number so that TCP layer can identify where to send the packets. [src](https://docs.oracle.com/javase/tutorial/networking/sockets/definition.html#:~:text=Definition%3A,address%20and%20a%20port%20number.)
* Web Socket - WebSocket is a communications protocol for a persistent, bi-directional, full duplex TCP connection from a user's web browser to a server. [src](https://whatis.techtarget.com/definition/WebSocket#:~:text=WebSocket%20is%20a%20communications%20protocol,web%20browser%20to%20a%20server.&text=The%20communication%20can%20be%20initiated,users%20to%20request%20new%20data.)
* Socket.io - a library for opening real time communication between server and clients. It is bi-directional.
* Client - a consumer of services provided by a server
* Server - computer software that provides services or informstion to clients.
* OSI Model: Open Systems Interconnection model with 7 layers.  Has strict boundaries. [src](https://www.geeksforgeeks.org/tcp-ip-model/)
* TCP Model - a more precise version of OSI with only 4 layers [src](https://www.geeksforgeeks.org/tcp-ip-model/)
  * Process / application layer
  * Host-to-host / transport layer
  * internet layer
  * network access / link layer
* TCP - transmission control protocol. Has packet acknowledgement
* UDP - user datagram protocol. Sends data with no acknowledgment
* Packets - small amount of data sent over a network [src](https://techterms.com/definition/packet#:~:text=A%20packet%20is%20a%20small,(or%20data)%20being%20transferred.)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
Sockets
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
Rooms and namespaces, and how this would work IRL.
3. What are you most excited about trying to implement or see how it works?
An actual system that uses these technologies with a front end.

## Preparation Materials

* [Socket.io Chat Example](https://socket.io/get-started/chat/)
* [Rooms and Namespaces](https://socket.io/docs/v3/rooms/index.html)
* [Socket.io Emit Cheatsheet](https://socket.io/docs/v3/emit-cheatsheet/index.html)
