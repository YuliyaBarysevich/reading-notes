# Express REST API


- [Middleware](https://www.tutorialspoint.com/expressjs/expressjs_middleware.html)
- [The route handler is middleware?](https://stackoverflow.com/questions/58925276/what-is-the-difference-between-a-route-handler-and-middleware-function-in-expres)]


## Review, Research, and Discussion

1. Name 3 real world use cases where you’d want to change the request with custom middleware
    - adding a new user with login and password
    - checking if user is logged in already 
    - display Date data


2. True or false: The route handler is middleware?
    - TRUE
    - Middleware functions are functions that take an extra argument, next along with req and res which is used to invoke the next middleware function. app.use() and the other HTTP derived methods(app.get(), app.all() etc) can use middleware functions. The difference between handler function and middleware function is same on both app and router object.
    - On the other hand, a handler function is a function that is specified by the routing methods. So when any of the routing methods pass a function that has req, res, and next then it is both a middleware function and a handler function.


3. In what ways can a middleware function end the process and send data to the browser?
   - when we use res.send(). 

```javascript
const validator = (req, res, next) => {
  if(req.query.name){
    res.status(200).send(req.query)
  } 
  else{
    next()
  }
}

```

```javascript

//middleware
var requestTime = function (req, res, next) {
  req.requestTime = Date.now()
  next()
}

//server.js
app.use(requestTime)

app.get('/', function (req, res) {
  var responseText = 'Hello World!<br>'
  responseText += '<small>Requested at: ' + req.requestTime + '</small>'
  res.send(responseText)
})
```

4. At what point in the request lifecycle can you “inject” middleware?
    - When server recieves a request, before it send back a response

5. What can cause express to error with “Request headers sent twice, cannot start a second response”
    - It usually happens when someone treats an async response inside an express route as a synchronous response and they end up sending data twice.

## Vocabulary Terms

1. Middleware
    - Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

2. [Request Object](https://www.tutorialspoint.com/nodejs/nodejs_request_object.htm)
    - The req object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on.

3. [Response Object](https://www.tutorialspoint.com/nodejs/nodejs_response_object.htm)
    - The res object represents the HTTP response that an Express app sends when it gets an HTTP request.

4. [Application Middleware](http://expressjs.com/en/guide/using-middleware.html#middleware.application)
    - Bind application-level middleware to an instance of the app object by using the app.use() and app.METHOD() functions, where METHOD is the HTTP method of the request that the middleware function handles (such as GET, PUT, or POST) 

5. [Routing Middleware](http://expressjs.com/en/guide/using-middleware.html#middleware.application)
    - Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().

6. [Test Driven Development](https://en.wikipedia.org/wiki/Test-driven_development)
    - Test-driven development (TDD) is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. This is opposed to software being developed first and test cases created later.
    
7. [Behavioral Testing](https://medium.com/javascript-scene/behavior-driven-development-bdd-and-functional-testing-62084ad7f1f2)
    - is a methodology where units of code are tested in isolation from the rest of the application.Unit tests are great to learn whether or not individual parts of an application work. 