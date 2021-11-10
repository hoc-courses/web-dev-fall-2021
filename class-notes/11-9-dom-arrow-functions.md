# 11/9 - DOM, arrow functions

### Anonymous Methods

In ES6, there is a new syntax for creating function expressions. It is a short-hand notation.

```csharp
// start with a standard function expression

const add = function(num1, num2) {
    return num1 + num2;
}

// convert to an arrow function

// 1. remove the "function" keyword
// 2. place an arrow after the parameters

const add  = (num1, num2) => {
    return num1 + num2;
}
```

So far, it's not that big of an improvement, and it does taking some getting used to the new syntax. The real advantage of the new syntax becomes clearer as you add some optional simplifications.

#### Body block curly braces are not required if there is a single statement.

Notice that the return keyword is not used when the body braces have been removed.

```csharp
// option 1
const add = (num1, num2) => {
    return num1 + num2;
}

// option 2 - remove body block braces, return keyword
const add = (num1, num2) => num1 + num2;


```

#### Parentheses are not required for a single parameter

```csharp
// option 1
const showMessage = (message) {
    alert(message);
}

// remove body block braces, return statement
const showMessage = (message) => alert(message);

// remove parameter parens

const showMessage = message => alert(message);

```

#### Summarizing Rules for Arrow Functions

* Function body block bracing is required if there is more than one statement in the function body. They can be removed if there is only a single statement;
* Parentheses surrounding the function parameters are optional if there is a single parameter.

Combining arrow functions with anonymous functions is where their usage really shines as you'll see below.

### Anonymous Functions

In the section on function expressions we demonstrated how a function can be passed as an argument to another function. In that case we first defined the function and assigned it to a variable, and then passed the variable to the function.

It is also possible, and more common, to define the function inline, using arrow functions, as I'll demonstrate below. The functions in this case are called anonymous, because they do not have a name and exist only as long as they are used in the context of the function call.

This is how we did it in the previous example. We defined a function expression, assigned it to the variable, and then passed the variable to the doSomething function.

```csharp
function doSomething(doThis) {
    doThis();
}

const sayHello = function() {
    alert("Hello");
}

doSomething(sayHello);
```

Here, we are passing in an anonymous function expression without having to bother with pre-defining it.

```csharp
function doSomething(doThis) {
    doThis();
}

doSomething(()=>alert("Hello"));
```

Anonymous functions are an extremely important concept to understand in JavaScript.  As an example of their typical usage, the JavaScript Array object has many methods that accept a function to apply to each of the elements in an array.

```csharp
// the filter method will return a new array
// containing the elements that return true
// when the passed-in function is called with the
// number as a parameter

const numArray = [1,2,3,4,5];
const result = numArray.filter((num)=>num<3);
console.log(result); // [1,2];
```

```csharp
// map applies the function to each element
// and returns an array with the new values.
const numArray = [1,2,3,4,5];
const result = numArray.map((num)=>num*2);
console.log(result); // [2,4,6,8,10];
```

#### Multi-line Complex Anonymous Functions

We discussed the rule earlier that the body braces and the return statement weren't required if the body contained a single statement only. The anonymous function can get a bit more complex as there is more involved in the body. Here is an example of how JavaScript typically looks when anonymous functions are used.

The anonymous function is the parameter to the someFunction, and it accepts two parameters. It also has the body braces and a more complex statement than the simple case we saw above when adding two numbers.

```csharp
someFunction((a1, a2) => {
  if (a1.equals(a2)) {
    doSomething(a1);
  } else {
    doSomethingElse(a2.propertyName);
  }
});
```

Sometimes it helps to pull out the anonymous function and pass it in as a variable to simplify it when you are first getting used to this format.

```csharp
const myFunc = (a1, a2) => {
  if (a1.equals(a2)) {
    doSomething(a1);
  } else {
    doSomethingElse(a2.propertyName);
  }
}

someFunction(myFunc);
```

Or, even convert it back a function expression without the arrow function notation.

```csharp
const myFunc = function(a1, a2) {
  if (a1.equals(a2)) {
    doSomething(a1);
  } else {
    doSomethingElse(a2.propertyName);
  }
}

someFunction(myFunc);
```

We're going to spend a lot of time working with anonymous arrow functions, as that is the way most JavaScript code is written and will be a skill you need to master.



### Array Methods

{% embed url="https://www.youtube.com/watch?v=R8rmfD9Y5-c" %}

### Array.forEach

The **for of** ES6 syntax largely replaces the need for forEach. Try to use it as your default loop.

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach" %}

