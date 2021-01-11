# What is a Script and how to Create it?

A script is a series of instructions that a computer can follow to acheive a goal.  

Scripts are made up of instructions a computer can follow step-by-step.

## Writing a Script

To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.  

Start with the big picture of what you want to achive, and break that down into smaller steps:

1. Define the goal 
    - need to define the task you want to achieve.
2. Design the Script
    - to design a script you split the goal out into a series of tasks that are going to be involved in solving your problem.
3. Code each step
    - Each of the steps needs to be written in a programming language that the computer understands.  

## Basics 

### Arithmetic Operators in JavaScript

1. (+) - Addition
2. (-) - Substruction
3. (/) - Division
4. (*) - Multiplication
5. (++) - Increment /Adds 1 to the current number/
6. (--) - Decrement /Substracts 1 from the current number/
7. (%) - Modulus /Devides two values and returns the remainder/

### String operator in JavaScript

> There is only one string operator: the (+) symbol. It is used to join the strings on either side of it. Programmers call the process of joining together two or more strings to create one new string **concatenation**.

- When you place quotes around a number, it is a string.
- If you try to add a number data type to a string, then the number becomes part of the string.
- If you try to use any of the other arithmetic operators on a string, then the value that results is usually a value called **NaN**.

## Functions in JavaScript

Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse function (rather than repeating the same set of statements).

### Declaring a Function 

To create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces. 

```javascript
function sayHello() {
    document.write('Hello!')
}
```

### Calling a Function

Haveing declared the function, you can then execute all of the statements between its curly braces with just one line if code.

```javascript
sayHello();
```

- The function can store the instructions for a specific task. 
- When you need the script to perform that task, you call the function.
- The function executes the code in that code block
- When it has finished, the code continues to run from the point where it was initially called.

### Declaring Functions that need Information

Sometimes a function needs specific information to perform its task. In such cases, when you declare the function you give it **parameters**. Inside the function, the parameters act like **variables**

```javascript
function getArea(width, height) {
    return width * height;
};
```

> This function will caculate and return the area of a rectangle. To do this, it needs the rectangle's width and height. Each time you call the function these values could be different.

### Calling Functions that need Information

When you call a function that has parameters, you specify the values it should use in the parantheses that follow its name. The values are called **arguments**, and they can be provided as values or as variables.

1. Arguments as values 
```javascript
getArea(3,5)
```
2. Arguments as variables
```javascript
rectangleWidth = 3;
rectangleHeight = 5;
getArea(rectangleWidth, rectangleHeight);
``` 

### Getting a Single Value out of a Function

Some functions return information to the code that called them. For example. when they perform a calculation, they return the result.

```javascript
function calculateArea (width, height) {
    var area = width * height;
    return area;
}

var wallOne = calculateArea (3, 5);
var wallTwo = calculateArea (8, 5);
``` 

- This function returns the area of rectangle to the code that called it.
- Inside the function, a variable called **area** is created. It holds the calculated area of the box.
- The **return** keyword is used to return a value to the code that called the function.  

[<== Back to ReadMe](../README.md)
