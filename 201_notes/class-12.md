# Chart.js, Canvas

## Charts 

Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly.  

A great way to get started with charts is with **Chart.js**, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more,

**Setting up instructions**:
1. [Download Chart.js](https://github.com/nnnick/Chart.js)
2. Copy the _Chart.min.js_ out of the unzipped folder and into the directory
3. Create a new html page and import the script

```html
<head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
``` 

**Drawing a line chart**

1. Create a canvas element in our HTML in which Chart.js can draw our chart. 

```html 
<canvas id="buyers" width="600" height="400"></canvas>
``` 
2. Write a script that will retrieve the context of the canvas, so add this to the foot of your body element.

```html
<script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
</script>
```
3. Inside the same script tags we need to create our data

```html 
<!-- Object that contains labels for the base of our chart and datasets to describe the values on the chart -->
<script>
var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}
</script>
```  
## Canvas

the `<canvas>` element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be **300 pixels** wide and **150 pixels** high.  

It is always a good idea to supply an `id` attribute because this makes it much easier to identify it in a script.  

The `<canvas>` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.  

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. 

### Csnvas / Colors  

To apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

1. `fillStyle = color`
    - Sets the style used when filling shapes.
2. `strokeStyle = color`
    - Sets the style for shapes' outlines.
```css
ctx.fillStyle = 'orange';
```

### Canvas / Drawing text

The canvas rendering context provides two methods to render text:

1. `fillText(text, x, y [, maxWidth])`
    - Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
2. `strokeText(text, x, y [, maxWidth])`
    - Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

```javascript 
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}

//text is not filled in with color, only lines
  function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.strokeText('Hello world', 10, 50);
}
```  


[<== Back to ReadMe](../README.md)