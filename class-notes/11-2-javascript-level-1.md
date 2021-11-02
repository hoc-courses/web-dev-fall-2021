# 11/2 - JavaScript Level 1

### Review of Looping Basics

#### for of&#x20;

This should really be your default choice. Use for or while if you need the index.

```javascript
const numbers = [1,2,3,4,5];

let total = 0;
for (let next of numbers) {
    total+=next;
}
console.log("total", total);
```

#### for&#x20;

```javascript
const numbers = [1,2,3,4,5];

let total = 0;
for (let i=0; i<numbers.length; ++i) {
    total+=numbers[i];
}
console.log("total", total);
```

#### while&#x20;

A while loop wouldn't be the best choice for looping through an array like this. It is better for problems such as looping until a condition is met that you don't know ahead of time. For example, until the user stops entering a response. It is also useful when you need to move through the array from both directions simultaneously, such as if you wanted to reverse the elements in the array. You would have an index set to the start and the end, and increment them both as you moved each toward the middle, swapping the elements at the start and end indices on each iteration.

```javascript
const numbers = [1,2,3,4,5];

let total = 0;
while (i<numbers.length) {
    total+=numbers[i];
    i++; // i=i+1;
}
console.log("total", total);
```

### Continue with JavaScript Workshop - Arrays Exercises

{% embed url="https://github.com/hackreactor/javascript_301/tree/master/3-array-iteration" %}

### Practice with arrays

```
let array = [-2, -1, 0, 5, 2, 4, 4, 5, 6];
// modify the array such that it equals
// console.log(array); => [0, 1, 2, 3, 4, 5]
```

**Mini-linter**: [https://classroom.github.com/a/c5VGfUCl](https://classroom.github.com/a/c5VGfUCl)

**js-lc-candidate-test**: [https://classroom.github.com/a/X334CqRx](https://classroom.github.com/a/X334CqRx)
