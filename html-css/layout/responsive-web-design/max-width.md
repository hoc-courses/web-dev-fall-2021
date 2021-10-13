# max-width

This is typically referred to as the **measure** in typographic circles and typographers recommend that a paragraph have a width of around 75 characters (1 character \~ 8 pixels) for legibility reasons. Anything longer than that becomes difficult to read and causes unnecessary strain on the eyes because of the distance the eye has to travel left-to-right and back again.

It is best to set the max-width on a container element so that it can be applied across paragraphs.

```markup
<div class="container">
  <p>This is where our text goes.</p>
</div>
```

```css
p {
  font-size: 18px;
  line-height: 24px;
}

.container {
  max-width: 600px;
}
```

#### Example

See how the paragraph text of th**is** [article ](https://medium.com/weekly-webtips/react-ecosystem-in-2021-87da221e5f71)width is limited and makes it easier to read.

Here is another example [codepen](https://codepen.io/robinrendle/pen/jdQXwd).
