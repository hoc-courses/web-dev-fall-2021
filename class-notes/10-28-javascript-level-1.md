# 10/28 - JavaScript Level 1

### Focused on arrays and loops

Iterated through an array of numbers to:

#### Find the sum of the numbers in an array

```javascript
const numbers = [1,2,3,4,5];

let total = 0;
for (let i=0; i<numbers.length; ++i) {
    total+=numbers[i];
}
console.log("total", total);

```

#### Find the largest number in an array of numbers

```javascript
const numbers = [1,2,3,4,5];

let max = 0;
for (let i=0; i<numbers.length; ++i) {
    if (numbers[i]>max) {
        max = numbers[i];
    }
}

console.log("max", max);
```
