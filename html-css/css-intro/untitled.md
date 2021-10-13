# The Cascade

## Browser Defaults

In addition to your own styles, the web browser provides a set of default styles.

The link below is for the default styles applied by the Chrome browser.

{% embed url="https://source.chromium.org/chromium/chromium/src/+/master:third_party/blink/renderer/core/html/resources/html.css" %}

Examples of some of the styles it sets include:

* display set to block (h1-h6, p, hr)
* font-size, font-weight for headings (h1-h6)
* list spacing, icon type for bullets at different indentation levels
* padding and margins - body has margin of 8px.

Below is a screen capture with no overrides except for colors to make it easier to see the margins and block elements. You can see that the font-size is different between the paragraph and the h1 and there is a margin around the content in the body. These are the default styles set in the user-agent stylesheet.

```css
/* Sample of Chrome default styles */

body {
    display: block;
    margin: 8px;
}

p {
    display: block;
}

h1 {
    display: block;
    font-size: 2em;
    font-weight: bold;
}
```

![](<../../.gitbook/assets/image (251).png>)

## Processing Order Matters - The Last Rule Wins

The web browser loads its default styles first, and then loads any styles defined by the web page author. If the the rule is repeated, the last one encountered will be used. For example, your own stylesheet could specify the color property of the `<h1>` element should be red, which would override the value defined by the web browser.

The same would be true if you re-defined the same style later in the same stylesheet file or in a stylesheet file that was loaded after the initial definition.

## CSS Property Inheritance

### Some Properties are Inherited

Inheritance is when some CSS properties are passed down the inheritance tree, so that descendant element inherit the style specified in an ancestor element. Background color is an example of an inherited property. Inherited properties can be overridden on a descendant element.

In the image on the right, the background color and text transform properties specified in the `<body>` element have been overridden in the `<h1>` and `<p>` descendent elements.

![](<../../.gitbook/assets/image (260).png>)

**Text-related properties are typically inherited**. For example, font-family, font-size, font-style, font-weight, letter-spacing, line-height, text-align, text-indent, text-transform, text color and word-spacing.

**Some list styles are inherited.** For example, list-style-image, list-style-position, list-style-type.

**Background colors are inherited.** background-color.

### Some Properties are not Inherited

It's pretty intuitive which styles are inherited and which are not. Inheritance of CSS styles is there to make the web developer's job easier, so it is applied for those elements where it makes sense.

Styles that you wouldn't want to be inherited are ones like borders, padding, margins.

For example, in the screen capture below the paragraph element has been set to have a dark cyan border. There is a span element within the paragraph, but it is not inheriting the border style. If the border style was inherited it would look like the screen capture below, which is obviously not what we would want.

![](<../../.gitbook/assets/image (256).png>)

## CSS Specificity

There can be multiple selectors, each setting the same properties, that target the same element. For example, a selector for a font property could be set on the body element, as well as a paragraph element.

When this happens, the browser needs to apply a set of rules to determine which selector will be applied to the element.

This is known as the specificity of the selector, or how strongly that selector binds to the element. The specificity, is given below from top (highest specificity) to bottom (lowest specificity):

* **inline** style (style attribute on element)
* **id** attribute on element
* **class** attribute on element
* **type** selector in stylesheet

![](<../../.gitbook/assets/image (247).png>)

```markup
<ul>
    <li><a style="color:dodgerblue" href="">style="color:dodgerblue"</a></li>
    <li><a id="id-link" href="">id="id-link"</a></li>
    <li><a class="class-links" href="">class="class-links"</a></li>
    <li><a href="">Nothing on element</a></li>
</ul>
```

```css
a {
    color:black;
    font-weight:800;
    font-size:40px;
}

#id-link {
    color:green;
}

.class-links {
    color:hotpink;
}
```

## Summary - Cascading Style Sheets

As you have learned, there are many different origins for a style (web browser defaults, inline, style element, and external CSS files) and there are many different rules for how to resolve which style should be applied when there are multiple rules targeting the same element and style. The algorithm the web browser uses to apply the correct styles is what makes up the "Cascade" in Cascading Style Sheets.

## Resources

{% embed url="https://wattenberger.com/blog/css-cascade" %}
