# Iterators

All iterators take a callback function

`.forEach()` - execute call backfunction on each element
- does not change the array and returns `undefined`
```javascript
const numbers = [1,2,3,4];
numbers.forEach(number => {
    console.log(number);
});
```

`.map()` - execute the same code on every element in an array
- returns a new array with updated elements
- similar to `forEach()` but returns a new updated array

`.filter()` - checks every element based on the criteria passed in
- the callback function must return `true` or `false` for each element
- returns a new array with elements that return `true`
```javascript
const numbers = [1,2,10, 40, 3];
const filteredArray = numbers.filter(n => {
    return n>5;
});
```

`.findIndex()` - returns find the index of the first matching element
- returns `-1` if no element found

`.reduce()` - combines the array into a single value
Takes a callback function with 2 parameters:
- `accumulator` is the value returned by the last iteration
- `currentValue` is the current element 
```javascript
const array = [1, 2, 3, 4];

const sum = array.reduce((accumulator, currentValue) => {
    return accumulator + currentValue;
});
```
