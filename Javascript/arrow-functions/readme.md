# Arrow Functions 

## Function Declaration
```javascript
// name function
function add(num1, num2) {
    return num1 + num2; 
}
// anonymous function 
const add = (num1, num2) {
    return num1+num2;
}
```

## Examples

```javascript
// Arrow function with 2 parameters
const sum = (firstParam, secondParam) => {
    return firstParam + secondParam;
}
console.log(sum(2,4));

// Arrow function with no param
const printHello = () => {
    console.log("Hello");
}
printHello();

// Arrow function with single param
const checkWeight = weight => {
    console.log(`weight is: ${weight} kg.`);
}
checkWeight(25);
```
Notes: 
- arrow functions with a single paramter do not require `()`

### Concise Function 
Arrow functions with a single expression can skip the `return` keyword.
```javascript
const multiply = (a, b) => a*b; 
console.log(multiply(3,5));
```
