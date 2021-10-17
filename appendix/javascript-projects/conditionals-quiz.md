# Conditionals Quiz

#### What will the code block log to the console?

```
let runTime = 35;
let runDistance = 3.5;
 
if (runTime <= 30 && runDistance > 3.5) {
  console.log("You're super fast!");
} else if (runTime >= 30 && runDistance <= 3) {
  console.log("You're not making your pace!");
} else if (runTime > 30 || runDistance > 3) {
  console.log("Nice workout!"); 
} else {
  console.log("Keep on running!");
}
```

#### What will the code block log to the console?

```
let weather = "spring";
let clothingChoice = "";
 
if (weather === "spring") {
  clothingChoice = "Put on rain boots.";
} else if (weather === "summer") {
  clothingChoice = "Make sure to take your sunscreen.";
} else if (weather === "fall") {
  clothingChoice = "Wear a light jacket.";
} else if (weather === 'winter') {
  clothingChoice = "Wear a heavy coat.";
} else {
  console.log('Invalid weather type.');
};
console.log(clothingChoice);
```

#### Translate this to JavaScript

Log “Bear!” to console if `isFurry` is `true` and `weight` is over `100` pounds.

```
// Some code
```

![](<../../.gitbook/assets/image (93).png>)

#### What will the code block log to the console?

```
let groceryItem = "apple";
 
switch (groceryItem) {
  case "tomato":
    console.log("Tomatoes are $0.49");
    break;
  case "lime":
    console.log("Limes are $1.49");
    break;
  case "papaya":
    console.log("Papayas are $1.29");
    break;
  default:
    console.log("Invalid item");
    break;
}
```

#### How would you properly refactor this code block using the ternary operator?

```
if (walkSignal === 'Walk') {
    console.log('You may walk!'); 
} else {   
    console.log('Do not walk!');
}
```
