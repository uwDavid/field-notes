# Higher Order Functions

## Functions: First-Class Objects
Javascript functions are first-class objects: 
- Functions have built-in properties and methods such as: `name` property and `.toString()` method
- Properties and methods can be added to them
- They can be passed as arguments, or returned from other functions
- They can be assigned to variables, array elements, and other objects

## Assign Function to a Variable
```javascript
const firstFunction = () => {
    console.log("First function declared")
}

// Assign this function to a variable
const another = firstFunction;

// Call the function
another();

// Display the original function using .name()
console.log(another.name);
```

## Function as Paramter
**Higher order function** is a function that: 
- accepts functions as parameters
- returns a function
- or both

**Callback functions** are functions that get passed in as parameters.

```javascript
const higherOrderFunc = param => {
    param();
    return `Just invoked ${param.name} as a callback funciton!`;
}

const anotherFunc = () => {
    return `callback func invoked by higher-order function`;
}

higherOrderFunc(anotherFunc);
```

### Quick Example of Higher Order Function
```javascript
const addTwo = num => {
    return num+2;
}

const checkAddTwo = (func, val) => {
    let checkA = val + 2;
    let checkB = func(val);

    return checkA===checkB;
}

console.log(checkAddTwo(addTwo, 3))
```
