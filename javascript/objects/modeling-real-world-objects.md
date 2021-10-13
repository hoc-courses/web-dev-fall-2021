# Modeling Real World Objects

_Excerpt from Jon Duckett's JavaScript & jQuery_

####

#### COMPUTERS CREATE MODELS OF THE WORLD USING DATA

Here is a model of a hotel, along with some model trees, model people, and model cars. To a human, it is clear what kind of real-world object each one represents.

![](<../../.gitbook/assets/image (94).png>)

A computer has no predefined concept of what a hotel or car is. It does not know what they are used for. Your laptop or phone will not have a favorite brand of car, nor will it know what star rating your hotel is.

So how do we use computers to create hotel booking apps, or video games where players can race a car? The answer is that programmers create a very different kind of model, especially for computers.

Programmers make these models using data. That is not as strange or as scary as it sounds because the data is all the computer needs in order to follow the instructions you give it to carry out its tasks.

#### OBJECTS & PROPERTIES

If you could not see the picture of the hotel and cars, the data in the information boxes alone would still tell you a lot about this scene.

**OBJECTS (THINGS)**

In computer programming, each physical thing in the world can be represented as an **object**. There are two different **types** of objects here: a hotel and a car.

Programmers might say that there is one **instance** of the hotel object, and two **instances** of the car object.

Each object can have its own:

* Properties
* Events
* Methods

Together they create a working model of that object.

**PROPERTIES (CHARACTERISTICS)**

Both of the cars share common characteristics. In fact, all cars have a make, a color, and engine size. You could even determine their current speed. Programmers call these characteristics the **properties** of an object.

Each property has a **name** and a **value**, and each of these name/value pairs tells you something about each individual instance of the object.

The most obvious property of this hotel is its name. The value for that property is Quay. You can tell the number of rooms the hotel has by looking at the value next to the rooms property.

The idea of name/value pairs is used in both HTML and CSS. In HTML, an attribute is like a property; different attributes have different names, and each attribute can have a value. Similarly, in CSS you can change the color of a heading by creating a rule that gives the color property a specific value, or you can change the typeface it is written in by giving the font-family property a specific value. Name/value pairs are used a lot in programming.

**HOTEL OBJECT**

The hotel object uses property names and values to tell you about this particular hotel, such as the hotel's name, its rating, the number of rooms it has, and how many of these are booked. You can also tell whether or not this hotel has certain facilities.

**CAR OBJECTS**

The car objects both share the same properties, but each one has different values for those properties. They tell you the make of car, what speed each car is currently traveling at, what color it is, and what type of fuel it requires.

![](<../../.gitbook/assets/image (104).png>)

#### EVENTS

In the real world, people interact with objects. These interactions can change the values of the properties in these objects.

**WHAT IS AN EVENT?**

There are common ways in which people interact with each type of object. For example, in a car a driver will typically use at least two pedals. The car has been designed to respond differently when the driver interacts with each of the different pedals:

* The accelerator makes the car go faster
* The brake slows it down

Similarly, programs are designed to do different things when users interact with the computer in different ways. For example, clicking on a contact link on a web page could bring up a contact form, and entering text into a search box may automatically trigger the search functionality.

An **event** is the computer's way of sticking up its hand to say, “Hey, this just happened!”

**WHAT DOES AN EVENT DO?**

Programmers choose which events they respond to. When a specific event happens, that event can be used to trigger a specific section of the code.

Scripts often use different events to trigger different types of functionality.

So a script will state which events the programmer wants to respond to, and what part of the script should be run when each of those events occur.

**HOTEL OBJECT EVENTS**

A hotel will regularly have bookings for rooms. Each time a room is reserved, an event called **book **can be used to trigger code that will increase the value of the bookings property. Likewise, a **cancel **event can trigger code that decreases the value of the bookings property.

**CAR OBJECT EVENTS**

A driver will accelerate and brake throughout any car journey. An **accelerate event** can trigger code to increase the value of the `currentSpeed `property and a **brake event** can trigger code to decrease it. You will learn about the code that responds to the events and changes these properties on the next page.

![](<../../.gitbook/assets/image (96).png>)

#### METHODS

Methods represent things people need to do with objects. They can retrieve or update the values of an object's properties.

**WHAT IS A METHOD?**

Methods typically represent how people (or other things) interact with an object in the real world.

They are like questions and instructions that:

* Tell you something about that object (using information stored in its properties)
* Change the value of one or more of that object's properties

**WHAT DOES A METHOD DO?**

The code for a method can contain lots of instructions that together represent one task.

When you use a method, you do not always need to know how it achieves its task; you just need to know how to ask the question and how to interpret any answers it gives you.

**HOTEL OBJECT METHODS**

Hotels will commonly be asked if any rooms are free. To answer this question, a method can be written that subtracts the number of bookings from the total number of rooms. Methods can also be used to increase and decrease the value of the bookings property when rooms are booked or cancelled.

**CAR OBJECT METHODS**

The value of the `currentSpeed `property needs to go up and down as the driver accelerates and brakes. The code to increase or decrease the value of the `currentSpeed `property could be written in a method, and that method could be called **`changeSpeed`**.

