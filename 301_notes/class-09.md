# Refactoring / Functional Programming 

**Resources:**

1. [Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa#_=_)
2. [Refactoring JavaScript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.  

**Fundamental concepts:**
**Pure functions**

- It returns the same result if given the same arguments 
- It does not cause any observable side effects
- Any function that relies on a random number generator cannot be pure.


```javascript 

// Impure function Because it uses a global object that was not passed as a parameter to the function.
let PI = 3.14;
const calculateArea = (radius) => radius * radius * PI;
calculateArea(10);

//Pure function. We are just accessing parameters passed to the function
let PI = 3.14;
const calculateArea = (radius, pi) => radius * radius * pi;
calculateArea(10, PI);
``` 

- It does not cause any observable side effects
  - modifying a global object or a parameter passed by reference.

```javascript 
//impure function receives counter value and re-assigns the counter with the value increased by 1.
let counter = 1;
function increaseCounter(value) {
  counter = value + 1;
}
increaseCounter(counter);
console.log(counter); // 2

//Pure function increaseCounter returns 2, but the counter value is still the same. The function returns the incremented value without altering the value of the variable.
let counter = 1;
const increaseCounter = (value) => value + 1;
increaseCounter(counter); // 2
console.log(counter); // 1
``` 

**Pure functions are  easier to test**

## Immutability

>Mutability is discouraged in functional programming.

- When data is immutable, its state cannot change after it’s created. Instead to change data, we can create a new object with the new value.

## Referential transparency

- The pure function will always have the same output, given the same input.
- If a function consistently yields the same result for the same input, it is referentially transparent.

## Functions as first-class entities

- Functions are also treated as values and used as data.
- Functions as first-class entities can:
  - refer to it from constants and variables
  - pass it as a parameter to other functions
  - return it as result from other functions

## Higher-order functions

- takes one or more functions as arguments
- returns a function as its result
- Examples: `filter()`, `map()`, and `reduce()` and etc.