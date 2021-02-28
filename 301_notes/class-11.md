# EJS

**Resources:**
1. [Intro to EJS in ExpressJS](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)
2. [EJS Tutorial](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)

EJS stands for _Embedded JavaScript_ is a Templating Language. It is a simple templating language that lets us generate HTML markup with plain JavaScript. 

- No religiousness about how to organize things. 
- No reinvention of iteration and control-flow. It's just plain JavaScript.

**EJS Features:**

1. Very Simple Syntax
2. Use Plain JavaScript
3. Very Fast Compilation and Execution
4. Compiles with Express View system
5. Caching for template and intermediate JavaScript
6. Includes feature available
7. Easy Debugging

## Getting statrted 

1. `npm install -S ejs`
2. 

```javascript 

const express=require("express");
const path=require("path");
const ejs=require("ejs");
const app=express();

app.set('view engine', 'ejs');
app.set('views', path.join(__dirname, 'views'));
``` 

3. Create a new folder **_views_**, inside folder create a file `index.ejs`
4. 

```javascript
//creating route for the root directory
app.get('/', function(req, res){
  res.resnder('index');

})

app.listen(3000, function(){
  console.log('Now listening on localhost 3000')
})
``` 

## Injecting values into the views

```javascript 
app.get('/', function(req, res){
  res.resnder('index', {
    key: 'world';
  });

})
``` 

```html 
<!-- index.ejs file -->

<h1>Hello <%= key%></h1>

<!-- output => 'Hello world' -->

```

## For Loops and Arrays 

```javascript 
app.get('/', function(req, res){
  res.resnder('index', {
   people: [
     {name: 'john'},
     {name: 'bobby'}
   ]
  });

})
``` 
```html 
<!-- index.ejs file -->

<ul>
  <% for(let person of people) { %>
  <li><%= person.name %></li>
  <% } %>
</ul>

<!-- output => 'john' 'bobby'-->

```

## If/Else Statement 

```javascript 
app.get('/', function(req, res){
  res.resnder('index', {
   people: [
     {name: 'john'},
     {name: 'bobby'}
   ]
  });

})
``` 

```html 
<!-- index.ejs file -->

<ul>
  <% for(let person of people) { %>
    <% if(person.name === 'john' { %>
     <li>This is definitely <%= person.name %>!!!</li>
    <% } else { %>
     <li>This is definitely not John!!! This is <%= person.name%></li>
    <% } %>
  <% } %>
</ul>

<!-- output => 'This is definetly john!!!', 'This is definetly not John!!! This is bobby'-->

```

## Syntax EJS

Tags :

1. `<%` 
    - 'Scriptlet' tag, for control-flow, no output
2. `<%_` 
    - ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it
3. `<%=` 
    - Outputs the value into the template (HTML escaped)
4. `<%-` 
    - Outputs the unescaped value into the template
5. `<%#` 
    - Comment tag, no execution, no output
6. `<%%` 
    - Outputs a literal `'<%'`
7. `%>` 
    - Plain ending tag
8. `-%>` 
    - Trim-mode ('newline slurp') tag, trims following newline
9. `_%>` 
    - ‘Whitespace Slurping’ ending tag, removes all whitespace after it