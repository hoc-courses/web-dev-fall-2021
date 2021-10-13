# Grid

The grid layout consists of parent container referred as _grid container_ and its **immediate children** which are called _grid items_.

## The Container

To create a grid container, just set the display property to grid. All of its immediate children will now be considered grid items.

```css
body {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr; 
    grid-template-rows: 1fr 2fr 1fr;
    grid-template-areas: 
      "green green green"
      "yellow red blue"
      "orange orange blue";
  }

  #green {
    grid-area: green;
  }

  #yellow {
    grid-area: yellow;
  }

  #orange {
    grid-area: orange;
  }

  #red {
    grid-area: red;
  }

  #blue {
    grid-area: blue;
  }
```

Grids are not only for the top-level layout. They can be created to layout sub-sections of the page, as in the yellow and red section content.

```css
#yellow ul, #red ul {
    display: grid;
    grid-template-columns: 1fr 1fr; 
    grid-template-rows: 1fr 1fr;
 }
```

![](<../../.gitbook/assets/image (81).png>)

```markup
 <body>
    <section id="green">
      <p>GREEN</p>
    </section>
    <section id="yellow">
      <p>YELLOW</p>
      <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
      </ul>
    </section>
    <section id="orange">
      <p>ORANGE</p>
    </section>
    <section id="red">
      <p>RED</p>
      <ul>
        <li>A</li>
        <li>B</li>
        <li>C</li>
        <li>D</li>
      </ul>
    </section>
    <section id="blue">
      <p>BLUE</p>
    </section>
  </body>
```

## grid-template-columns, grid-template-rows

Defines the columns and rows of the grid with a space-separated list of values. The values can be a length, a percentage, or a fraction of the free space in the grid (using the fr unit).

## grid-template-areas

Defines a grid template by referencing the names of the grid areas which are specified with the grid-area property. Repeating the name of a grid area causes the content to span those cells. A period signifies an empty cell. The syntax itself provides a visualization of the structure of the grid.

## column-gap, row-gap, grid-gap

Specifies the size of the grid lines. You can think of it like setting the width of the gutters between the columns/rows.

## Resources

{% embed url="https://css-tricks.com/snippets/css/complete-guide-grid/" %}

{% embed url="https://scrimba.com/learn/cssgrid/template-areas-css-grid-tutorial-c7Jqdfa" %}
