# HTML & JavaScript Basics

## Structure of HTML page (Summary)

- HTML pages are text documents
- HTML uses tags (characters that sit inside <>) to give the information they surround special meaning.
- Tags usually come in pairs. 

```html
<article>
  <p>Text...</p>
  </article>
``` 

- Opening tags can carry attributes, which tell us more about the content of that element

## HTML5 Layout

- The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure.
- The new elements proviide clearer code (compared with using multiple <div> elements)
- Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements.
- [Read More about Semantic HTML](../102_notes/html_intro.md)

## JavaScript. ABC of Programming

### A. What is a script and how do I create one?

A script is a series of instructions that a computer can follow to achieve a goal.  
To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achive it.

1. Define The Goal
2. Design The Script
3. Code Each Step  

### B. How do computers fit in with the world around them?

Computers create models of the world using data.  

The models use objects to represent physical things. Objects can have: 
- **Properties** 
    - tell us about the object 
- **Methods** 
    - perform tasks using the properties of that object 
- **Events** 
    - which are triggered when a user interacts with the computer

### C. How do I write a script for a Web Page? 

JavaScript is written in plain text, just like HTML and CSS. It is best to keep JavaScript code in its own JavaScript file. Need to use (**.js**) extenssion. 

When you want to use JavaScript with web page, you use HTML `<script>` element to load JS file into the page. It has an attribute **src**. whose value is the path to the script you created.  

This tells the browser to find and load the script file (just like the src attribute on an `<img>` tag)  

[<== Back to ReadMe](../README.md)