```javascript
// 01 - Convert the following for loop to a forEach and a for of call on the array

// Create the array
const flavors = ['chocolate', 'ginger', 'carrot', 'coffee', 'walnut', 'banana'];

// Create the for loop
for (let i = 0; i < flavors.length; i++) {
  console.log('I like ' + flavors[i] + ' cake');
}

// 02 - Convert the following for loop to a forEach call on the array

const numbers = [2, 4, 6, 8];

for (let i = 0; i < numbers.length; i++) {
  console.log('The number', numbers[i], 'is at index', i);
}

// 03 - Convert the following for loop to a forEach call on the array

const evenNumbers = [2, 4, 6, 8, 10];

for (let i = 0; i < evenNumbers.length; i++) {
  evenNumbers[i] = evenNumbers[i] * 2;
}

console.log(evenNumbers);

// 04 - Log the name of each product to the page with a forEach call on the products array

let products = [{
  name: 'Running shoes',
  price: 75
}, {
  name: 'Golf shoes',
  price: 85
}, {
  name: 'Dress shoes',
  price: 95
}, {
  name: 'Walking shoes',
  price: 65
}, {
  name: 'Sandals',
  price: 55
}];
```

### Array.find

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find" %}

### Array.map

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map" %}

![](<../.gitbook/assets/image (97).png>)

{% embed url="https://www.jbakebwa.dev/posts/js-array-map.html" %}

```javascript
// 01 - Create a new array with the numbers doubled

const numbers = [13, 42, 1337];


// 02 - create a new array with the first 3 letters of each day
// hint: use the String.substring method to get the sub-string

const days = [
  'Sunday',
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday',
  'Saturday'
];


// 03 - Create a new array with the string full name of 
// each person

const people = [{
  first_name: 'CJ',
  last_name: 'R.'
}, {
  first_name: 'Brendan',
  last_name: 'Eich'
}, {
  first_name: 'Kyle',
  last_name: 'Simpson'
}, {
  first_name: 'Douglas',
  last_name: 'Crockford'
}];


// 04 - Create a new array with just the names of the animals

const animals = [{
  'name': 'cat',
  'size': 'small'
}, {
  'name': 'dog',
  'size': 'small'
}, {
  'name': 'lion',
  'size': 'medium'
}, {
  'name': 'elephant',
  'size': 'big'
}];

```

### Array.filter&#x20;

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter" %}

![](<../.gitbook/assets/image (91).png>)

```javascript
// 01 - Create a new array with only the even numbers

const numbers = [1, 3, 4, 5, 6, 7, 8, 9, 10];


// 02 - create a new array with only the days that start 
// with the letter T

const days = [
  'Sunday',
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday',
  'Saturday'
];



// 03 - Create a new array with only the people who's 
// first name is less than 4 characters long.

const people = [{
  first_name: 'CJ',
  last_name: 'R.'
}, {
  first_name: 'Brendan',
  last_name: 'Eich'
}, {
  first_name: 'Kyle',
  last_name: 'Simpson'
}, {
  first_name: 'Douglas',
  last_name: 'Crockford'
}];


// 04 - Create a new array with only the animals of size small

const animals = [{
  name: 'cat',
  size: 'small'
}, {
  name: 'dog',
  size: 'small'
}, {
  name: 'lion',
  size: 'medium'
}, {
  name: 'elephant',
  size: 'big'
}];


// 05 - create a new array with only the words with a length 
// longer than 6

const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];ZZ
```

### Zoo Project

{% embed url="https://github.com/hoc-labs/zoo-showcase" %}

#### Using Array methods to access zoo data

```javascript
// Array.find returns the first element in the list
// that returns true, or undefined if none return true

// find the object in the animals array that has the 
// name==='Faustino'
let animal = zoo.animals.find(x=>x.name==='Faustino');
console.log(animal);

// find the element in the animalTypes array that has the
// name 'lion' and get the id property value from it.
let lionTypeId = zoo.animalTypes.find(x=>x.name==='lion').id;

// Array.filter returns a new array containing only those
// elements that return true

// get an array of objects that have the property "typeId===1"
let lions = zoo.animals.filter(x=>x.typeId===lionTypeId);
console.log(lions);


// Array.map returns a new array that contains the
// same number of elements, but each element in the
// output array is what is returned from the map function.

// get an array that contains each of the lion names.
let lionNames = lions.map(x=>x.name);
console.log(lionNames);
```



### Lab - Working with data to update HTML

#### Exercise Outcome

The goal of this exercise is to learn to create event handlers and dynamically update the HTML content in the page using data describing the content. Typically the data would come from a request to the web API, but for now, we've just created data in JavaScript files that is equivalent to what would be returned from the web API calls.

The expected behavior is when the user clicks on one of the buttons at the top of the page, new HTML content will be updated in the main area to show information about the type of animal selected.

![](<../.gitbook/assets/image (94) (1).png>)

#### Data

For the exercise, there is a single data file, named zoo.js, that contains data about animals in a zoo. There a three different objects, with relationships between them. We're going to be using this data to build up the HTML content.

**Animal **- describes an individual animal.

**Animal Type **- describes a type of animal, like lion, bear, frog, etc.

