# CSS Colors

> Every color on a computer screen is created by mixing amounts of red, green, and blue.

## The Main Color Properties in CSS

1. Color: 
    - the color property allows you to specify the color of text inside an element.

2. Backgrround-color:
    - CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

## How we can specify colors in CSS?

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
````

> Alpha (hsla or rgba) - opacity property which allows you to specify the opacity of an element. The value is a number between 0 and 1. (0.5 is 50% of opacity and 0.15 is 15% of opacity)

