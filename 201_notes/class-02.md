# Basics of HTML, CSS and JavaScript

## HTML / Structural markup

1. `<h1> </h1> - <h6> </h6>`
    - HTML has six "levels" of **headings**.
    - Browsers dispalay the contents of **headings** at different sizes.
2. `<p> </p>`
    - A **paragraph** consists of one or more sentences.
    - The start of **paragraph** is indicated by a new line.
3. `<b> </b> / <i> </i>`
    - **BOLD** & _ITALIC_
4. `<sup> </sup>`
    - Used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts
5. `<sub> </sub>`
    - Used to contain characters that should be subscript. Commonly used with foot notes or chemical formulas.

Examples for 4 & 5:

```html
<p>On the 4<sup>th</sup> of September you will learn about E = MC<sup>2</sup>.</p>
<br>
<p>The amount of CO<sub>2</sub> in the atmosphere grew by 2ppm in 2009<sub>1</sub>.</p>
``` 

<p>On the 4<sup>th</sup> of September you will learn about E = MC<sup>2</sup>.</p>

<p>The amount of CO<sub>2</sub> in the atmosphere grew by 2ppm in 2009<sub>1</sub>.</p>

6. `<br /> & <hr />`
    - Adds a line break (may be used inside a paragraph)
    - Horizontal rule break

## HTML / Semantic markup

1. ` <strong> </strong> / <em> </em> `
    - **STRONG** / _EMPHASIS_
2. ` <blockquote> </blockquote>`
    - <blockquote><p> Did you ever stop to think, and forget to start again?</p> </blockquote>
3. `<abbr> </abbr> `
    - Used for abbreviations and acronyms. 
4. `<cite> </cite>`
    - Used for referencing a piece of work such as book, film or research paper.
5. `<dfn> </dfn`
    - Used to indicate the defining instance of a new term.
6. `<address> </address>`
    - Used to contain contact details for the author of the page. 
7. `<ins> <ins> & <del> </del>`
    - <ins>best</ins> & <del>worst</del>
8. `<s> </s>`
    - Indicates something something that is no longer acuurate or relevant (but that should not be deleted)

## Introducing CSS 

**Linking CSS to HTML**

1. In HTML document inside `<head> </head>` element.

` <link href = "css/style.css" type = "text/css" rel = "stylesheet">`

2. Within an HTML page by placing inside `<style> </style> element`

```html
<head>
  <style type = "text/css">
  body {
    color: pink;
    font-size: 20px;
  }
   </style>
  </head>
``` 

## CSS Selectors

| Selector  |  Meaning |  Example |
|:-:|---|---|
| Universal Selector | Applies to all elements in the document  | `* {}` Targets all elements on the page  |
| Type Selector  | Matches elements names  | `h1, h2, h3 {}` Targets the `<h1>, <h2>, <h3>` elements  |
| Class Selector  | Matches an element whose **class** attribute has a value that matches the one specified after the period  | `.note {}` Targets any element whose **class** attribute has a value of **note** |
| ID Selector  | Matches an element whose **ID** attribute has a value that matches the one specified after the pound or hash symbol  | `#introduction {}` Targets any element whose **ID** attribute has a value of **introduction** |
| Child Selector  | Matches an element that is direct child of another  | `li > a {}` Targets any `<a>` elements that are children on an `<li>`element |
| Descendant Selector  | Matches an element that is descendant of another specified element  | `p a {}` Targets any `<a>` elements that sit inside a `<p>` element. |
| Adjacent Sibling Selector  | Matches an element that is the next sibling of another  | `h1+p {}` Targets the first `<p>` element after any `<h1>`element  |
| General Sibling Selector  | Matches an element that is a sibling of another, although it does not have to be the directly preceding element  | `h1˜p {}` If you had two `<p>` elements that are siblings of an `<h>` element, this rule would apply to both  |

## Basic JavaScript Instructions

### Writing a Script

To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.  

Start with the big picture of what you want to achive, and break that down into smaller steps:

1. Define the goal 
    - need to define the task you want to achieve.
2. Design the Script
    - to design a script you split the goal out into a series of tasks that are going to be involved in solving your problem.
3. Code each step
    - Each of the steps needs to be written in a programming language that the computer understands.  
 

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

## Decision Making / Conditions

There are often several places in a script where decisions are made that determine which lines of code should be run next.  

**There are two components to a decision**: 
1. An expression is evaluated, which returns a value.
2. A conditional statement says what to do in a given situation

```javascript 
if (score > 50) {
  document.write('You passed!')
} else {
  document.write('Try again...')
}
``` 
> **IF** the condition returns _**true**  

> execute the statements between the **first** set of curly brackets   

> **ELSE** / otherwise  

> execute the statements between the **second** set of curly brackets  

### Comparison operators

You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a Boolean: **true** or **false**.

1. == 
    - is equal to 
    - this operator compares 2 values to see if they are the same
2. === 
    - strict equal to 
    - this operator compares two values to check that both the data type and value are the same.
3. !=
    - is not equal to
    - this operator compares 2 values to see if they are _not_ the same.
4. !==
    - strict not equal to
    - this operator compares 2 values to check that both he data type and value are _not_ the same.
5. `>`
    - greater than
6. < 
    - less than 
7. `>`=
    - greater than or equal to
8. <=
    - less than or equal to 

### Logical operators 

Comparison operators usually return single values of **true** or **false**. Logical operators allow you to compare the results of more than one comparison operator.

```javascript
((5 < 2) && (2 >= 3))
```

1. && 
    - LOGICAL _**AND**_
    - if both expressions evaluate to **true** then the expression returns **true**. If just one of these returns **false**, the the expression will return **false**.
2. ||
    - LOGICAL _**OR**_
    - if either expression evaluates to **true**, then the expression returns **true**. If both return **false**, then the expression will return **false**.
3. !
    - LOGICAL _**NOT**_
    - this reverses the state of an expression. If it was **false** it would return **true**. If the statement was **true**. it would return **false**
> !true returns false; !false returns true;


## Loops 

Loops check a condition. If it returns **true**, a code block will run. Then the condition will be checked again and if it still returns **true**, the code block will run again. It repeats until the condition returns **false**. There are three common types of Loops:

1. **FOR**
    - If you need to run code a specific number of times, use a for loop. In a for loop, the condition is usually a counter which is used to tell how many times the loop should run.
```javascript
for (var i = 0; i < 10; i++) {
    document.write(i);
    
}
``` 

2. **WHILE**
    - The purpose of a while loop is to execute a statement or code block repeatedly as long as an expression is true. Once the expression becomes false, the loop terminates.

```javascript
var count = 0;
 document.write("Starting Loop ");
         
while (count < 10) {
    document.write("Current Count : " + count + "<br />");
    count++;
}
``` 

[<== Back to ReadMe](../README.md)