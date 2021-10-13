# Tables

Tables are used for storing tabular data. Basically the equivalent of a spreadsheet.

Historically, before the div element and grid/flex were introduced, web developers often used tables to define the structure of their web pages. Now that these other techniques exists, it is a bad practice to use tables for this purpose,. They should only be used to store tabular data.

{% embed url="https://learn.shayhowe.com/html-css/organizing-data-with-tables/" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics" %}

Here's an example of a table for the animals in a zoo. It has four columns, and a row for each type of animal.

![](<../../../.gitbook/assets/image (46).png>)

## Table element

The `<table>`element is the top-level HTML element required to define a table.

```markup
<table>
</table>
```

The `<table>`element has two child components.

## Column headers

The `<thead>` element is used for specifying the column headers.

```markup
 <thead>
      <th>Type</th>
      <th>Location</th>
      <th>Number</th>
      <th>Residents</th>
  </thead>
```

## Rows

The `<tbody>` element surrounds all of the rows, and then for each row, there is a `<tr>`, with `<td>` elements for each column in the row.

```markup
 <tbody>
    <tr>
      <td>Lion</td>
      <td>NE</td>
      <td>4</td>
      <td>Dee, Zena, Faustino, Maxwell</td>
    </tr>
</tbody>
```

The `<thead>`and `<tbody>`elements are not required, but good practice, as the web browser uses them to enable scrolling of the table body independent of the header.

Here's a complete table element with one row of data.

```markup
  <table>
    <thead>
      <th>Type</th>
      <th>Location</th>
      <th>Number</th>
      <th>Residents</th>
    </thead>
    <tbody>
        <tr>
          <td>Lion</td>
          <td>NE</td>
          <td>4</td>
          <td>Dee, Zena, Faustino, Maxwell</td>
        </tr>
    </tbody>
  </table>
```

{% hint style="success" %}
**Check for understanding**. Create a table to describe your family members, with columns list the name, sex, and age of each.
{% endhint %}
