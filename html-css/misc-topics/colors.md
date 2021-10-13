# Colors

Computer monitors are made up of thousands of tiny squares called pixels. Each pixel can be a different color. The color of each pixel is a mixture of the amounts of red, green and blue.

We're going to cover the three most common ways to specify colors in CSS:

* named colors
* hex codes
* RGB values

## Named Colors

```css
p {
    color: red;
}
```

Using named colors is the easiest format for adding color in CSS, but is primarily used for prototypes, since they only represent a small fraction of the available colors.

There are currently 140 color names supported by modern browsers. Red, blue gold, and maroon are just a few examples. You can find the full list below.

{% embed url="https://htmlcolorcodes.com/color-names/" %}

## Hex Codes

```css
p {
    color: #644B92;
}
```

Hex color codes are specified by a hashtag followed by three pairs of characters that represent the intensity of the three primary colors (red, green, and blue). Possible values range from 0 to 255, but are expressed in hexadecimal. 00 (the lowest intensity) to FF (the highest intensity).

* **White**: #FFFFFF (highest intensity for all)
* **Black**: #000000 (lowest intensity for all)
* **Red**: #FF0000
* **Green**: #00FF00
* **Blue**: #0000FF

{% hint style="info" %}
Transparency can be specified by adding two additional digits. Values range from 00 (completely transparent) to 99 (completely opaque).
{% endhint %}

```css
.p1 {
  background-color: #FF0000;
}
.p2 {
  background-color: #FF000050;
}
```

Since there are so many possibilities, web developers use color picker tools to find the hex values for colors.

{% embed url="https://htmlcolorcodes.com/color-picker/" %}

```css
p {
    rgb(116, 96, 152);
}
```

## RGB Values

RBG color codes are similar to hex, except represented by decimal values between 0 and 255 for the intensity of the red, green and blue colors.

* **White**: rgb(255, 255, 255) (highest intensity for all)
* **Black**: rgb(0, 0, 0) (lowest intensity for all)
* **Red**:  rgb(255, 0, 0)
* **Green**: rgb(0, 255, 0)
* **Blue**: rgb(0, 0, 255)

{% hint style="info" %}
**Transparency** : add a fourth value to indicate the transparency. Values range from 0 (completely transparent) to 1 (completely opaque).
{% endhint %}

```css
.p1 {
    background-color: rgb(255, 0, 0);
}

.p2 {
    background-color: rgb(255, 0, 0, .5);
}
```

## HSL

{% embed url="http://web.simmons.edu/~grovesd/comm244/notes/week3/css-colors#hsl" %}

## Resources

The following page has a very good overview of the different options and formats for specifying colors.

{% embed url="http://web.simmons.edu/~grovesd/comm244/notes/week3/css-colors" %}
