# Object-Oriented Programming, HTML Tables

## HTML Tables

A table represents information in a grid format.  

### Basic Table Structure

1. `<table> </table>`
    - used to create a table. The contents of the table are written out row by row.
2. `<tr> </tr>`
    - indicates the start of each row
    - it is follow =d by one or more `<td>`elements
    - at the end of the row you use `</tr>`tag.
3. `<td> </td>`
    - each cell of a table is represented using `<td>`element
    - stands for table data
4. `<th> </th>`
    - used like `<td>` element but its purpose is to represent the heading for either a column or a row.
    - even if a cell has no content, you should still use a `<td>` or `<th>` element to represent the presence of an empty cell.

### Spanning Columns / Rows

> The _**colspan**_ attribute can be used on a `<th>` or `<td>` element and indicates how many columns that cell should run across.

> The _**rowspan**_ attribute can be used on a `<th>`or `<td>` element to indicate how many rows a cell should span down the table.

## Object-Oriented Programming

### Creating an Object: Constructor Notation

The _**new**_ keyword and the object constructor create a blank object. Then we can add properties and methods to the object.

```javascript

// creating a new object using a combination of the 'new' keyword and the 'Object()` constructor function.

var hotel = new Object();

//adding properties and methods using dot notation

hotel.name = 'Quay';
hotel.rooms = 40;
hotel.booked = 25;
hotel.checkAvailability = function () {
  return this.rooms - this.booked;
}
``` 

### Updating an Object 

To update the value of properties, we can use dot notation or square brackets.

> To delete a property, we can use the _**delete** _keyword.

```javascript 
//if the object does not have adding property, it will be added to the object

//dot notation
hotel.name = 'Park';

//square brackets notation

hotel['name'] = 'Park';

//deleting a property
delete hotel.name;

// clear the value of a property, setting it to a empty string
hotel.name = '';
``` 

### Creating many Objects: Constructor Notation

If we need to create several objects to represent similar things, we can use **Object Constructors.  

First, we need to create the template with the object's properties and methods.

```javascript 
function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.rooms - this.booked;
  };
}

// 'this' keyword is used instead of the object name to indicate that the property or method belongs to the object that 'this' function creates.
// the name of a constructor function usually begins with a capital letter