**Caretaker **- describes a zoo employee responsible for a type of animal.

![](<../.gitbook/assets/image (96).png>)

```javascript
zoo = {
  caretakers: [
    {
      id: 1,
      firstName: "Nigel",
      lastName: "Nelson",
      imageURL: "https://images.unsplash.com/photo-1600180758890-6b94519a8ba6?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTYyfHxwcm9maWxlJTIwcGhvdG98ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
    },
    {
      id: 2,
      firstName: "Burl",
      lastName: "Bethea",
      imageURL: "https://images.unsplash.com/photo-1590031905406-f18a426d772d?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MjAyfHxwcm9maWxlJTIwcGhvdG98ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
    },
    {
      id: 3,
      firstName: "Ola",
      lastName: "Orloff"
    },
    // ... caretakers
  ],
  animalTypes: [
    {
      id: 1,
      name: 'lion',
      location: 'NE',
      caretakerId: 1, // Nigel
    },
    {
      id: 2,
      name: 'tiger',
      location: 'NW',
      caretakerId: 2, // Burl
    },
    {
      id: 3,
      name: 'bear',
      location: 'NE',
      caretakerId: 4, // Wilburn
    },
    // ... animal types
  ],
  animals: [
    {
      name: "Zena",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1571835782488-1793036d8887?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTI3fHxsaW9ufGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 12,
      typeId: 1, // lion
    },
    // ... lions
    {
      name: "Shu",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1562552476-8ac59b2a2e46?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fHRpZ2VyfGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
       age: 19,
      typeId: 2, // tiger
    },
    // ... tigers
    {
      name: "Hiram",
      sex: "male",
      imageURL: "https://images.unsplash.com/photo-1589656966895-2f33e7653819?ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8YmVhcnN8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 4,
      typeId: 3, // bear
    },
    // ... bears
    {
      name: "Joe",
      sex: "male",
      imageURL: "https://images.unsplash.com/photo-1598439210625-5067c578f3f6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTV8fHBlbmd1aW58ZW58MHx8MHx8&auto=format&fit=crop&w=400&q=60",
      age: 10,
      typeId: 4, // penguin
    },
    // .. penguins
    {
      name: "Neville",
      sex: "male",
      imageURL: "https://images.unsplash.com/photo-1599236449650-f2a86b592422?ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8b3R0ZXJ8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 9,
      typeId: 5, // otter
    },
    // .. otters
    {
      name: "Cathey",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1559253664-ca249d4608c6?ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8ZnJvZ3xlbnwwfHwwfHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 3,
      typeId: 6, // frog
    },
    // ... frogs
    {
      name: "Paulette",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1528158222524-d4d912d2e208?ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8c25ha2V8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 5,
      typeId: 7, // snake
    },
    // ... snakes
    {
      name: "Ilana",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1557178985-891ca9b9b01c?ixid=MnwxMjA3fDB8MHxzZWFyY2h8OXx8ZWxlcGhhbnR8ZW58MHx8MHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=60",
      age: 11,
      typeId: 8, // elephant
    },
    // .. elephants
    {
      name: "Gracia",
      sex: "female",
      imageURL: "https://images.unsplash.com/photo-1547721064-da6cfb341d50?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Z2lyYWZmZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=400&q=60",
      age: 11,
      typeId: 9, // giraffe
    },
   // ... giraffes
  ]
}
```

#### Buttons / Event Handlers

We've got a bunch of buttons that the user will click. We need to setup event handlers that will respond to those clicks by calling a function that will build the HTML for the animal type that is clicked and update the main area of the page with the new content.

```bash
<div class="buttons">
    <button id="lion-link" class="btn btn-primary">Lions</button>
    <button id="bear-link" class="btn btn-primary">Bears</button>
    <button id="tiger-link" class="btn btn-primary">Tigers</button>
    <button id="penguin-link" class="btn btn-primary">Penguins</button>
    <button id="otter-link" class="btn btn-primary">Otters</button>
    <button id="frog-link" class="btn btn-primary">Frogs</button>
    <button id="snake-link" class="btn btn-primary">Snakes</button>
    <button id="giraffe-link" class="btn btn-primary">Giraffes</button>
    <button id="elephant-link" class="btn btn-primary">Elephants</button>
 </div>
```

You register the event handler in JavaScript by calling the  addEventListener method on the DOM element and passing a function for the event handler.

```javascript
let button = document.getElementById('lion-link');

button.addEventListener("click", () => {
 // add code to handle event here ...
});
```

### Add Default Content

Right now there is no content displayed when the page first loads. Your first task is to build some content for the default view. You're going to display a showcase animal. Each animal object in the zoo data has a boolean property named "showcase". You'll need to find the animal that has a value of true (there is only one) and then display the HTML for that animal in the main content area.

Your task is to modify the initLionButton function to do the steps outlined inside to build the new content and update the main-content element.

```
```

###
