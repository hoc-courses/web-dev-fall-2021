# HTML Elements/Attributes

### HTML Element Syntax

![](<../../.gitbook/assets/image (7).png>)

#### HTML Elements

HTML consists of **markup elements** (opening and closing tags) that **wrap content** to mark it for specific formatting.

#### HTML Attributes

Markup elements can contain **attributes** (name/value pairs) **on the opening tag** to specify additional information.

#### An Example

```markup
<a href="https://jellyfish.html">Jelly Fish Facts</a>
```

* A **tag** is the HTML element name enclosed in angle brackets
  * `<a>` is the **opening tag**
  * `</a>` is the **closing tag**
* An **attribute** comes after the HTML element name within the angle brackets
  * `href="https://jellyfish.html"` is the **attribute**
  * `href` is the **attribute name**
  * `http://jellyfish.html` is the **attribute value**
* The **content** is the part of the code in between the opening and closing tags
  * `Jelly Fish Facts` is the **content**

###

### Self-closing elements

Some elements do not contain any content between the opening and closing tags. In this case, the element is called a **self-closing tag** and can be simplified by having just a single tag with the "/" symbol at the end.

The image element is an example of a self-closing tag and can be written as follows.

```markup
<img src="logo.jpg" alt="logo"/>
```

For a full list of self-closing elements, see the [MDN Documentation](https://developer.mozilla.org/en-US/docs/Glossary/Empty_element).



{% hint style="success" %}
**Test for Understanding**: In the code sample below:

* Which elements have content?
* Which elements do not have content?
* How can you tell the difference?
* What elements have attributes?
* Which element(s) are self-closing?
{% endhint %}

```markup
<article>
  <h1>Learning HTML</h1>
  <p>Get to know the HTML basics.</p>
  <a href="http://html5rocks.com">Read Article</a>
  <img src="images/photo.jpg"/>
</article>
```
