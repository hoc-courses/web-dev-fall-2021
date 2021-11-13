# 11/13 - Array Methods

### Practice with Array methods

{% embed url="https://github.com/hoc-labs/hoc-practice" %}

#### Using Article Data to redo the news site:

{% embed url="https://github.com/SJJCoding/Group-newssite" %}

### Tables

Today we're going to learn about tables. They are used for storing tabular data. Basically the equivalent of a spreadsheet.&#x20;

Historically, before the div element and grid/flex were introduced, web developers often used tables to define the structure of their web pages. Now that these other techniques exists, it is a bad practice to use tables for this purpose. They should only be used to store tabular data.

{% embed url="https://learn.shayhowe.com/html-css/organizing-data-with-tables/" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics" %}

Here's an example of a table for our zoo exercise. It has four columns, and a row for each type of animal.

![](<../.gitbook/assets/image (101) (1).png>)

#### Table element

The table element is the top-level HTML element required to define a table.&#x20;

```markup
<table>
</table>
```

The table element has two child components.

#### Column headers

```markup
 <thead>
      <th>Type</th>
      <th>Location</th>
      <th>Number</th>
      <th>Residents</th>
  </thead>
```

#### Rows

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

The thead and tbody elements are not required, but good practice, as the web browser uses them to enable scrolling of the table body independent of the header.

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

#### Dynamically building a summary table for our zoo data.

First, add a new button to the end of the list of buttons at the top of the page and give it an id="summary-link".

```markup
<button id="summary-link" class="btn btn-primary">Summary</button>
```

Next, create a function to initialize the summary button with a click event handler.

From within the click handler code, call a new function named showSummaryTable.

The showSummaryTable function should retrieve the div with the id="main-content" and the update the element's HTML with the new HTML content you are going to build for the summary table.

```javascript
function showSummaryTable() {
  let element = document.getElementById('main-content');
  element.innerHTML = getHTMLForSummaryTable();
}

function initSummaryButton() {
  let button = document.getElementById("summary-link");
  button.addEventListener("click", ()=> {
    showSummaryTable();
  });
}

initSummaryButton();
```

The next step is to build out the HTML for the summary table. The basic structure of the table is pretty straightforward. I've added some bootstrap styles to the table element to make the table look nice. If you remove them you can see the before/after to see what they add.

```javascript
function getHTMLForSummaryTable() {

  let rowsHTML = "";

  let html = `
    <table class="table table-striped">
      <thead>
        <th>Type</th>
        <th>Location</th>
        <th>Number</th>
        <th>Residents</th>
      </thead>
      <tbody>
        ${rowsHTML}
      </tbody>
    </table>
  `;

  return html;
}
```

The next step is to build the HTML for the rows. For each animal type, we will call a new function, named getHTMLForSummaryTableRow, that will build up the HTML for a single row in the table.

For the first step, we'll only build the content for the first three columns and leave the last column empty.

```javascript
function getHTMLForSummaryTableRow(animalType) {

  let animals = zoo.animals.filter(animal=>animal.typeId===animalType.id);
  
  return `
    <tr>
      <td>${animalType.name}</td>
      <td>${animalType.location}</td>
      <td>${animals.length}</td>
      <td></td>
    </tr>
    `;
}

function getHTMLForSummaryTable() {

  let rowsHTML = zoo.animalTypes
      .map(animalType =>getHTMLForSummaryTableRow(animalType))
      .join(" ");

  let html = `
    <table class="table table-striped">
      <thead>
        <th>Type</th>
        <th>Location</th>
        <th>Number</th>
        <th>Residents</th>
      </thead>
      <tbody>
        ${rowsHTML}
      </tbody>
    </table>
  `;

  return html;
}
```

![](<../.gitbook/assets/image (102) (1).png>)

Last, we'll build the HTML content for the last column. It's a bit more complicated, because we want to build up a list of the animals (name, age, sex).

```javascript

function getHTMLForSummaryTableRow(animalType) {

  let animals = zoo.animals.filter(animal=>animal.typeId===animalType.id);

    let animalsOfTypeSummaryString = animals.map(animal=>{
      return `
        <strong>${animal.name}</strong> (${animal.sex}, ${animal.age})
      `;
    }).join(" ");

    return `
    <tr>
      <td>${animalType.name}</td>
      <td>${animalType.location}</td>
      <td>${animals.length}</td>
      <td>${animalsOfTypeSummaryString}</td>
    </tr>
    `;
}
```

###
