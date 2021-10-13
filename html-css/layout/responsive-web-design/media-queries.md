# Media Queries

Media queries allow us to add new styles or override existing styles that target specific conditions.

#### Basic Syntax

media-type can be values such as screen, print. If we leave out the media-type, then it targets all media types. We don't need to include the media-type when we are only targeting the web.

```css
@media media-type () {

}
```

```css
/* mobile-first: targets widths >= 600px */
@media (min-width:600px) {

}

/* desktop-first: targets widths <= 600px */
@media (max-width:600px) {

}

/* can combine to have a range */
@media (min-width:600px) and (max-width:600px) {

}
```

### Break points

What size should you use for your breakpoints? Some people try to target as many different devices as they can, but this isn't really very effective. 

A better process is to determine when the layout starts to fail. Play with it in the dev tools and just decide when it needs to change the layout based on how it looks.

Try to make as few breakpoints as possible to make your CSS more maintainable.

### Resources

{% embed url="https://www.freecodecamp.org/news/the-100-correct-way-to-do-css-breakpoints-88d6a5ba1862/" %}