![](<../../.gitbook/assets/image (100).png>)

#### PUTTING IT ALL TOGETHER

Computers use data to create models of things in the real world. The events, methods, and properties of an object all relate to each other: Events can trigger methods, and methods can retrieve or update an object's properties.

![](<../../.gitbook/assets/image (103).png>)

**HOTEL OBJECT**

1\. When a reservation is made, the book event fires.

2\. The book event triggers the `makeBooking()` method, which increases the value of the bookings property.

3\. The value of the bookings property is changed to reflect how many rooms the hotel has available.

**CAR OBJECTS**

1\. As a driver speeds up, the accelerate event fires.

2\. The accelerate event calls the `changeSpeed()` method, which in turn increases the value of the `currentSpeed `property.

3\. The value of the `currentSpeed` property reflects how fast the car is traveling.

#### WEB BROWSERS ARE PROGRAMS BUILT USING OBJECTS

You have seen how data can be used to create a model of a hotel or a car. Web browsers create similar models of the web page they are showing and of the browser window that the page is being shown in.

**WINDOW OBJECT**

In the image below you can see a model of a computer with a browser open on the screen.

The browser represents each window or tab using a window object. The location property of the window object will tell you the URL of the current page.

**DOCUMENT OBJECT**

The current web page loaded into each window is modelled using a document object.

The title property of the document object tells you what is between the opening `<title>` and closing `</title>` tag for that web page, and the `lastModified `property of the document object tells you the date this page was last updated.

![](<../../.gitbook/assets/image (88).png>)

#### THE DOCUMENT OBJECT REPRESENTS AN HTML PAGE

Using the document object, you can access and change what content users see on the page and respond to how they interact with it.

Like other objects that represent real-world things, the document object has:

**PROPERTIES**

Properties describe characteristics of the current web page (such as the title of the page).

**METHODS**

Methods perform tasks associated with the document currently loaded in the browser (such as getting information from a specified element or adding new content).

**EVENTS**

You can respond to events, such as a user clicking or tapping on an element.

Because all major web browsers implement the document object in the same way, the people who create the browsers have already:

* Implemented properties that you can access to find out about the current page in the browser
* Written methods that achieve some common tasks that you are likely to want to do with an HTML page

So you will be learning how to work with this object. In fact, the document object is just one of a set of objects that all major browsers support. When the browser creates a model of a web page, it not only creates a document object, but it also creates a new object for each element on the page. Together these objects are described in the **Document Object Model**, which you will meet in Chapter 5.

#### HOW A BROWSER SEES A WEB PAGE

In order to understand how you can change the content of an HTML page using JavaScript, you need to know how a browser interprets the HTML code and applies styling to it.

**1: RECEIVE A PAGE AS HTML CODE**

Each page on a website can be seen as a separate **document**. So, the web consists of many sites, each made up of one or more documents.

```markup
<!DOCTYPE html>
<html>
  <head>
    <title>Constructive &amp; Co.</title>
    <link rel=“stylesheet” href=“css/styles.css” />
  </head>
  <body>
    <h1>Constructive &amp; Co.</h1>
    <p>For all orders and inquiries please call
      <em>555-3344</em>
    </p>
  </body>
</html>
```

**2: CREATES A IN-MEMORY MODEL OF THE PAGE**

The model shown below is a representation of one very basic page. Its structure is reminiscent of a family tree. At the top of the model is a **document object**, which represents the whole document.

Beneath the **document** object each box is called a **node**. Each of these nodes is another object. This example features three types of nodes representing elements, text within the elements, and attribute.

![](<../../.gitbook/assets/image (91).png>)

**3: USE A RENDERING ENGINE TO SHOW THE PAGE ON SCREEN**

If there is no CSS, the rendering engine will apply default styles to HTML elements. However, the HTML code for this example links to a CSS style sheet, so the browser requests that file and displays the page accordingly.

When the browser receives CSS rules, the rendering engine processes them and applies each rule to its corresponding elements. This is how the browser positions the elements in the correct place, with the right colors, fonts, and so on.

![](<../../.gitbook/assets/image (102).png>)

**4: USE JAVASCRIPT TO INTERACT WITH THE IN-MEMORY PAGE MODEL**

When you use JavaScript in the browser, there is a part of the browser that is called an JavaScript Engine.

When the browser encounters a script element, it passes the JavaScript code to the JavaScript Engine to process. The JavaScript Engine will read each line of code

In an **interpreted programming language**, like JavaScript, each line of code is translated one-by-one as the script is run.

### SUMMARY

*   Computers create models of the world using data.

    The models use objects to represent physical things. Objects can have: 

    * **properties **that tell us about the object
    * **methods **that perform tasks using the properties of that object
    * **events **which are triggered when a user interacts with the computer.
* Programmers can write code to say “When this event occurs, run that code.”
* Web browsers use HTML markup to create a model of the web page. Each element creates its own node (which is a kind of object).
* To make web pages interactive, you write code that uses the browser's model of the web page.
