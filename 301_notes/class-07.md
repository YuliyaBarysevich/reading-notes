# APIs continued

**Resources:**

1. [How I explained REST to my brother](https://gist.github.com/brookr/5977550)  
2. [SuperAgent](http://smalljs.org/ajax/superagent/)
3. [Documentation for SuperAgent](https://visionmedia.github.io/superagent/)
4. [What Google Learned From Its Quest to Build the Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html);

## What is SuperAgent? 

- SuperAgent is a light-weight, flexible and expressive Ajax library.

**The Basics =>**

```javascript
//If using npm
var request = require('superagent');

//request can be initiated by invoking the appropriate method on the request object, then calling .then()
 request
   .post('/api/pet')
   .send({ name: 'Manny', species: 'cat' })
   .set('X-API-Key', 'foobar')
   .set('Accept', 'application/json')
   .then(res => {
      alert('yay got ' + JSON.stringify(res.body));
   });
// simple GET request

 request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });

// HTTP method may also be passed as a string
request('GET', '/search').then(success, failure);
``` 
To Be Continued ...

## What google has learned about its quest to build the perfect team?  

Many of today’s most valuable firms have come to realize that analyzing and improving individual workers ­— a practice known as ‘‘employee performance optimization’ — isn’t enough. As commerce becomes increasingly global and complex, the bulk of modern work is more and more team-based.  

Studies also show that people working in teams tend to achieve better results and report higher job satisfaction. In a 2015 study, executives said that profitability increases when workers are persuaded to collaborate more.  

Team members may behave in certain ways as individuals — they may chafe against authority or prefer working independently — but when they gather, the group’s norms typically override individual proclivities and encourage deference to the team.  

**Behaviors that all the good teams generally shared**:

1. Members of team spoke in roughly the same proportion.
    - On some teams, everyone spoke during each task; on others, leadership shifted among teammates from assignment to assignment. But in each case, by the end of the day, everyone had spoken roughly the same amount.
2. Good teams all have high ‘average social sensitivity’  
    - People were skilled at intuiting how others felt based on their tone of voice, their expressions and other nonverbal cues.  

For Project Aristotle, research on psychological safety pointed to particular norms that are vital to success. There were other behaviors that seemed important as well — like making sure teams had clear goals and creating a culture of dependability.  

> The technology industry is not just one of the fastest growing parts of our economy; it is also increasingly the world’s dominant commercial culture. Software engineers are encouraged to work together, in part because studies show that groups tend to innovate faster, see mistakes more quickly and find better solutions to problems.  

## [How I explained REST to my brother](https://gist.github.com/brookr/5977550)

- **HTTP**
  - _Hypertext Transfer Protocol_ is the protocol used to transfer data over the web.
  - it is capable of describing the location of something anywhere in the world from anywhere in the world. It's the foundation of the web.  
- **REST** 
  - whole world wide web is built on an architectural style _REpresentational State Transfer_
  - when _RESTful API_ is called, the server will transfer to the client a representation of the state of the requested resource

**What the server does when you, the client, call one of its APIs depends on 2 things that you need to provide to the server:**

1. An identifier for the resource you are interested in. This is the URL for the resource, also known as the endpoint. In fact, URL stands for Uniform Resource Locator.  

2. The operation you want the server to perform on that resource, in the form of an HTTP method, or verb. The common HTTP methods are GET, POST, PUT, and DELETE.