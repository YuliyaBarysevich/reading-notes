# The Call Stack and Debugging

1. [Call stack MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
2. [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

## What is call stack? 

A **call stack** is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

**Summary:**  

we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

## JavaScript error messages && debugging

**Types of error messages:**

1. Reference errors
    - when we try to use a variable that is not yet declared you get this type os errors.
    - when we assign variable value before declaration.

2. Syntax errors
    - occurs when we have something that cannot be parsed in terms of syntax

3. Range errors
4. Type errors
    - occurs when the types (number, string and so on we are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

### Debugging

To debug JS code, the easiest and maybe the most common way its to simply console.log() the variables we want to check or, by using chrome developer tools.  

_Using Node.js with Visual Studio Code we can press the debug tab and add a configuration similar to this:_

```json 
"version": "0.2.0",
"configurations":[
  {
    "type": "node",
    "request": "launch",
    "name": "Launch Program",
    "program": "${workspaceRoot}/index.js"
  }
]
// debugger by pressing F5
``` 
Another way to find errors in code, using call stack in the console, which is the path that program has taken to reach the point were we set a breaking point or were we have an error.
>For call stack it’s better to navigate when you have names to your functions

### Handling errors

Good practice to handle errors is `try` to `catch` the errors so we can fallback to a default state of our application in case of an error.

```javascript
(function testing(){
  function add(a, b) {
    try {
      var result = a + b
      return result.split('')
    } catch (error) {
      console.error('add went wrong ->', error)
      return [] // default value
    }
  }
  var stringResult = add("1", "2")
  var numberResult = add(1, 2)
})()
``` 

Tools to avoid runtime errors: 

- [quokka](https://quokkajs.com/) to evaluate your code as you type
- [https://eslint.org/](https://eslint.org/) to make sure style guide is consistency.
