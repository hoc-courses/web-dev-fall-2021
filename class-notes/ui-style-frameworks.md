# UI Style Frameworks

{% embed url="https://getbootstrap.com" %}

{% embed url="https://material.io/design" %}

### Styling &#x20;

For this exercise, we're going to use Bootstrap to help make our job of styling the form easier.

{% embed url="https://getbootstrap.com/docs/4.0/components/forms" %}

### Building the Zoo Form

Our goal for this exercise is to create a form that allows a customer to purchase tickets.

![](<../.gitbook/assets/image (94).png>)

After the data is entered and the Submit button is clicked, the form will be processed and the following table will be displayed.

![](<../.gitbook/assets/image (104).png>)



**BootStrap Components**

* form-group
* select/option - drop down list
* button

### Step 1 - No Coupon, just Total Up the Cost for all Tickets

First, we're going to process the form with just the three select boxes that ask how many tickets for the different types. Then, we're going to display the total on the screen.

### Processing the Form

The first step is to setup an event handler to respond to the click event on the submit button for the form.

```javascript
function processForm() {
  // todo
}

function setupFormEventHandler() {
  
  // when user clicks "Submit" on form
  let submitBtn = document.getElementById("submit-btn");
  submitBtn.addEventListener("click", (event)=> {
    processForm(event);
  });
}

setupFormEventHandler();
```

Next, we need to collect the data from the form elements. After getting the form element from the DOM, there are properties on the form object for accessing the elements. The form element will have a property called "elements" which will contain a property for each form field that we have added.

For example, we have a select form element with a name="adults".&#x20;

```html
<form id="form">
          <h1>Purchase Tickets</h1>
     
          <div class="form-group">
            <label for="adults" class="control-label">Number of Adults</label>
            <select name="adults" required class="form-control">
              <option value="0" selected>0</option>
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4">4</option>
              <option value="5">5</option>
            </select>
          </div>
```

To get the value of that form element from the DOM form element, we can access it like this (we use parseInt to convert a string value to an integer.

```
let form = document.getElementById("form");

let numAdults = parseInt(form.elements.adults.value);

```

So, well need to do this for each form element value that we are collecting.

Next, we want to do some processing of the data.

### Print a simple total

We want to calculate the total cost for the tickets. I've added some new data to the zoo data for the prices.  We'll use this in our calculations and then, as a first step, just print out the total to the screen.

```javascript
zoo = {
  prices: { 
    adult: 49.99, 
    senior: 24.99, 
    child: 20.99 
  },
  // other data
}
```

![](<../.gitbook/assets/image (103).png>)



### Build a table to contain more detail.

### Coupon Code

Add one additional field on the form that collects a coupon code, which will be used to calculate a discount on the total price. If the coupon code is added, then the total price will include a 10% discount.

![](<../.gitbook/assets/image (101).png>)



The processForm function will need to be modified in the following ways:

* get the value from the coupon form element
* check to see if the coupon was entered, and if it matches the word "ZOOPASS", then apply a 10% discount to the totalCost.
* Add an additional row in the table, just below the last row that give the total. This row has the following HTML.

The output should look like this:

![](<../.gitbook/assets/image (102).png>)

