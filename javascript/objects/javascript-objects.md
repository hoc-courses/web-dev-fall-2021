# JavaScript Objects

## Basic Data Types - text, numbers, boolean

In most programming languages there are three basic data types: **strings** (text), **numbers **(integers and decimal) and **boolean **(true/false).  When your program needs to store data, it must create a variable to store data based on one of these basic types.

For example, in our draw polygon block we created earlier, we store two pieces of data about a shape: 

* the number of sides (number)
* the length of each side (number)

![](<../../.gitbook/assets/image (95).png>)

This was a simple script, and those two variables were all that was needed to accomplish the task of drawing a polygon. But what happens as the complexity of what we are building increases?  Computer applications are complex and need to model processes that involve real world objects, such as movies, products, shopping carts, users, hotels, cars, family trees, etc... The list is endless. How do we represent the data we need to store for these more complex objects?

## Composite Data Types - objects

We build objects (composite data types built from combining basic data types) to model the real world things that we want to represent in our programs.

In the previous topic ([Modelling Real World Objects](broken-reference)), a hotel and car object were introduced. This same process can be used to describe any real-world object.

In addition to storing data associated with these objects we're modelling, we typically also want to associate functionality with the object.  So an object has two components:

* **properties**: data
* **methods**: functionality

### The Snap! Pen object

Let's take the example of the Snap! program itself and the software developers that built that program. What are the objects that they are modelling? There's the window, palette, blocks, pen, stage, etc. Let's look at the pen more closely. To represent the pen in the Snap! program, what are some examples of the type of data it needs to store and the functionality that operate on that data?

#### Pen Data/Properties

| Variable              | Data Type |
| --------------------- | --------- |
| Color                 | numeric   |
| Size (line thickness) | numeric   |
| Draw State (up/down)  | boolean   |

#### Pen Methods

| Method   | Description                                                                   |
| -------- | ----------------------------------------------------------------------------- |
| Clear    | Erase any drawings on the stage                                               |
| Pen Up   | Change the state of the pen so that it will not draw when the sprite is moved |
| Pen Down | Change the state of the pen so that it will draw when the sprite is moved     |
| Fill     | Fills a containing polygon at the current position of the sprite              |

So a Pen has a number of basic properties that store the data about the pen being used by the user and a set of methods that allow the user to perform actions with the pen.

### A JavaScript Example

In JavaScript, you can define an object by enumerating a comma-separated set of property name/value pairs within an enclosing block.

```javascript
let product = {
    id: 1,
    title: 'Mens Cotton Jacket',
    price: 55.99,
    description: 'great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors',
    category: 'men\'s clothing',
    image: 'https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg'
}
```

And you can store a collection of objects in an array.

```javascript
let products = [
{
    id: 1,
    title: 'Mens Cotton Jacket',
    price: 55.99,
    description: 'great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors',
    category: 'men\'s clothing',
    image: 'https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg'
},
{
    id: 2,
    title: "WD 4TB Gaming Drive Works with Playstation 4 Portable External Hard Drive",
    price: 114,
    description: "Expand your PS4 gaming experience, Play anywhere Fast and easy, setup Sleek design with high capacity, 3-year manufacturer's limited warranty",
    category: "electronics",
    image: "https://fakestoreapi.com/img/61mtL65D4cL._AC_SX679_.jpg"
}
]
```

## Nested Object Structure

Again, in the real world, objects are more often complex structures, containing nested objects within them. For example, a Shopping Cart object might contain a collection of Product objects, each of which  contains its own properties, such as title, description, price, availability, etc. And the cart needs to manage adding/removing products from the cart, purchasing the products, etc.

Programming languages provide features that allow programmers to define these complex objects. Here's an example in JavaScript.

#### Product Object

```javascript
let jacket = {
    id: 1,
    title: 'Mens Cotton Jacket',
    price: 55.99,
    description: 'great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors',
    category: 'men\'s clothing',
    image: 'https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg'
}

let playstation = {
    id: 2,
    title: "WD 4TB Gaming Drive Works with Playstation 4 Portable External Hard Drive",
    price: 114,
    description: "Expand your PS4 gaming experience, Play anywhere Fast and easy, setup Sleek design with high capacity, 3-year manufacturer's limited warranty",
    category: "electronics",
    image: "https://fakestoreapi.com/img/61mtL65D4cL._AC_SX679_.jpg"
}

const products = [jacket, playstation];
```

#### Shopping Cart Object

```javascript
const shoppingCart = {
    products: [],
    user: null,
    
    initialize: function(user) {}
    addItem: function (product) {}
    removeItem: function(product) {}
    checkOut: function() {}
}

shoppingCart.initialize(user1);
shoppingCart.addItem(products[0]);
shoppingCart.addItem(products[1]);
shoppingCart.checkOut();
```

## Resources

{% embed url="https://www.mikedane.com/web-development/javascript/real-world-objects/" %}
