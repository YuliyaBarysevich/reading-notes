# Class 02 - Express

- [PUT / PATCH](https://stackoverflow.com/questions/21660791/what-is-the-main-difference-between-patch-and-put-request)
- [PUT / PATCH Wikipedia](https://en.wikipedia.org/wiki/Patch_verb#:~:text=The%20main%20difference%20between%20the,instructions%20to%20modify%20the%20resource.)
- [SOAP vs REST](https://raygun.com/blog/soap-vs-rest-vs-json/#:~:text=As%20opposed%20to%20SOAP%2C%20REST,protocol%20but%20an%20architectural%20style.&text=It%20allows%20different%20messaging%20formats,services%20have%20a%20better%20performance.)

## Review, Research, and Discussion

1. What’s the difference between PUT and PATCH?
    - The main difference between the **PUT and PATCH** method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource.
    - **PUT** => If user can update all or just a portion of the record, use PUT (user controls what gets updated)
    - **PATCH** => If user can only update a partial record, say just an email address (application controls what can be updated), use PATCH.

2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
    - [MockServer](https://www.mock-server.com/)
    - [Beeceptor](https://beeceptor.com/)
    - [Stoplight](https://stoplight.io/mocking/)

3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
    - 404 Not found
    - 403 Request is forbidden
    - 500 Internal Server Error

4. Compare and contrast SOAP and ReST

|   | SOAP  | REST  |
|---|---|---|
| Meaning  | Simple Object Access Protocol  | Representational State Transfer  |
| Design  | Standardized protocol with pre-defined rules to follow.  |  Architectural style with loose guidelines and recommendations. |
| Approach  | Function-driven (data available as services, e.g.: “getUser”)  | Data-driven (data available as resources, e.g. “user”).  |
| Statefulness  | Stateless by default, but it’s possible to make a SOAP API stateful.  |  Stateless (no server-side sessions). |
| Caching  |  API calls cannot be cached. | API calls can be cached.  |
| Security  | WS-Security with SSL support. Built-in ACID compliance.  | Supports HTTPS and SSL.  |
| Performance  | Requires more bandwidth and computing power.  | Requires fewer resources.  |
| Message format  | Only XML.  | Plain text, HTML, XML, JSON, YAML, and others.  |
| Transfer protocol(s)  | HTTP, SMTP, UDP, and others.  | Only HTTP  |
| Recommended for  | Enterprise apps, high-security apps, distributed environment, financial services, payment gateways, telecommunication services.  | Public APIs for web services, mobile services, social networks.  |
| Advantages  | High security, standardized, extensibility.  | Scalability, better performance, browser-friendliness, flexibility.  |
| Disadvantages  | Poorer performance, more complexity, less flexibility.  | Less security, not suitable for distributed environments.  |

## Document the following Vocabulary Terms

| Term  | Definition  |
|---|---|
| [Web Server](https://economictimes.indiatimes.com/definition/web-server)  | It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users. This intercommunication is done using Hypertext Transfer Protocol (HTTP).  |
| Express  | Express. js is a free and open-source web application framework for Node. js. It is used for designing and building web applications quickly and easily.  |
| Routing  | Routing is the process of selecting a path for traffic in a network or between or across multiple networks.  |
| WRRC  | Web Request Response Cycle. The request/response cycle traces how a user's request flows through the app. |

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
    - express
    - npm 
    - nodeJS
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    - I definently want to know about TDD
    - Middleware, I am still confused with export/import. I think I need more practice
    - Tools that allow to “mock” an API. I've never used it before
