# Data Modeling  

**Resources:**

- [Why Use Test Driven Development](https://www.codica.com/blog/test-driven-development-benefits/)
- [Advantages and disadvantages of Test Driven Development ](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-test-driven-development-tdd/#:~:text=Probably%2C%20the%20strongest%20argument%20against,vary%20the%20code%20and%20tests.&text=So%2C%20actually%2C%20this%20disadvantage%20is,apparently%20takes%20an%20extended%20time.)
- [As a JS Developer, This Is What Keeps Me Up at Night](https://www.toptal.com/javascript/es6-class-chaos-keeps-js-developer-up#:~:text=Prototypes%20vs.,is%20itself%20an%20object%20instance.&text=A%20class%20constructor%20creates%20an%20instance%20of%20the%20class.)
- [When Is REST Better?](https://stormpath.com/blog/rest-vs-soap#:~:text=REST%20also%20makes%20efficient%20use,better%20support%20for%20browser%20clients.)

## Review, Research, and Discussion

1. Name 3 advantages to Test Driven Development
   - TDD reduces the time required for project development. The TDD approach allows identifying any issues very fast due to fast feedback.
   - Code flexibility and easier maintenance. According to the IEEE Software publication, implementation of Test Driven Development reduces the percentage of bugs by 40 - 80 percent, which consequently means that less time is required for fixing them.
   - Better program design and higher code quality. When writing tests, programmers first have to define a goal they will achieve with the code piece.
2. In what case would you need to use beforeEach() or afterEach() in a test suite?
    - beforeEach and afterEach can handle asynchronous code in the same ways that tests can handle asynchronous code - they can either take a done parameter or return a promise. 
3. What is one downside of Test Driven Development
    - Tests got to be maintained when requirements change
4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    - The most important difference between class- and prototype-based inheritance is that a class defines a type which can be instantiated at runtime, whereas a prototype is itself an object instance.
5. Why REST?
    - REST is easy to understand: it uses HTTP and basic CRUD operations, so it is simple to write and document. This ease of use also makes it easy for other developers to understand and write services against.
    - REST supports many data formats, but the predominant use of JSON means better support for browser clients. 

## Document the following Vocabulary Terms

1. [Functional programming](https://www.guru99.com/functional-programming-tutorial.html#1)
    - Functional programming is a way of thinking about software construction by creating pure functions. It avoid concepts of shared state, mutable data observed in Object Oriented Programming.

2. Object-oriented programming (OOP)
    - It is a programming paradigm that relies on the concept of classes and objects. It is used to structure a software program into simple, reusable pieces of code blueprints (usually called classes), which are used to create individual instances of objects.
3. Class
    - Class are a blueprint or a set of instructions to build a specific type of object. It is a basic concept of Object-Oriented Programming which revolve around the real-life entities. Class determines how an object will behave and what the object will contain.
4. [super](https://css-tricks.com/what-is-super-in-javascript/)
    - In a child class, you use super() to call its parent’s constructor and super.<methodName> to access its parent’s methods.
5. [this](https://codeburst.io/all-about-this-and-new-keywords-in-javascript-38039f71780c#:~:text=Patro%20on%20Unsplash-,What%20is%20%E2%80%9Cthis%E2%80%9D%20keyword%20in%20JavaScript,how%20the%20function%20is%20called.)
    - this keyword refers to an object, that object which is executing the current bit of javascript code.
6. [Test Driven Development (TDD)](https://en.wikipedia.org/wiki/Test-driven_development)
    - Test-driven development (TDD) is a software development process relying on software requirements being converted to test cases before software is fully developed, and tracking all software development by repeatedly testing the software against all test cases. This is opposed to software being developed first and test cases created later.
7. Jest
    - JavaScript Testing Framework with a focus on simplicity.
8. [Continuous Integration (CI)](https://www.atlassian.com/continuous-delivery/continuous-integration)
    - It is the practice of automating the integration of code changes from multiple contributors into a single software project. It’s allowing developers to frequently merge code changes into a central repository where builds and tests then run.
9. REST
    - stands for REpresentational State Transfer..
    - REST is a set of principles that define how Web standards, such as HTTP and URIs, are supposed to be used 
10. [Data Model](https://en.wikipedia.org/wiki/Data_model)
    - It is an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.