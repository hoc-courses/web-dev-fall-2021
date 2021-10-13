# Web Browser Objects

![](<../../.gitbook/assets/image (92).png>)

#### Data/Properties

| Name                                                                    | Description                                                                                                        | Data Type       |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | --------------- |
| [outerHeight](https://www.w3schools.com/jsref/prop_win_outerheight.asp) | Returns the height of the browser window, including toolbars/scrollbars                                            | numeric         |
| [outerWidth](https://www.w3schools.com/jsref/prop_win_outerheight.asp)  | Returns the width of the browser window, including toolbars/scrollbars                                             | numeric         |
| [innerHeight](https://www.w3schools.com/jsref/prop_win_innerheight.asp) | Returns the height of the window's content area (viewport) including scrollbars                                    | numeric         |
| [innerWidth](https://www.w3schools.com/jsref/prop_win_innerheight.asp)  | Returns the width of a window's content area (viewport) including scrollbars                                       | numeric         |
| [name](https://www.w3schools.com/jsref/prop_win_name.asp)               | Returns the name of the window                                                                                     | string          |
| [location](https://www.w3schools.com/jsref/obj_location.asp)            | Returns the Location object for the window                                                                         | Location Object |
| [history](https://www.w3schools.com/jsref/obj_history.asp)              | Returns the History object for the window                                                                          | History Object  |
| [document](https://www.w3schools.com/jsref/dom_obj_document.asp)        | Returns the Document object for the window                                                                         | Document Object |
| [console](https://www.w3schools.com/jsref/obj_console.asp)              | Returns a reference to the Console object, which provides methods for logging information to the browser's console | Console Object  |

#### Methods

| Method                                                         | Description                        |
| -------------------------------------------------------------- | ---------------------------------- |
| [alert](https://www.w3schools.com/jsref/met_win_alert.asp)     | display an alert dialog            |
| [confirm](https://www.w3schools.com/jsref/met_win_confirm.asp) | display a dialog with a question   |
| [prompt](https://www.w3schools.com/jsref/met_win_prompt.asp)   | prompt the user to input some text |

## Location Object

The [location ](https://www.w3schools.com/jsref/obj_location.asp)object contains information about the current URL and is accessed through the window.location property.

One of  the most important properties on the location object is the [href ](https://www.w3schools.com/jsref/prop_loc_href.asp)property. Your programs can set this property to a new value, which will load a new document in the browser.

```javascript
window.location = 'http://www.google.com'
```

## History Object

The [history ](https://www.w3schools.com/jsref/obj_history.asp)object contains the URLs visited by the user (within a browser window).

The history object is part of the window object and is accessed through the window.history property. It has methods for loading pages in the browser based on the history of where the user has navigated.

| [back](https://www.w3schools.com/jsref/met_his_back.asp)       | Loads the previous URL in the history list |
| -------------------------------------------------------------- | ------------------------------------------ |
| [forward](https://www.w3schools.com/jsref/met_his_forward.asp) | Loads the next URL in the history list     |
| [go](https://www.w3schools.com/jsref/met_his_go.asp)           | Loads a specific URL from the history list |

## Console Object

The [console ](https://www.w3schools.com/jsref/obj_console.asp)object provides access to the browser's debugging console. One of the most important methods to learn to use early on is the [log ](https://www.w3schools.com/jsref/met_console_log.asp)method. Calling this method will display the contents you passed to the method on the Console within the browser's debugging console.

```javascript
const answer = someComplexCalculation();
// log to check during development/debugging
console.log("The answer", answer);
```

## Document Object

The [document ](https://www.w3schools.com/jsref/dom_obj_document.asp)is the actual page loaded into the window. This object is referred to as the Document Object Model (DOM) and is an object that you will use heavily in your JavaScript programs. It is a complex object that models the entire HTML document loaded into the web browser.

Think about what kind of structure you would need to model an HTML document. The document consists of elements in a tree structure and each element has a collection of attributes. Additionally, each element has a relationship with its parent and child elements.

The browser application uses this model to render the document on the screen. It also properties and methods that are available for your code to use to manipulate the current document after it has been rendered by the browser.

For example, your code can use methods on the DOM to get a reference to an element in the DOM, change its text content, apply new styles to it, or even add or remove elements in the tree. This is the basis of how your JavaScript code adds interactivity to a web page.

Below are some of the methods that are commonly used. As you can see, the Document object has nested objects, such as Element and Attribute, for storing the data associated with each "node" in the HTML document tree.

#### Methods

| Name                                                                                  | Description                                                                                           |
| ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| [getElementById](https://www.w3schools.com/jsref/met_document_getelementbyid.asp)     | Returns the element that has the ID attribute with the specified value                                |
| [createElement](https://www.w3schools.com/jsref/met_document_createelement.asp)       | Creates an Element node                                                                               |
| [createAttribute](https://www.w3schools.com/jsref/met_document_createattribute.asp)   | Creates an Attribute node                                                                             |
| [addEventListener](https://www.w3schools.com/jsref/met_document_addeventlistener.asp) | Attaches an event handler to the document, such as responding to button clicks, mouse movements, etc. |

## Accessing Window Properties

Because the window properties that access these other objects are used so frequently, the JavaScript runtime environment allows you to access them directly, without having to go through the window object.

In the code below, the two statements are equivalent.

```javascript
window.console.log(window.location.href);

console.log(location.href);
```
