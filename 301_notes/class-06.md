#  Node, Express, and APIs


**Resources:**
1. [Linda Vivah](https://medium.com/@LindaVivah/the-beginners-guide-understanding-node-js-express-js-fundamentals-e15493462be1) 
2. [What Is Node and When Should I Use It?](https://www.sitepoint.com/an-introduction-to-node-js/)

## What is Node? 

It’s a JavaScript free and open source cross-platform for server-side programming that allows users to build network applications quickly.  

**Node.js** is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

### Running local server  

One of the most common uses for node is running your server. Let’s create your first Node.js HTTP server.

**Demo**:
_In your terminal_ => 

1. `mkdir hello-world`
    - create a folder called “Hello World”
2. `touch app.js`
    - inside the project create a file called app.js
3. Paste code below in app.js file
```javascript 

// This http variable contains a function called createServer. This is all you need to do to create an http server.
const http = require('http');

// callback function => We use the response variable that’s passed in to the callback to write the head and pass in the content type and we end that response with hello world. => This function returns an object that we are going to put in to our server variable and this object is going to have another function called “listen” =>
var server = http.createServer(function (request, response) {
    response.writeHead(200, {"Content-Type": "text/plain"});
    response.end("Hello World\n");
});

// we call listen that’s when our server is going to start running as we listen to this port.
server.listen(4000);
```

4. `node app.js`
    - run server in terminal 

5. `http://localhost:4000/`
    - open browser

### What Kind of Apps Is Node.js Suited To?

Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else. It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded. 

### Advantages of Node.js

1. It’s a JavaScript runtime built on Chrome’s V8 JavaScript engine.
    - Both Node and the JS that is executed inside of your browser are running on the same engine → It’s an open source engine that takes JS code and compiles it to much faster machine code → this is what makes Node.js so fast!
2. Uses an event-driven, non-blocking I/O model that makes it light weight & efficient
    - **Event-driven programming** is a different way of thinking about your program flow. The flow of your program is defined by the events that are taking place. (see below for more details)
    - **I/O** is Input/Output
    - **Difference between blocking & non-blocking software development** Blocking methods execute synchronously and non-blocking methods execute asynchronously. 
3. Node.js’ package ecosystem, npm, is the largest ecosystem if open source libraries in the world 