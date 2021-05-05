# Class 12

**Resources:**

- [The Computer Dictionary](https://techterms.com/definition/packet)
- [Accepting Connections](https://www.gnu.org/software/libc/manual/html_node/Accepting-Connections.html)
- [Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)
- [Event Queue](https://www.techopedia.com/definition/24963/event-queue)

## Review, Research, and Discussion

1. **What is the benefit of transforming data into packets?**
    - Packets are intended to transfer data reliably and efficiently. Instead of transferring a large file as a single block of data, sending smaller packets helps ensure each section is transmitted successfully. 
2. UDP is often refereed to as a connectionless protocol. Why is this?
    - No connection needs to be established between the source and destination before you transmit data. UDP does not acknowledge that the packets being sent have been received.
3. Can a socket server application have multiple socket connections?
    - A socket that has been established as a server can accept connection requests from multiple clients. The server’s original socket does not become part of the connection; instead, accept makes a new socket which participates in the connection. accept returns the descriptor for this socket. The server’s original socket remains available for listening for further connection requests.
4. Can a socket connection application be connected to multiple socket servers?
    - You can have two socket.io servers attached to the same web server. To make it work, each socket.io instance needs to be on a different path (one can be the default path and one can be custom). That means you need to set the path option in both socket.io client and socket.io server to match for one of the servers.
5. Can an application be both a socket server and a socket connection?

## Vocabulary Terms

1. Observer Pattern
    - it is a popular pattern used across all sorts of JavaScript applications. The instance (subject) maintains a collection of objects (observers) and notifies them all when changes to the state occurs. 
2. Listener
    - An event listener is a procedure or function in a computer program that waits for an event to occur. Examples of an event are the user clicking or moving the mouse, pressing a key on the keyboard and etc. The listener is programmed to react to an input or signal by calling the event's handler.
3. Event Handler
    - The browser notifies the system that something has happened, and that it needs to be handled. It gets handled by registering a function, called an event handler, that listens for a particular type of event.
4. Event Driven Programming
    - Event-driven programming is when a program is designed to respond to user engagement in various forms. It is known as a programming paradigm in which the flow of program execution is determined by “events.” Events are any user interaction, such as a click or key press, in response to prompt from the system.
5. Event Loop
    - The event loop is what allows Node.js to perform non-blocking I/O operations — despite the fact that JavaScript is single-threaded — by offloading operations to the system kernel whenever possible.
6. Event Queue
    - An event queue is a repository where events from an application are held prior to being processed by a receiving program or system. Event queues are often used in the context of an enterprise messaging system.
7. Call Stack
    - This is where all javascript code gets pushed and executed one by one as the interpreter reads program, and gets popped out once the execution is done. If statement is asynchronous: setTimeout, ajax(), promise, or click event, then that code gets forwarded to Event table, this table is responsible for moving asynchronous code to callback/event queue after specified time.
8. Emit/Raise/Trigger
    - An event emitter is a pattern that listens to a named event, fires a callback, then emits that event with a value. Sometimes this is referred to as a “pub/sub” model, or listener.
9. Subscribe
    - It is part of Publish/Subscribe Pattern. 
    - The Observer Pattern defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.
    - The main idea is that we have one main object to which you subscribe (Subject/Observable) and a lot of objects (Observers) that subscribe and wait for events.
10. Database
    - A database is a data structure that stores organized information. Most databases contain multiple tables, which may each include several different fields. 