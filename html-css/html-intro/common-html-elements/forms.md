# Forms

## What is a Form?

An HTML form allows a user to enter data that will be sent to a server for processing. The `<form>` element is the container for one or more `<input>` elements that specify the input fields and the types of input data that will be collected and included in the form submission.

The following attributes are associated with sending the data to the server:

### form action and method attributes

The purpose of the **action** attribute is to specify the URL to which the form data will be sent when the user submits the form. The **method** attribute specifies how the data will be sent. This method value typically would be a POST request, which indicates that the input data will be included in the request body.

### input name attribute

The **name** attribute is the form field name that will be used when the data is included in the request body.

```markup
<form action="https://formspree.io/f/xpzkzqpn" method="POST">
    <input name="firstName" type="text" />
    <input name="lastName" type="text" />
    <input type="submit" value="Submit"/>
</form>
```

![](<../../../.gitbook/assets/image (39).png>)

## Form Input Data

The essential elements contained within the `<form>` element are `<input>` elements. The `<input>` elements tell the web browser what the data elements are included on the form and the type attribute describes the type of data the element contains.

HTML supports many different input data types for the `<input>` element. The web browser will present the appropriate UI control and in some cases there is built-in validation based on the data type specified. The full list of data types supported by HTML5 can be[ found here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input). The input type is a client-side attribute to assist in collecting the data and is not sent to with the form data sent to the server for processing.

The only form data that is sent to the server is the names of the input fields and their associated values.

![](<../../../.gitbook/assets/image (30).png>)

![](<../../../.gitbook/assets/image (6).png>)

## Form Styling

In the HTML code sample above, I omitted the elements that I added for the field labels and the CSS to make everything look nice. HTML forms need a lot of CSS to properly position and style their elements. For example, here is what is displayed in the browser with just the minimal HTML from the code block above. There are just two `<input>` elements of type text, for the first and last name, and a single `<input>` element of type submit, which will be rendered as a button with default styling.

![](<../../../.gitbook/assets/image (5).png>)

## Adding Input Field Labels

The `<label>` element is used to associate a label with a form input element. To associate the two, the label element must have the **for attribute** set to the value of the **id attribute** on the associated input element.

{% hint style="info" %}
The **id attribute** is necessary to associate a label, whereas the **name attribute** is necessary to indicate the field name to the POST request.
{% endhint %}

```markup
<label for="firstName">First Name:</label>
<input id="firstName" name="firstName" type="text" />
<label for="lastname">Last Name:</label>
<input id="lastName" name="lastName" type="text" />
```

![](<../../../.gitbook/assets/image (10).png>)

## Adding Input Field Block Display

By default, the `<input>` and `<label>` elements are both inline elements, which is causing the entire form to be displayed on a single line. A common technique to get each input field to be in its own row is to wrap each with a `<div>` element (which is a block element) and add a margin on the bottom of each.

![](<../../../.gitbook/assets/image (152).png>)

```markup
<form action="https://formspree.io/f/xpzkzqpn" method="POST">
    <div>
        <label for="firstName">First Name:</label>
        <input id="firstName" name="firstName" type="text" />
    </div>
    <div>
        <label for="lastname">Last Name:</label>
        <input id="lastName" name="lastName" type="text" />
    </div>
    <input type="submit" value="Submit"/>
    </form>
```

```css
form > div {
    margin-bottom:20px;
}
```

## Additional Input Types

Below are a few of the common input types that are available. As you can see, the browser has provided type-specific input controls to gather and validate the data.

![](<../../../.gitbook/assets/image (73).png>)

## Styling

A big part of form development is the additional styling that is required to make the form look presentable, as the default styling by the web browser is pretty limited. Additionally, validation of the data is necessary. This functionality is often a selling point of adopting a front-end framework, such as Bootstrap, which provides extensive support for forms.



### Resources

* [Demo Repo](https://github.com/hoc-demos/form-action)
