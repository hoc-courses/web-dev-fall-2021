# Box-Model Properties

Every element on a page is displayed as a rectangular box. The box-model describes the box. Each box consists of the following:

**Content** - The actual content (text, images, videos...) of the HTML element.

**Padding** - Defined by the padding property. In-between the border and content of an element. It is transparent.

**Border** - Defined by the border property. Surrounds the padding and content of an element.

**Margin** - Defined by the margin property. Adds space between the border and other HTML elements. Is transparent.

![](<../../.gitbook/assets/image (2).png>)

When to use the margin vs. the padding property can be confusing. The way to think about it is that the padding is specific to the element, whereas the margin is the space between elements. 

### Margins Collapse

One important aspect of margins is that they collapse vertically to the largest margin between the adjacent boxes. When adding a new section to a part of the page, you don't want to have to think about what the adjacent element's margin is. You just want to think about how much margin you want to be between them.

![](<../../.gitbook/assets/image (19).png>)

An important aspect of collapsing margins is that the first child's top margin will collapse with the margin of the parent element and the last child's bottom margin will collapse with the bottom margin of the parent element. 

To get accurate padding in a container:

* use padding on all sides
* to remove the extra margin on the first child, make a general style for all block text elements, such as headers, p, lists, that sets the margin-top:0. 
* to remove the extra margin on the last child, set the margin-bottom of the last child in the container to 0, if it is a block element.

## Specifying Box-model Properties in CSS

```css
.main-content {
  border-width: 1px;
  border-style: solid;
  border-color: black;

  margin-top: 1rem;
  margin-right: 1rem;
  margin-bottom: 1rem;
  margin-left: 1rem;

  padding-top: 0.5rem;
  padding-right: 1rem;
  padding-bottom: 0.5rem;
  padding-left: 1rem;
}
```

Measurements are specified: top right bottom left (like a clock). You can set a single value if all sides have the same value. You can set two values (top/bottom right/left), if top/bottom and left/right have the same values.

```css
/* if the values are different on all sides */
.main-content {
    margin-top:5px;
    margin-left: 15px;
    margin-bottom:10px;
    margin-right:0px;    
}

/* if the values are the same on top/bottom and left/right */
.main-content {
    margin: 5px 10px;
}

/* if the values are the same on all sides */
.main-content {
    margin: 10px;
}
```

## CSS Box-sizing

In CSS, by default, the width of the box is only the width of the content. To calculate the total width, we have to add the margin, border and padding. This can lead to unexpected results.

The solution is to use the box-sizing property to force the browser to include the margin, border and padding in the width calculation.

The setting is typically set on all elements.

```css
* {
  box-sizing: border-box;
}
```

Here's is a useful [article ](https://css-tricks.com/international-box-sizing-awareness-day/)on this topic.

## Resources

{% embed url="https://codepen.io/annechinn/full/dyNeLpQ" %}

{% embed url="https://learn.shayhowe.com/html-css/opening-the-box-model/" %}

