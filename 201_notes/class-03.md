# HTML Lists, Control Flow with JS, and the CSS Box Model

## HTML Lists

### _/UNORDERED LISTS/_

The unordered list is created with the `<ul> </ul>` element.
Each item in the list is placed between an opening `<li>` and a closing `</li>`tag.

```html
<ul>
  <li>Potatoes</li>
  <li>Milk</li>
  <li>Bread</li>
  <li>Butter</li>
 </ul>
``` 

**Output:** 
<ul>
  <li>Potatoes</li>
  <li>Milk</li>
  <li>Bread</li>
  <li>Butter</li>
 </ul>

### _/ORDERED LISTS/_

The ordered list is created with the `<ol> </ol>` element.
Each item in the list is placed between an opening `<li>` and a closing `</li>`tag.

```html
<ol>
  <li>Potatoes</li>
  <li>Milk</li>
  <li>Bread</li>
  <li>Butter</li>
 </ol>
``` 
**Output:**
<ol>
  <li>Potatoes</li>
  <li>Milk</li>
  <li>Bread</li>
  <li>Butter</li>
 </ol>

 ### _/DEFINITION LISTS/_

 The definition list is created with the `<dl> </dl>` element and usually consists of a series of terms and conditions. Inside the `<dl>`element you will usually see pairs of `<dt> </dt>` and `<dd> </dd>` elements.  
 `<dt> </dt>` is used to contain the term being defined (the definition term).  
 `<dd> </dd>`is used to contain definition.  

 ```html
 <dl>
   <dt>Bread</dt>
   <dd>A baked food made of flour.</dd>
   <dt>Coffee</dt>
   <dd>A drink made from roasted coffee beans.</dd>
  </dl>
  ``` 
  **Output:** 
  <dl>
   <dt>Bread</dt>
   <dd>A baked food made of flour.</dd>
   <dt>Coffee</dt>
   <dd>A drink made from roasted coffee beans.</dd>
  </dl>  

  ### _/NESTED LISTS/_

  You can put a second list inside an `<li>` element to create a sub-list or nested list.

  ```html
  <ul>
    <li>Mousses</li>
    <li>Pastries
      <ul>
        <li>Croissant</li>
        <li>Mille-feuille</li>
        <li>Palmier</li>
        <li>Profiterole</li>
       </ul>
      </li>
    <li>Tarts</li>
   </ul>
``` 
**Output:**
<ul>
    <li>Mousses</li>
    <li>Pastries
      <ul>
        <li>Croissant</li>
        <li>Mille-feuille</li>
        <li>Palmier</li>
        <li>Profiterole</li>
       </ul>
      </li>
    <li>Tarts</li>
   </ul>  

## CSS Box Model

### Height / Width

- **CSS** treats each **HTML** element as if it has its own box.  
- By default a box is sized to hold its contents. To set your own dimensions for a box we can use the **height** and **width** properties. 
- The most popular ways to specify the size of a box are to use **pixels**, **percentage**, or **ems**.

### Limiting Width / Limiting Height

Some page designs expand and shrink to fit the size of the user's screen. In such designs, the **min-width** property specifies the smallest size a box can be displayed at when the browser window is narrow, and the **max-width** property indicates the maximum width a box can stretch to when the browser window is wide.  

In the same way we may also want to limit the height of the box. This is achieved using the **min-height** and **max-height** properties. 

### Overflowing Content 

The overflow property tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
1. **hidden**
    - This property simply hides any extra content that does not fit in the box.
2. **scroll**
    - This property adds a scrollbar to the box so that user can scroll to see the missing content.

### Border, Margin, Padding

1. Border
    - Every box has a border (even if it is not visible). The border separates the edge of one box from another.
2. Margin
    - Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.
3. Padding
    - Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents. 

#### Borders

**Border Width**

```css
p.one{
  border-width: 2px;
}
p.two{
  border-top-width: medium;
}
p.three{
  border-width: 2px 1px 1px 2px;
}
``` 
**Border Style**

- solid
- dotted 
- dashed
- double
- groove (appears to be carved into the page)
- ridge (appears to stick out from the page)
- inset (appears embedded into the page)
- outset (looks like it is coming out of the screen)
- hedden/none

**Border Color**

You can specify the color of a border like any other color in CSS.  

It is possible to individually control the colors of the borders on different sides of a box using.  

