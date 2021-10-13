# CSS Stylesheet Rules

To change the style of an element you must target the element using a CSS Rule.

![](<../../.gitbook/assets/image (289).png>)

A CSS rule is made up of **selectors**, **properties**, and **values**.

* A **selector** describes which HTML elements to style
  * `h1` is the **selector**
* A **property** is the specific style to apply
  * `font-size` is the **property**
* A **value** is the value for the property
  * `1.5rem` is the **value**
* A **declaration** is the combination of the property and value
  * `font-size: 1.5rem;` is the **declaration**
* A **rule** is the combination of the selector and its declarations
  * `h1 { font-size: 1.5rem; }` is the **rule**

{% hint style="success" %}
**Check for understanding**. In the CSS code below, which parts are the rules, selectors, properties, values, and declarations?
{% endhint %}

```css
h1, h2, h3, h4, h5, h6, p {
  color: #333333;
  margin-bottom: 2rem;
}

.box {
  border: 1px solid #333;
}
```
