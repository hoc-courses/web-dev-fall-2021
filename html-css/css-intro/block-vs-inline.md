# Block vs Inline

## CSS Display Property

The CSS display property has four values that are used to determine how much horizontal and vertical space an element takes up.

* **block**: take up the entire line, unless they are empty. headings, paragraphs, lists are examples of elements that have their display property set to block by default. 
* **inline**: take up width of their content only. images, links, spans are examples of elements that have their display property set to inline by default.
* **inline-block**: like inline, except can specify width and height. this is used for special cases.
* **none**: the element is hidden from view.

The image below has three different sections, each demonstrating the different display property values and how it effects the space the element takes up.

![](<../../.gitbook/assets/image (35).png>)

## display: inline

Elements only occupy the horizontal and vertical space occupied by its own content. The element sits "inline" with the rest of the text.

Examples include: `<span>`, `<b>`, `<img>`, `<a>` ([full list](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements))

![](<../../.gitbook/assets/image (128).png>)

An inline element will accept margin and padding, but the element still sits inline as you might expect. Margin and padding will only push other elements horizontally away, not vertically.

![](<../../.gitbook/assets/image (144).png>)

## display: inline-block

An element set to inline-block is very similar to inline in that it will set inline with the natural flow of text. The difference is that you are able to set a width and height which will be respected.

![](<../../.gitbook/assets/image (70).png>)

## display: block

The web browser's default stylesheet sets the default value for the display property to block for a number of elements, including paragraphs, lists, div, or headings. Block level elements do not sit inline. By default (without setting a width) they take up as much horizontal space as they can. By default their height equals 0. It will fill vertically around content.

Examples: `<p>`, `<ul>`, `<li>`, `<h1>`, `<div>` ([full list](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements))

![](<../../.gitbook/assets/image (107).png>)

## display: none

Hides the element from view. The element is still there, but not visible to the user.

![](<../../.gitbook/assets/image (98).png>)

### Inline Elements on Their Own Line

To re-enforce the your understanding of how inline and block elements behave in relation to each other, here is one more example.

The screen capture below shows how an `<img>` element, which we saw above is an inline element, behaves when it is positioned before, at the beginning and in the middle of a paragraph element.

The difference is not due to the `img` element, but rather that the fact that the `p` element is a block element and a block element always starts on a new line.

**Example #1**: the `img` element is following a`h4` element and before an `p` element (both of which are block elements), so it ends up being on its own line, since the block elements neighbors must be one their own lines.

![](<../../.gitbook/assets/image (241).png>)

```markup
<h4>Image placed before paragraph</h4>
<img src="images/photo.png"/>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat.  
</p>
```

**Example #2**: the `img` element is embedded as the first item in the `p` element, so it only has a single neighbor, which is the text following it within the paragraph. Since text is an inline element, the text following the img element starts immediately after the `img` element.

![](<../../.gitbook/assets/image (214).png>)

```markup
<h4>Image placed at the beginning of paragraph</h4>
<p>
    <img src="images/photo.png"/>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat. 
    Lorem ipsum dolor sit amet. 
</p>
```

**Example #3**: the `img` element is again embedded in the paragraph, and its neighboring elements are the text before and after it. Since they are all inline, the `img` element takes up the minimal amount of horizontal space in the text.

![](<../../.gitbook/assets/image (216).png>)

```markup
<h4>Image placed in the middle of paragraph</h4>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniamLorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam, <img src="images/photo.png"/>
    quis nostrud exercitation ullamco 
    laboris nisi ut aliquip ex ea commodo consequat.
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
    Ut enim ad minim veniam 
</p>
```
