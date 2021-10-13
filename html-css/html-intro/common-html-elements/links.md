# Anchor

## Anchor Element - \<a>

The anchor element is primarily used for hyper-links, usually referred to as links, to other HTML documents. There are different types of document hyper-links.

### Attributes

| Attribute  | Description                                                                                                                                                  |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|            | A link within or between documents                                                                                                                           |
| **href**   | The value of the href attribute can be the URL of another page within the site, or a remote site. Or it can be the id of an element within the current page. |
| **target** | The value of "\_blank" opens the linked to page in a new window.                                                                                             |
| **title**  | The browser may show this as a tooltip when the user hovers over the link.                                                                                   |

### ****

### **Different Types of Anchors**

**External Pages (Absolute URL):** The URL assigned to the `href` attribute is an absolute URL, or the entire path to the remote resource. These are used to navigate to an external site.

{% hint style="info" %}
Set the attribute target="\_blank" to have the target web page launch in a new browser tab instead of replacing the contents of the current tab.
{% endhint %}

```markup
<a href="http://www.google.com" target="_blank">Google</a>
```

**Internal Site Pages (Relative URL):** The URL assigned to the `href` attribute is a relative URL, meaning that is is a path relative to the current web page that contains the hyper-link. It is used to link to another page within your site.

```markup
<!-- .. indicates one level up -->
<a href="../page1.html">Page 1</a>

<!-- same folder -->
<a href="page2.html">Page 2</a>

<!-- down into subDir folder -->
<a href="subDir/page3.html">Page 3</a>
```

**Internal Page Reference (within the same page)**: The anchor element can specify a special `href` syntax to indicate that the _\*\*_hyper-link is to a different location in the current document. The target location must be an element with an attribute named id that uniquely identifies the element. The anchor's `href` attribute value must be of the form "#\[id-of-target-element]".

```markup
<a href="#section1">Section 1</a>

<!-- Lots of other stuff here -->
<section id="section1">
    <p>This is section 1</p>
</section>
```
