# Class 13

**Resources:**

- [BENEFITS AND APPLICATIONS OF WEBSOCKETS](https://www.amx.com/en/site_elements/benefits-and-applications-of-websockets)
- [SOCKET.io](https://socket.io/docs/v4/index.html)

## Review, Research, and Discussion

1. What does it mean that web sockets are bidirectional? Why is this useful?
    - Whereas HTTP relies on a client request to receive a response from the server for every exchange,
WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates
asynchronously, without requiring the client to submit a request each time. In the context of networked AV and control
systems, this allows devices to send and receive continuous streams of data to and from any point on the network.
2. Does socket.io use HTTP? Why?
    - Yes, to connect nsmespaces and rooms
3. What happens when a client emits an event?
    - An event will be send to server 
4. What happens when a server emits an event?
    - Server defines where (all clients or not) to send data
5. What happens if a client “misses” an event?
    - Event will be ignored
6. How can we mitigate this?


## Vocabulary Terms

1. Socket
    - A socket is one endpoint of a two-way communication link between two programs running on the network.
2. Web Socket
    - WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.
3. [Socket.io](https://www.tutorialspoint.com/socket.io/socket.io_overview.htm#:~:text=Socket.IO%20is%20a%20JavaScript,between%20web%20clients%20and%20servers.&text=js.,components%20have%20an%20identical%20API/)
    - It is a JavaScript library for real-time web applications. It enables real-time, bi-directional communication between web clients and servers. 
4. Client
    - in client/server relationships the server can push messages to clients. Whenever an event occurs, the idea is that the server will get it and push it to the concerned connected clients.
5. [Server](https://techterms.com/definition/server)
    - A server is a computer that provides data to other computers. It may serve data to systems on a local area network (LAN) or a wide area network (WAN) over the Internet.
6. [OSI Model](https://techterms.com/definition/osi_model)
    - The OSI (Open Systems Interconnection) model was created by the ISO to help standardize communication between computer systems. It divides communications into seven different layers, which each include multiple hardware standards, protocols, or other types of services.
    - Layers of the OSI model : The Physical layer, The Data Link layer, The Network layer, The Transport layer, The Session layer,The Presentation layer, The Application layer
7. [TCP Model](https://www.geeksforgeeks.org/tcp-ip-model/)
    - The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. 
    - The layers are: Process/Application Layer, Host-to-Host/Transport Layer, Internet Layer, Network Access/Link Layer
8. [TCP](https://searchnetworking.techtarget.com/definition/TCP#:~:text=TCP%20(Transmission%20Control%20Protocol)%20is,of%20data%20to%20each%20other/)
    - Transmission Control Protocol.
    - It is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data.
9. [UDP](https://www.sdxcentral.com/resources/glossary/user-datagram-protocol-udp/#:~:text=User%20Datagram%20Protocol%20(UDP)%20%E2%80%93,referred%20to%20as%20UDP%2FIP/)
    - a communications protocol that facilitates the exchange of messages between computing devices in a network. It's an alternative to the transmission control protocol (TCP). In a network that uses the Internet Protocol (IP), it is sometimes referred to as UDP/IP.
10. [Packets](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/#:~:text=In%20networking%2C%20a%20packet%20is,or%20device%20that%20receives%20them.&text=This%20is%20similar%20to%20how%20packets%20work%20on%20the%20Internet/)
    - is a small segment of a larger message. Data sent over computer networks, such as the Internet, is divided into packets.