# Class 06

**Resources:**

- [What Does Singleton Mean?](https://www.techopedia.com/definition/15830/singleton)
- [Design patterns in Node.js: A practical guide](https://blog.logrocket.com/design-patterns-in-node-js/)
- [As a JS Developer, This Is What Keeps Me Up at Night](https://www.toptal.com/javascript/es6-class-chaos-keeps-js-developer-up#:~:text=Prototypes%20vs.,is%20itself%20an%20object%20instance.&text=A%20class%20constructor%20creates%20an%20instance%20of%20the%20class.)
- [When Is REST Better?](https://stormpath.com/blog/rest-vs-soap#:~:text=REST%20also%20makes%20efficient%20use,better%20support%20for%20browser%20clients.)


## Review, Research, and Discussion

1. Explain what a “Singleton” is (in Computer Science terms)

A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object. This is helpful usually when a single object is required to coordinate actions across a system.  

The singleton pattern is used in programming languages such as Java and .NET to define a global variable. A single object used across systems remains constant and needs to be defined only once rather than many times.  


2. Explain how the Singleton pattern can be used with Node modules, specifically with classes

When we need to make sure that you have one and only one instance of an object. A singleton represents a single instance of an object. Only one can be created, no matter how many times the object is instantiated.

We could implement this  by using modules and having singleton class using a locally global variable, in which to store our instance. By doing this, the class itself gets exported out of the module, but the global variable remains local to the module. 


3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

First I have to determine what is the purpose of this middleware and where will I use it later. It can be Error Handing Middleware, Logging Middleware, Router Level Middleware and etc.

 When we construct a middleware we need to pass `(request, response, next)` since middleware have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle.


## Vocabulary Terms

1. Router Middleware
    - middleware that can change user request before it reaches the server
    - If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function.

2. Dynamic Module Loading
    - This allows to dynamically load modules only when they are needed, rather than having to load everything up front.

3. Singleton Pattern
    - is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.

4. CRUD -> REST Method Matches
    - CREATE --> GET
    - READ --> POST
    - UPDATE --> PUT
    - DELETE --> DELETE
5. Mock Testing
    - Mocking means creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object’s properties, rather than its function or behavior, a mock can be used.