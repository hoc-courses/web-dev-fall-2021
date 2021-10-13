# Semantic Elements

In web design, a semantic element is an element that has intrinsic meaning, and conveys that meaning to both the browser and the developer.

Most HTML elements convey their meaning: such as a `<p>` for a paragraph or an `<h1>` for a header.  But there are two elements that were introduced early on to allow web developers to group a  section of HTML elements together for the purposes of applying styling: the \<div> and \<span> elements. These became very popular, but they are not semantic elements and make the HTML less readable for both developers and users viewing the site that rely on assistive technologies.

The `<div>` and `<span>` were a new kind of element, because they were the first to not display and content themselves. Their sole purpose is to group a sub-section of the HTML element hierarchy to apply styles to.

Below is a worst-case scenario that contains nothing but `<div>` elements, that is non-the-less legal HTML. As you can see, it requires more thought, even for the web developer, to gather at a glance what the content is and how it is organized.

```markup
<div>Pancake recipe</div>
<div>A quick and easy recipe to make pancakes!</div>
<div>Ingredients</div>
<div>
  <div>175g flour</div>
  <div>3 eggs</div>
  <div>450ml milk</div>
  <div>Sunflower oil</div>
</div>
<div>Method</div>
<div>
  <div>Add the flour, eggs, and milk to a bowl</div>
  <div>Whisk the mixture and set it aside for half an hour</div>
  <div>Heat a pan and add some sunflower oil</div>
  <div>Add some of the mix to the pan and cook for a few minutes</div>
  <div>Flip and cook the other side until done, then serve</div>
</div>
```

The latest version of HTML, HTML5, introduced several new semantic elements to provide alternatives to using the \<div> element.

Some of the most important semantic elements are those that allow us to divide our page into sections.

![](https://syllabus.codeyourfuture.io/c4fbd24f5cbf819fd867bd5b4785e795.png)

The image above shows a common layout of a web page. We can use specific semantic HTML elements for each of these sections.

* We can use a `<header>` tag for the header content
* We can use a `<footer>` tag for the footer content
* We can use a `<main>` tag for the main content of the page
* Sidebar content can go in an `<aside>` tag
* If there is a list of links, such as in the `<header>`, they can go in a `<nav>` tag
* Additionally, we can use `<article>` and `<section>` to divide these sections into more sections.

The code below demonstrates the use of semantic elements. Semantic elements often do not contain text themselves, but just wrap other elements to separate the page into semantic sections.

```markup
<body>
  <header>
    <h1>Title</h1>
    <nav>
      <a href="#">A link</a>
      <a href="#">Another link</a>
    </nav>
  </header>
  <main>
    <article>
      <section>
        <img src="http://enes.in/f.png" />
        <p>Ea commodo consequat duis autem vel eum iriure dolor in hendrerit.</p>
      </section>
      <section>
        <p>Decima eodem modo typi qui nunc nobis videntur.</p>
        <p>Tincidunt ut laoreet dolore magna, aliquam erat volutpat ut wisi enim ad minim.</p>
        <p>Id quod mazim, placerat facer possim assum typi non!</p>
        <p>Legere me lius quod ii, <a href="#">legunt saepius</a> claritas.</p>
        <p>Gothica quam nunc putamus parum claram anteposuerit litterarum formas humanitatis per seacula.</p>
      </section>
     </article>
  </main>
  <footer>
    <ul>
      <li><a href="#">Foo</a></li>
      <li><a href="#">Bar</a></li>
      <li><a href="#">Bam</a></li>
      <li><a href="#">Baz</a></li>
      <li><a href="#">Trek</a></li>
    </ul>
  </footer>
</body>
```

### Migrating from \<div> elements to semantic elements

{% hint style="success" %}
**Check for understanding**: Revisit the code we saw earlier that contained only \<div> elements and this time use more appropriate semantic elements.
{% endhint %}

```markup
<div>Pancake recipe</div>
<div>A quick and easy recipe to make pancakes!</div>
<div>Ingredients</div>
<div>
  <div>175g flour</div>
  <div>3 eggs</div>
  <div>450ml milk</div>
  <div>Sunflower oil</div>
</div>
<div>Method</div>
<div>
  <div>Add the flour, eggs, and milk to a bowl</div>
  <div>Whisk the mixture and set it aside for half an hour</div>
  <div>Heat a pan and add some sunflower oil</div>
  <div>Add some of the mix to the pan and cook for a few minutes</div>
  <div>Flip and cook the other side until done, then serve</div>
</div>
```
