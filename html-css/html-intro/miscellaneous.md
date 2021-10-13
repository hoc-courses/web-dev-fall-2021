# Miscellaneous

#### Adding comments in HTML

Anything that starts with **\<!--** and ends with **-->** will be ignored by the browser. This is useful for documenting your code and making notes to yourself, or for commenting out HTML that you are debugging.

```markup
<body>
    <!-- This will be ignored -->
    <p>Lorem ipsum dolor sit amet, consectetur 
        sed do eiusmod tempor</p>
    <!-- <p>Lorem ipsum dolor sit amet, consect, 
        sed do eiusmod tempor</p> -->  
</body>
```

#### White-space in HTML is ignored

You can add as much white-space as you want within the text of an element, and it will be ignored.

![](<../../.gitbook/assets/image (275).png>)

#### Browsers are Forgiving

While there are ways to enforce HTML code to follow the rules, browsers have always attempted to gracefully handle syntax errors in HTML. The HTML that currently exists on the web is full of such errors, so it is not possible to change this behavior now without breaking lots of websites.

It's up to you to carefully review your HTML code to make sure the syntax is correct, otherwise you'll get unexpected results as the web browser attempts to correct errors.
