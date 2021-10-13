# Global CSS Vars

You can define variables in CSS so that they can be applied repeatedly throughout a stylesheet.

The format for defining a CSS variable is to specify the variable within a selector with the following syntax: **--variable name: value**.

```css
body {
  --cyan: hsl(179, 62%, 43%);
  --cyan-lighter: hsl(179, 47%, 52%);
  --yellow: hsl(71, 73%, 54%);
  --lightGrey: hsl(204, 43%, 93%);
  --blueGrey: hsl(218, 22%, 67%);
  --white: hsl(69, 69%, 100%);
}
```

Then, anywhere you want to use that variable you can do the following: **var(--variable-name), **and the value of the variable will be substituted.

```css
h1 {
  color: var(--cyan);
  margin-bottom:30px;
}

h2 {
  color: var(--yellow);
  font-size: 16px;
}

h3 {
  margin-bottom: 16px;
  color:white;
}

.card {
  box-shadow: 0 4px 12px 0 var(--lightGrey);
}
```
