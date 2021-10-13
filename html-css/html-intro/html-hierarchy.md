# HTML Hierarchy

HTML tags are arranged in a hierarchy. This is sometimes called **nesting** tags or creating an HTML **tree**. Between the opening `<header>` tag and the closing `</header>` tag there are two other tags. We call these **child** tags, because they have a parent-child relationship.

```markup
<div>
  <header>
    <h1>Title</h1>
    <nav>
      <a href="#">A link</a>
      <a href="#">Another link</a>
    </nav>
  </header>
  <main>
    <img src="http://enes.in/f.png" />
    <p>Ea commodo consequat duis autem vel eum iriure dolor in hendrerit.</p>
    <p>Decima eodem modo typi qui nunc nobis videntur.</p>
    <p>Tincidunt ut laoreet dolore magna, aliquam erat volutpat ut wisi enim ad minim.</p>
    <p>Id quod mazim, placerat facer possim assum typi non!</p>
    <p>Legere me lius quod ii, <a href="#">legunt saepius</a> claritas.</p>
    <p>Gothica quam nunc putamus parum claram anteposuerit litterarum formas humanitatis per seacula.</p>
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
</div>
```

The tree structure can be seen more easily below.

![](<../../.gitbook/assets/image (287).png>)