```css
border-top-color:
border-right-color:
border-bottom-color:
border-left-color:
``` 

**Shorthand Border**

The border property allows to specify the width, style and color in one property.

```css
p{
border: 3px dotted black;
}
``` 

#### Padding

Padding property allows you to specify how much space should appear between the content of an element and its border.

```css
p {
  padding: 10px;
}
h1 {
  padding-top: 10px;
  padding-right: 15px;
  padding-bottom: 20px;
  padding-left: 15px;
}
h2{
  padding: 10px 15px 20px 15px;
}
``` 

#### Margin

Margin property controls the gap between boxes. 
```css
p {
  margin: 10px;
}
h1 {
  margin-top: 10px;
  margin-right: 15px;
  margin-bottom: 20px;
  margin-left: 15px;
}
h2{
  margin: 10px 15px 20px 15px;
}
``` 

> Sometimes you might see the following, which means that the left and right margins/paddings should be 10 pixels and the top and the bottom margins/paddings should be 20px: _**margin/padding: 20px 10px**_.  

#### Change Inline/Box

The **display** property alolows you to turn an inline element into a block-level element or vice versa, and can also be used to hide an element from the page.

Display: 

1. **inline**
    - This causes a block level element to act like an inline element.
2. **block**
    - This causes an inline element to act like a block-level element.
3. **inline-block**
    - This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.
4. **none**
    - This hides an element from the page. The element acts as though it is not on the page at all.

#### Visibility

The Visibility property allows you to hide bixes from users but it leaves a space where the element would have been.

Visibility: 

1. **hidden**
    - This hides the element.
2. **visible**
    - This shows the element.

## JavaScript / Arrays

Values in an array are accessed as if they are in a numbered list. 
> Numbering of the list starts at zero (not 1).

```javascript 

// create the array 
var colors = ['white', 'black', 'red']

// accessing items in an array 

var secondColor = colors[1];

//update the third item in the array 

colors[2] = 'blue';

// NOW : colors = ['white', 'black', 'red']

var numOfColors = colors.length // numOfColors = 3;
``` 
## JavaScript / Switch Statements / Loops

### Switch Statements 

The switch statements provide a means of checking an expression against multiple case clauses. If a case matches, the code inside that clause is executed.

The case clause should finish with a **break** keyword. If no case matches but a default clause is included, the code inside default will be executed.

_Note: If break is omitted from the block of a case, the switch statement will continue to check against case values until a break is encountered or the flow is broken._

```javascript
const food = 'salad';
 
switch (food) {
  case 'oyster':
    console.log('The taste of the sea 🦪');
    break;
  case 'pizza':
    console.log('A delicious pie 🍕');
    break;
  default:
    console.log('Enjoy your meal');
}
 
// Prints: Enjoy your meal
``` 

### Truthy / Falthy Values

**Falsy Values**
- false (boolean)
- 0
- Empty strings like "" or ''
- null which represent when there is no value at all
- undefined which represent when a declared variable lacks a value
- NaN, or Not a Number  

**Truthy Values**

Almost everything that is not in the _falthy_ table can be treated as it were true.

### While Loops 

The **while** loop creates a loop that is executed as long as a specified condition evaluates to **true**. The loop will continue to run until the condition evaluates to **false**. The condition is specified before the loop, and usually, some variable is incremented or altered in the **while loop** body to determine when the loop should stop.
```javascript
while (condition) {
  // code block to be executed
}
 
let i = 0;
 
while (i < 5) {        
  console.log(i);
  i++;
}
``` 
### Do...While Loop

A **do...while** statement creates a loop that executes a block of code once, checks if a condition is true, and then repeats the loop as long as the condition is true. They are used when you want the code to always execute at least once. The loop ends when the condition evaluates to false.
```javascript 
x = 0
i = 0
 
do {
  x = x + i;
  console.log(x)
  i++;
} while (i < 5);
 
// Prints: 0 1 3 6 10
``` 

### For Loop

A for loop declares looping instructions, with three important pieces of information separated by semicolons ;:

- The initialization defines where to begin the loop by declaring (or referencing) the iterator variable
- The stopping condition determines when to stop looping (when the expression evaluates to false)
- The iteration statement updates the iterator each time the loop is completed

```javascript 
for (let i = 0; i < 4; i += 1) {
  console.log(i);
};
 
// Output: 0, 1, 2, 3
```  


[<== Back to ReadMe](../README.md)