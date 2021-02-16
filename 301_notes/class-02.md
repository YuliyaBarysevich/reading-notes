# jQuery, Events, and The DOM

**Resources**:
1. 'JavaScript and jQuery'  by Jon Duckett  

## jQuery 

- offers a simple way to achieve a variety of common JavaScript tasks quickly and consistently.

1. Select Elements
    - It is simpler to access elements using jQuery's CSS-style selectors than it is using DOM queries.
2. Perform Tasks
    - jQuery methods let update the DOM tree, animate elements into and out of view, and loop through a set of elements, all ine one line of code.
3. Handle Events 
    - jQuery includes methods that allow to attach event listeners to selected elements without having to write any fallback code to support older browsers.

```javascript 

//JS 

var el = document.getElementById('start')
el.innerHTML = 'GO';

//jQuery 

$('#start').html('GO');
```  

### Getting Started

- good practice to wait for the HTML document to be fully loaded and ready before working with it.  

1. Link jQuery in HTML file 

```html 
<head>
  <script src = "https://code.jquery.com...">
  </script>
</head>
``` 

2. Make HTML document to be fully loaded and ready before working with it

```javascript 

$(document).ready(function(){
  // jQuery code goes here
});

//shortcut 
$(function(){
  //jQuery code goes here
})
``` 

3. Basic Syntax
    - `$("selector").action()``
    - **$** accesses jQuery.
    - **(selector)** finds HTML elements.
    - **action()** is then performed on the element(s).

### Selectors 

```javascript 
$("div")  // selects all <div> elements

$("#test") // select the element with the id="test"

$(".menu") //selects all elements with class="menu"

$("div.menu")  // all <div> elements with class="menu"

$("p:first")  // the first <p> element

$("h1, p") // all <h1> and all <p> elements

$("*")  // all elements of the DOM
``` 
### Get & Set Attribute Values


We can manipulate attributes (`href`, `src`, `id`, `class`, `style`) assigned to HTML elements easily through jQuery. 

**The _attr()_ method is used for getting value of an attribute.**

```html 

<a href = "www.google.com">
  Click Here
  </a>
```

```javascript 
$(function(){
  var value = $('a').attr('href');
  alert(value);
});

//alerts "www.google.com"
``` 

**The _attr()_ method also allows to set a value for an attribute by specifying it as the second parametr.**

```javascript 

$(function(){
  $('a').attr('href', 'https://www.amazon.com')
})
``` 

**_removeAttr()_ method is used for removing any attribute of an element.**

```javascript 

$(function(){
  $('table').removeAttr('class');
})
``` 
**GET / SET Content**

**_html()_ method is used to get the content of HTML elements, including the HTML markup.**

**_text()_ method is used to get only text content**  

> The same `html()` and `text()` methods can be used to change content of HTML elements.

```javascript 

$(function(){
  $('#test').text('hello!')
})
``` 

### Adding Content

jQuery has methods that are used to add new content to a selected element without deleting the existing content:

1. `append()` 
    - inserts content at the end of the selected elements.
2. `prepend()` 
    - inserts content at the beginning of the selected elements.
3. `after()` 
    - inserts content after the selected elements.
4. `before()` 
    - inserts content before the selected elements.  

The `append()`, `prepend()`, `before()` and `after()` methods can also be used to add newly created elements. 

```html 

<p id="demo">Hello</p>

``` 

```javascript 
$(function() {
    var txt = $("<p></p>").text("Hi");
    $("#demo").after(txt);
});

//  inserts the newly created <p> element after the #demo paragraph.
```

## Manipulating CSS  

- jQuery has several methods for CSS manipulation.

1. `addClass()`
    - adds one or more classes to the selected elements.
2. `removeClass()`
    - removes one or more class names from the selected elements.
3. `toggleClass()`
    - toggles between adding/removing classes from the selected elements (if the specified class exists for the element, it is removed, and if it does not exist, it is added). 

## Manipulating DOM  

| Method  |  What It Returns |
|---|---|
| `parent`  | direct parent element of the selected element  |
| `parents()`  | all ancestor elemnts of the selected element  |
| `children()`  | all direct children of the selected element  |
| `siblings()`  | all siblings elements  |
| `next()`/`nextAll()`  | next / all next sibling element/s  |
| `prev()`/`prevAll()`  | previous/all previous sibling elementof the selected element  |
| `eq()`  | element with a specific index number of the selected elements  |

```javascript
// The eq() method can be used to select a specific element from multiple selected elements.
// For example, if the page contains multiple div elements and we want to select the third one

$("div").eq(2);

``` 

### Remove Elements

**`remove()` method**

```html 
<p style="color:red">Red</p>
<p style="color:green">Green</p>
<p style="color:blue">Blue</p>
```

```javascript 
$(function() {
    $("p").eq(1).remove();
});

// removes Green, the second paragraph element. 
```

**`empty()`method**  

- used to remove the child elements of the selected element(s).

```html 
<div>
   <p style="color:red">Red</p>
   <p style="color:green">Green</p>
   <p style="color:blue">Blue</p>
</div>
```
```javascript 
$(function() {
    $("div").empty();
});
// removes all the three child elements of the div, leaving it empty.
``` 