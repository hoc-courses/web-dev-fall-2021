# Container Elements

So far we have been working with basic HTML elements whose purpose is to display some content. We have seen that these elements flow down the page, with some variation based on whether the element is a block or inline element.

A more typical web page, has a lot of these basic HTML elements, but as you'll notice in the screen capture below, they don't all flow down the page. The page has a layout which can be broken down into distinct functional areas, and each area has a group of basic HTML elements.

![](<../../.gitbook/assets/image (238).png>)

This layout cannot be achieved with HTML alone. It requires a combination of a new type of HTML element and CSS layout styles.

Below is a mapping of the basic HTML elements as they are displayed with no CSS layout styles applied (flows down the page), and the corresponding area in the styled view (layout)

![](<../../.gitbook/assets/image (222) (1).png>)

## Generic Container Elements - div, span

In the early versions of HTML, CSS didn't exist, and there wasn't a way to change the default flow of the document on the left to the layout on the right.

In 1996-1997, two important improvements were made. The first version of CSS was introduced and and two new HTML elements, `<div>` and `<span>` were added. The \<div> element allowed web developers to wrap a group of HTML elements in the document and then apply styles to that sub-section of the HTML document tree. The \<span> element allowed web developers to wrap some text to apply a style to a region of text.

The `<div>` and `<span>` were a new kind of element, because they were the first to not display and content themselves. Their sole purpose is to select a sub-section of the HTML element hierarchy to apply styles to.

The `<div>` element, in combination with a style, allowed web developers to specify styles for specific sub-sections of the page.

While this was a big improvement, the styles that CSS provided at the time for positioning element in a layout similar to the one above were limited and web developers resorted to hacks to achieve their layout goals. For example, the `<table>` element (think of a grid) was introduced at the same time, and it became popular to use it to layout the overall structure of the page, and then place the desired content in the different table cells.

The problem with this approach is that HTML is meant to be used semantically. HTML elements are supposed to describe the content they display. Using a `<table>` element to display non-tabular data, or nesting `<div>` elements was confusing for screen readers, hence limiting accessibility and it made the HTML code more difficult to read.

## Semantic Container Elements

> Semantic HTML is the use of HTML markup to reinforce the semantics, or **meaning**, of the information in webpages and web applications rather than merely to define its presentation or look. [Wikipedia](https://en.wikipedia.org/wiki/Semantic_HTML).

With the release of HTML5 in 2008, a new set of semantic HTML elements was introduced. These elements are similar to the `<div>` and `<span>` elements, in that they are generic container elements with no content of their own, but they have the advantage that they give meaning to the content they contain.

Now, instead of using a `<div>` element to organize the large chunks of content on the page, we have a new set of semantic HTML elements that can be used instead, and they better describe the purpose of the content within the element.

![](<../../.gitbook/assets/image (4).png>)

{% hint style="info" %}
Use these sectioning HTML elements in every website you build. This lets screen reader users jump to these sections of the website quickly.
{% endhint %}

## Revisit our Previous Layout

Now we can take a closer look at what's in the HTML of the page we described above. You can see that there are semantic HTML elements surrounding each of the major sections of the page.

![](<../../.gitbook/assets/image (219) (1).png>)

And here's the corresponding HTML. I have left out the details within the semantic elements so it's easier to see the overall layout. With these container elements, it is now possible to specify that a particular element, such as the \<aside>, should be positioned in a specific location within the page.

```markup
<body>
  <header>
    <nav></nav>
    <form></form>
  </header>
  <nav></nav>
  <main>
    <article></article>
  </main>
  <aside>
    <section></section>
    <section></section>
  </aside>
  <footer></footer>
</body>
```

## The Default Flow is Still Down

One thing to keep in mind, is that a style is applied to a particular element in the overall HTML element hierarchy. Setting a layout style on a particular element will allow the **immediate children of that element to have a particular layout**.

For example, all of the immediately children of the second row (left `<nav>` section, middle `<main>` section, and right `<aside>` section are styled to flow horizontally instead of the default flow down.

But the descendants of those children will flow down by default within the containing rectangular box. Any descendants that you want to deviate from that default flow would have to have an additional style applied at that level in the element hierarchy.

For example, in the screen capture below, the top-level rows can be seen outlined in red, with the corresponding number down the right edge: #1, #2 and #3. Each row is following the next, so they are flowing down, and there was no additional positioning necessary.

Likewise, within each of the three sub-sections of #2 row, the content is naturally flowing down.

But within rows #1 and #3, the flow is horizontal, and so the display was changed override the default and have the child elements flow horizontally (this can be achieved using the flex display property).

![](<../../.gitbook/assets/image (237).png>)

## Visualizing the HTML Element Tree

There is a really helpful Google Chrome Extension for viewing an HTML document as a tree. It helps to visualize how an HTML document is just a hierarchy of HTML components in a tree structure.

{% embed url="https://chrome.google.com/webstore/detail/html-tree-generator/dlbbmhhaadfnbbdnjalilhdakfmiffeg?hl=en-US" %}

![](<../../.gitbook/assets/image (219).png>)

### Main Element Tree

```markup
<main>
  <article>
    <h1>Main article heading</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quae sunt igitur communia vobis cum antiquis, iis sic utamur quasi concessis; Nihil acciderat ei, quod nollet, nisi quod anulum, quo delectabatur, in mari abiecerat. Unum est sine dolore esse, alterum cum voluptate. Laboro autem non sine causa; Theophrasti igitur, inquit, tibi liber ille placet de beata vita? Nihil opus est exemplis hoc facere longius. Duo Reges constructio interrete. Graecum enim hunc versum nostis omnes Suavis laborum est praeteritorum memoria. Haec et tu ita posuisti, et verba vestra sunt.</p>

    <h2>Article secondary heading</h2>
    <p>Nos commodius agimus. A mene tu? Tantum dico, magis fuisse vestrum agere Epicuri diem natalem, quam illius testamento cavere ut ageretur. Tenesne igitur, inquam, Hieronymus Rhodius quid dicat esse summum bonum, quo putet omnia referri oportere? Nihilo beatiorem esse Metellum quam Regulum. Sed quanta sit alias, nunc tantum possitne esse tanta. Philosophi autem in suis lectulis plerumque moriuntur. Esse enim, nisi eris, non potes.</p>
    <p>Sunt enim quasi prima elementa naturae, quibus ubertas orationis adhiberi vix potest, nec equidem eam cogito consectari. Id Sextilius factum negabat. Quorum sine causa fieri nihil putandum est. Quae autem natura suae primae institutionis oblita est?</p>
  </article>
</main>
```

![](<../../.gitbook/assets/image (218).png>)

You can see that a layout/style could be put on the `<main>` HTML element to position it in the overall page layout, but that within the `<article>` element, all of the child elements will flow down following the default flow within a containing rectangular box.

## Resources

{% embed url="https://www.freecodecamp.org/news/semantic-html5-elements/" %}
