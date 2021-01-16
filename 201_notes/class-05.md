# Images, Color, and Text

## Images 

1. Images can be used to set the tone for a site in less time than it takes to read a description.
2. If you have a page that shows several images then putting them on a simple, consistent background helps them look better as a group.  

**Stock Photos**:
- www.istockphoto.com
- www.gettyimages.com
- www.veer.com
- www.sxc.hu
- www.fotolia.com  

**Adding Images**

Need to use `<img>`tag following `src` attribute (tells the browser where it can find the image file) and `alt` attribute (provides text description if you cannot see the image).

```html
<img src = "images/pic.jpg" alt ="Ocean view" />
```

**Height / Width**

Height and width can specified inside `<img>`tag. But better practice is to specify it in CSS.

```html
<img src = "images/pic.jpg" alt ="Ocean view" width="600" height="400"/>

<style>
 img {

   height: 400px;
   width: 600px;
 } 
  </style>
``` 

> `<img>` is inline element. If it is inside a block level element, any text or other inline elements will flow around the image.

**Three rules for creating Images**

1. Save Images in the right format
    - Websites mainly use images in **jpeg**, **gif**, or **png** format. If you choose the wrong image format then your image might not look as sharp as it should and can make the web page slower to load.
2. Save Images at the right format
    - You should save the image at the same width and height it will appear on the website (measured in px). 
3. Measure Images in pixels
    - Computer screens are made up of tiny squares known as pixels. The number of pixels shown per inch of screen can vary if the user increses or decreses the resolution. 

**Tools to Edit & Save Images**

- www.photoshop.com
- www.pixlr.com
- www.splashup.com
- www.ipiccy.com

**HTML: FIGURE & FIGURE CAPTION**

Images often come with captions. In HTML5 you can use `<figure>` element to wrap images and their caption so that the two are assoiciated.  You can have more than one images inside the `<figure>` element as long as they all share the same caption. The `<figcaption>` element allows web page author to add a caption to an image. 

```html
<figure>
<img src = "image/otters.jpg" alt = "Picture of two sea otters floating in water" />
<br />
<figcaption>Sea otters hold hands when they sleep so they don't drift away from each other.</figcaption>
</figure>
```   

## CSS / Color

> Every color on a computer screen is created by mixing amounts of red, green, and blue.

### The Main Color Properties in CSS

1. Color: 
    - the color property allows you to specify the color of text inside an element.

2. Backgrround-color:
    - CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

### How we can specify colors in CSS?

> Colors can be described in 4 different ways.

- Named colors
- Hexadecimal codes /hex colors/
- RGB / Mix of red, green, and blue/
- HSL / Mix of hue, saturation, and lightness/


### Color Names

Colors are represented by predefined names. There are only 147 names supported by browsers. 

```css
color: white;
color: MediumAquaMarine;
color: black;
color: Aqua;
```

### Hexadecimal colors

Hex values represent values for red, green, and blue in hexadecimal codes.

```css
color: #A52A2A; (Brown)
color: #000000; (Black)
color: #00FFFF; (Aqua)
color: #66CDAA; (MediumAquaMarine)
```
### RGB Values

Values for red, green, and blue are expressed as numbers between 0 and 255.

```css
color: rgb(102,205,170); (MediumAquaMarine)
color: rgb(0,255,255); (Aqua)
color: rgb(0,0,0); (Black)
```

### HSL Colors

- Hue is near to the colloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color. (0 - 360 degrees)
- Saturation is the amount of gray in color. Represented as a percentage. (100% is full saturation, 0% is a shade of gray)
- Lightness is the amount of white or black in a color. Lightness is represented as a percentage. (0% lightness is black, 100% lightness is white)

```css
color: hsl(0, 0%, 0%); (Black)
color: hsl(180, 100%, 50%); (Aqua)
color: hsl(160, 51%, 60%); (MediumAquaMarine)
```

> Alpha (hsla or rgba) - opacity property which allows you to specify the opacity of an element. The value is a number between 0 and 1. (0.5 is 50% of opacity and 0.15 is 15% of opacity).


## CSS / Text

### Properties to manipulate Text elements

1. **color**
    - used to set the color of a text
    - :black; :white; :anyColor
2. **direction**
    - used to set text direction
    - :rtl; :ltr;
3. **letter-spacing**
    - used to add or subtract space between the letters that make up a word
    - :normal; :0.4em; :1px;
4. **word-spacing**
    - used to add or subtract space between the words of a sentence 
    - :3px; :0.3em; :1em;
5. **text-align**
    - used to align the text of document.
    - :left; :right; :center; :justify;
6. **text-decoration**
    - used to underline, overline, and strikethrough text
    - :underline; :overline; :line-through;
    - _Also can be used with multiple values_ `text-decoration: solid underline purple 4px;`
7. **text-transform**
    - used to capitalize text or convert text to uppercase or lowercase letters
    - :capitalize; :uppercase; :lowercase;
8. **text-shadow**
    - used to set the text shadow around a text
    - :5px 10px; :white 2px 5px;
9. **line height**
    - used to set the space between the lines
    - :2.5; :3em; :32px;  

### CSS @font-face rule 

The CSS @font-face rule allows external fonts or font files to be imported directly into stylesheets.  

The location of the font file must be specified in the CSS rule so that the files can be loaded from that location. This rule also allows locally hosted fonts to be added using a relative file path instead of a web URL.

```css
@font-face {
  font-family: 'Glegoo';
  src: url('../fonts/Glegoo-Regular.ttf') format('truetype');
}
```

### CSS Fallback Fonts

The CSS font-family property can have multiple fonts declared in order of preference. In this case the fonts following the initial font are known as the fallback fonts.

If the initial value of the property font-family fails to load to the webpage, the fallback fonts will be used.

```css 
/* Here `Arial` is the fallback font for <p> tags */
p {
  font-family: "Helvetica", "Arial";
}
```   

[<== Back to ReadMe](../README.md)

