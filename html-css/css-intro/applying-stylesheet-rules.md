# Applying Stylesheet Rules

### Three Methods for Applying Styles

**1. External Stylesheets** - styles are loaded from an external stylesheet referenced in a `<link>` element. This is the **preferred method**, as all of the styles are maintained in one place and can be shared across web pages.

```markup
<head>
    <title>Jellies From the Deep</title>
    <link rel="stylesheet" href="styles.css">
</head>
```

```css
// styles.css

a {
  text-decoration: none;
  color:red;
  font-size:36px;
}

#pink-jelly {
  color: deeppink;
}

#yellow-jelly {
  color: #ff9900;
}

#orange-jelly {
  color: #ff3300;
}

li:before {
  content: '🎐'
}
```

**2. Embedded Stylesheets** - styles embedded directly in the html `<style>` element within the `<head>` section of the page. This method is discouraged because it is harder to maintain and re-use styles.

```markup
<head>
    <title>Jellies From the Deep</title>
    <style>
      a {
        text-decoration: none;
        color:red;
        font-size:36px;
      }
      #pink-jelly {
        color: deeppink;
      }

      #yellow-jelly {
        color: #ff9900;
      }

      #orange-jelly {
        color: #ff3300;
      }
      li:before {
        content: '🎐'
      }
    </style>
</head>
```

**3. Inline** - styles are specified as attributes directly on the HTML element to which you want to apply the style. This method is also discourages for the reasons explain for embedded styles.

```markup
<h2 style="color:#ff9900">Orange Jelly</h2>
```
