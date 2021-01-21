# HTML Forms and JS Events

## HTML Forms / Form Controls

### Adding Text 

1. Text Input (single line)
    - used for a single line of text such as email address and username
2. Password input
    - like a single line text box but it masks the characters entered
3. Text Area (multi-line)
    - used for longer areas such as messages and comments

### Making Choices

1. Radio buttons
    - used when a user must select one of a number of options
2. Checkboxes
    - used to select and unselect one or more options
3. Drop-down boxes
    - used when a user must pick one of a number of options from a list 

### Submitting Forms
1. Submit buttons 
    - used to submit data from form to another webpage
2. Image buttons
    - similar to submit buttons but they allow to use in image
3. Uploading files
    - allows user to upload files to a website

## Form Structure 

Form controls live inside a `<form>` element. This element should always carry the **action** attribute and will usually have a method and id attribute too.  

Every `<form>`element requires an action attribute. Its value is the URL for the page on the server that will receive the information in the form when it submitted.  

Forms can be sent using one of two methods: **get** or **post**.

1. Get Method
    - values from the form are added to the end of the URL specified in the action attribute.
    - ideal for short forms (such as search boxes)
2. Post Method
    - values are sent in what are known as HTTP headers
    - need to be used if form allows users to upload a file / contains sensitive data

The `<input>` element is used to create several different form controls. The value of the type attribute determines what kind of input they will be creating.

Value of `name` attribute identifies the form control and is sent along with the information users enter to the server.

```html
<!-- element <textarea> used to create a multi-line text input -->
<form action="/example.html" method="POST">
  <textarea rows="10" cols="30" name="comment">Enter your comments...</textarea>
</form>

<!-- type="radio" attribute that renders a single radio button. Multiple radio buttons of a related topic are given the same name attribute value. Only a single option can be chosen from a group of radio buttons. -->
<form action="/example.html">
  <input name="delivery_option" type="radio" value="pickup" />
  <input name="delivery_option" type="radio" value="delivery" />
</form>

<!-- type="checkbox" attribute will render a single checkbox item. To create a group of checkboxes related to the same topic, they should all use the same name attribute. Since it’s a checkbox, multiple checkboxes can be selected for the same topic. -->
<form action="/example.html">
  <input type="checkbox" name="breakfast" value="bacon">Bacon <br>
  <input type="checkbox" name="breakfast" value="eggs">Eggs <br>
  <input type="checkbox" name="breakfast" value="pancakes">Pancakes <br>
</form>

<!-- <select> element can be used to create a dropdown list. A list of choices for the dropdown list can be created using one or more <option> elements. By default, only one <option> can be selected at a time. "multiple" attribuye allows users to select multiple options -->
<form action="/example.html">
 <select name="rental-option">
  <option value="small">Small</option>
  <option value="family">Family Sedan</option>
  <option value="lux">Luxury</option>
</select>
</form>

<!-- <input> elements can have a type attribute set to submit, by adding type="submit". With this attribute included, a submit button will be rendered and, by default, will submit the <form> and execute its action. -->
<form action = "/example.html">
<input type = "submit" name = "subscribe" value = "Subscribe" />
</form>
``` 

## List / Tables Styling CSS

Properties for LISTS:

1. `list-style-type`
    - allows to control the shape or style of a bullet point
    - can be used on rules that apply to the `<ol>`, `<ul>`, and `<li>` elements.
    - UL values (`disc`, `circle`, `square`) / OL values (`decimal-leading-zero`, `lower-alpha`, `lower-roman`)
2. `list-style-image`
    - can be used to specify an image to act as a bullet''
    - `list-style-image: url("picture.png")`
3. `list-style-position` : **outside** or **inside**
    - indicates whether the marker should appear on the inside or the outside of the box
4. `list-style`
    - shorthand property to style lists
    - `list-style: inside circle;`

Properies for TABLES:

1. `width`
    - setting the width of the table
2. `padding`
    - setting the space between the border of each table cell and its content
3. `text-transform`
    - converting the content of the table to uppercase
4. `letter-spacing`, `font-size`
5. `border-top`, `border-bottom`
6. `text-alighn` 
7. `background-color`
8. `:hover`
9. `empty-cells`
    - using to specify empty cells borders (show, hide, inherit)
10. `border-spacing`
    - allows to control the distance between adjacent cells
11. `border-collapse`
    - collapsed into a single border where possible

## JavaScript Events 

Events are actions or occurrences that happen in the system you are programming, which the system tells you about so you can respond to them in some way if desired. For example, if the user selects a button on a webpage, you might want to respond to that action by displaying an information box.  

In the case of the Web, events are fired inside the browser window, and tend to be attached to a specific item that resides in it — this might be a single element, set of elements, the HTML document loaded in the current tab, or the entire browser window. There are many different types of events that can occur. For example:

- The user selects a certain element or hovers the cursor over a certain element.
- The user chooses a key on the keyboard.
- The user resizes or closes the browser window.
- A web page finishes loading.
- A form is submitted.
- A video is played, paused, or finishes.
- An error occurs.

```html
<button>Change color</button>
``` 

```javascript
//storing a reference to the button inside a variable called btn, using the Document.querySelector() function. Defining a function that returns a random number. 
var btn = document.querySelector('button');

function random(number) {
  return Math.floor(Math.random() * (number+1));
}

btn.onclick = function() {
  const rndCol = 'rgb(' + random(255) + ',' + random(255) + ',' + random(255) + ')';
  document.body.style.backgroundColor = rndCol;
}

//code generates a random RGB color and sets the <body> background-color equal to it.
``` 
Event Types :

| Events  | Description  |
|---|---|
| load  | web page has finished loading  |
| error  | browser encounters JavaScript error  |
| click  | user presses and releases a button over the same element  |
| dblclick  | user presses and releases a button twice over the same element  |
| mousemove  | user moves the mouse  |
| mpouseover  | user moves the mouse over an element  |
| input  | Value in any `<input>` or `<textarea>` element has changed or any element with the contented i table attribute  |
| change  | Value in select box, checkbox, or radio button changes  |
| submit  | User submits a form (using a button or a key)  |
| select  | User selects some text in a form field  |
| copy  | User copies content from a form field  |
| paste  | User pastes content into a form field |
  
  
[<== Back to ReadMe](../README.md)