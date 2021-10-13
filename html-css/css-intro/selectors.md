# Selectors

CSS Selectors map a single CSS rule to a specific HTML element.

![https://www.internetingishard.com/html-and-css/css-selectors/](<../../.gitbook/assets/image (280).png>)

As we saw earlier, we can assign a style to all elements of a particular type. This type of selector, called a **type selector**, is less-frequently used because you typically want to be more granular in targeting the elements you want to style.

![](<../../.gitbook/assets/image (272).png>)

There are several types of CSS selectors, which offer different ways to select HTML elements. The common ones are shown in the following table.

| Selector                  | Example       | Description                                                                   |
| ------------------------- | ------------- | ----------------------------------------------------------------------------- |
| **Class selector**        | `.text { }`   | Selects all HTML elements with class `class="text"`                           |
| **Type selector**         | `p { }`       | Selects all `p` HTML elements                                                 |
| **ID selector**           | `#text { }`   | Selects all HTML elements with ID `id="text"`                                 |
| **Descendant combinator** | `article p`   | Selects all `p` HTML elements that are a descendant of an `article` element   |
| **Child combinator**      | `article > p` | Selects all `p` HTML elements that are a direct child of an `article` element |
| **Pseudo-class selector** | `p:hover { }` | Selects all `p` HTML elements that have a mouse hovering on them              |

### Class Selectors

Class selectors let you apply CSS styles to particular elements. Class selectors require two things:

* A class attribute on the HTML element(s) you want to target
* A matching **CSS class selector (.classname)** in your stylesheet.

```css
<p class="abstract">This is the abstract for an article</p>
```

```css
.abstract {  
    font-style: itaclic;
}
```

The CSS rule is only applied to the HTML elements that have the corresponding class attribute. One class selector can be applied to multiple HTML elements.

![](<../../.gitbook/assets/image (263).png>)

You will use class selectors more than any other type, as they are the most flexible and you can target multiple elements with one selector.

### **ID Selectors**

ID selectors let you apply CSS styles to one specific element. ID selectors require two things:

* An id attribute on the HTML element you want to target
* A matching **CSS id selector (#id)** in your stylesheet.

The CSS rule is only applied to the HTML element that has the corresponding id attribute.

![](<../../.gitbook/assets/image (156).png>)

Limit your use of ID selectors. They are harder to maintain, since they are tied to a single HTML element.

### Child and Descendant CSS Selectors

These two selectors are used to target descendants of a given element.

**Child Selector: parent `>` child**\
**(**targets immediate children only)

![](<../../.gitbook/assets/image (244).png>)

In the example below, only the`<a>` element directly beneath the `<section>` element matches the selector `section > a`.

![](<../../.gitbook/assets/image (266).png>)

**Descendant Selector**: **parent \`\` descendant**\
(targets any descendant)

![](<../../.gitbook/assets/image (250).png>)

In the example below, every `<a>` element beneath the `<section>` element matches the selector `section a`.

![](<../../.gitbook/assets/image (271).png>)

### Pseudo Selectors

A CSS **pseudo-class** is a keyword added to a selector that specifies a special state of the selected element(s). The most frequent use-case for pseudo-classes are for styling links based on the different states:

* **:hover** - when the mouse hovers over link
* **:link** - default style for link
* **:visited** - style after link has been clicked/visited

```css
a:hover {
    color: dodgerblue;
}
```

## Universal CSS selector

Not all browsers implement each CSS feature exactly the same. To ensure that your HTML pages look the same across browsers, you can set the default styles and then set your own default starting from a known base-line.

```
* {
    margin: 0;
    padding: 0;
}
```

### Advanced Selectors

There are more selectors, but it's better to focus on the ones you will use most often before moving on to the more advanced ones, such as combining selectors, attribute selectors, nth-child selectors and more. For the full list, consult [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors).

### Miscellaneous

#### selector naming conventions

The value for the HTML class or id attribute can be almost anything you want as long as it matches your selector in your CSS file. The standard naming convention is to use all lowercase and hyphens for spaces.

```css
.pink-jelly-image {
    border: solid 3px deeppink;
}
```

#### multiple classes can be applied to one HTML element

An HTML element can have more than one CSS class selector specified in the class attribute. In this case all of the CSS rules matching the CSS class selectors will be applied.

```css
<h2 class="article article-sports"></h2>
```

```css
.article {
    font-size: 24px;
}

.article-sports {
    color: red;
}

.article-tech {
    color: blue;
}
```

#### multiple selectors can map to a set of properties

```css
h1, h2 {
    color: red;
}
```

#### multiple properties can be applied for a selector

An HTML element can have more than one CSS class selector specified in the class attribute. In this case all of the CSS rules matching the CSS class selectors will be applied.

Each property-name property-value pair should be on a single line with a semi-colon at the end of the line.

```css
a {
   text-decoration: none;
   color:red;
   font-size:36px;
 }
```

### Resources

{% embed url="https://css-tricks.com/how-css-selectors-work/" %}

{% embed url="https://nanajeon.com/css-selectors-cheatsheet-details/" %}

{% embed url="https://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048" %}

{% embed url="https://flukeout.github.io/" %}

{% embed url="https://youtu.be/b3zIKoZxDGQ" %}