var quayHotel = new Hotel ('Quay', 40, 25);
var parkHotel = new Hotel ('Park', 120, 77);
``` 

### Arrays of Objects & Objects in Arrays

Arrays are actually a special type of object. They hold a related set of key/value pairs (like all objects), but the key for each value is its index number.  

We can combine arrays and objects to create complex data structures: Arrays can store a series of objects (and remember their order). Objects can also hold arrays (as values of their properties).

### The Browser Object Model: the Window Object

The window object represents the current browser window or tab. It is the topmost object in the Browser Object Model, and it contains other objects that tell about browser.

| PROPERTY  | DESCRIPTION  |
|---|---|
| `window.innerHeight`  | Height of window (excluding browser chrome/user interface) (in pixels)  |
| `window.innerWidth` | Width of window (excluding browser chrome/user interface) (in pixels)  |
| `window.pageXOffset`  | Distance document has been scrolled horizontally (in pixels)  |
| `window.pageYOffset`  | Distance document has been scrolled vertically (in pixels)  |
| `window.screenX`  | X-coordinate of pointer, relative to top left corner of screen (in pixels)  |
| `window.screenY`  | Y-coordinate of pointer, relative to top left corner of screen (in pixels)|
| `window.location`  | Current URL of window object (or local file path)  |
| `window.document`  | Reference to document object, which is used to represent the current page contained in window  |
| `window.history`  | Reference to history object for browser window or tab, which contains details of the pages that have been viewed in that window or tab  |
|`window.history.length`| Number of items in hi story object for browser window or tab  |
| `window.screen` | Reference to screen object  |
| `window.screen.width`  | Accesses screen object and finds value of its width property (in pixels)  |
| `window.screen.height`  |Accesses screen object and finds value of its height property (in pixels)   |


| METHOD  | DESCRIPTION  |
|---|---|
| `window.a1ert()`  | Creates dialog box with message (user must click OK button to close it)  |
| `window.open()`  | Opens new browser window with URL specified as parameter|
| `window.print()`  | Tells browser that user wants to print contents of current page (acts like user has clicked a print option in the browser's user interface) |

### The Document Object Model: the Document Object   

Here are some properties of the document object, which tell you about the current page

| PROPERTY  | DESCRIPTION  |
|---|---|
| `document.title` | Title of current document  |
| `document.lastModified`  | Date on which document was last modified  |
| `document.URL`  | Returns string containing URL of current document  |
| `document.domain`  | Returns domain of current document  |  

The following are few of the methods that select content or update the content of a page 
| METHOD  | DESCRIPTION  |
|---|---|
| `document.write()`  | Writes text to document   |
| `document.getElementByld()`  | Returns element, if there is an element with the value of the id attribute that matches   |
| `document.querySe1ectorAll()`  | Returns list of elements that match a CSS selector, which is specified as a parameter  |
| `document.createElement()`  | Creates new element  |
| `document.createTextNode()`  | Creates new text node  |


### Global Objects: String Object   

These properties and methods are often used to work with text stored in variables or objects.

| METHOD  | DESCRIPTION  |
|---|---|
| `toUpperCase()`  |Changes string to uppercase characters   |
| `toLowerCase()`  | Changes string to lowercase characters  |
| `charAt()`  | Takes an index number as a parameter, and returns the character found at that position  |
| `indexOf()`  | Returns index number of the first time a character or set of characters is found within the string  |
| `lastIndexOf()`  | Returns index number of the last time a character or set of characters is found within the string  |
| `substring()`  | Returns characters found between two index numbers where the character for the first index number is included and the character for the last index number is not included  |
| `split()`  | When a character is specified, it splits the string each time it is found, then stores each individual part ih an array  |
| `trim()`  |Removes whitespace from start and end of string   |
| `replace()`  |Like find and replace, it takes one value that should be found, and another to replace it (by default, it only replaces the first match it finds)   |

### Global Objects: Math Object

The Math object has properties and methods for mathematical constants and functions.

| PROPERTY / METHOD  | DESCRIPTION  |
|---|---|
| `Math.PI` | Returns pi (approximately 3.14159265359)  |
| `Math.round()`  | Rounds number to the nearest integer  |
| `Math.sqrt(n)`  | Returns square root of positive number, e.g., Math.sqrt(9) returns 3  |
| `Math.ceil()` |Rounds number up to the nearest integer   |
| `Math.floor()`  | Rounds number down to the nearest integer  |
| `Math.random()`  | Generates a random number between 0 (inclusive) and 1(not inclusive)  |  

### GlobalObjects: Date Object (and Time)

In order to work with dates, we create an instance of the Data object.  

To create Data object, we can use the `Data()`object constructor. The syntax is the same for creating any object with a constructor function.  

By default, when we create a Data object it will hold today's date and the current time.

| METHOD  | DESCRIPTION  |
|---|---|
| `getDate()`/ `setDate()`  | Returns / sets the day of the month  |
| `getDay()`  | Returns the day of the week (0-6)  |
| `getFullYear()` / `setFullYear()`  | Returns / sets the year (4 digits)  |
| `getHours()`/ `setHours()`  | Returns / sets the hour (0-23)  |
| `getMilliseconds()`/ `setMilliseconds()`  | Returns / sets the milliseconds(0-999)  |
| `getMinutes()`/ `setMinutes()`  | Returns / sets the minutes(0-59)  |
| `getMonth()`/ `setMonth()`  | Returns / sets the month (0-11)  |
| `getSeconds()`/ `setSeconds()`  | Returns / sets the seconds (0-59)  |
| `getTime()` / `setTime()`  |Number of milliseconds since January 1, 1970, 00:00:00 UTC (coordinated Universal Time) and a negative number for any time before  |
| `getTimezoneOffset()`  |Returns time zone offset in mins for locale   |
| `toDateString()` | Returns "date" as a human-readable string  |
| `toTimeString()`  | Returns "time" as a human-readable string  |
| `toString()`  | Returns astring representing the specified date  |  

[<== Back to ReadMe](../README.md)