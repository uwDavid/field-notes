# Objects

Like arrays, objects are also `mutable`. 
Even when objects are declared as `const` the properties can be changed. It is only the `reference` to the object that cannot be changed. 

## For...in Loop
`for...in` loop can be used to iterate over the keys of an object
```javascript
let mobile = {
    brand: 'Samsung',
    model: 'Galaxy Note 9',
}

for (let key in mobile) {
    console.log(`${key}: ${mobile[key]}`);
}
```

## Delete operator
Use the `delete` operator to delete a property from an object
```javascript
const person {
    firstName: "David",
    lastName: "Blain",
    hobby: "knitting",
}

delete person.hobby;
```
## JavaScript Object Methods 
Object methods are defined using arrow functions or `shorthand` method 
```javascript
const engine = {
    // shorthand method
    start(adverb) {
        console.log(`The engine starts ${adverb}`);
    }

    // arrow function
    sputter: () => {
        console.log("The engine sputters...");
    }
}
```
## Object Destructuring
Shorthand syntax to extract object properties into specific variables
```javascript
const rubikCube = {
    possiblePermutations: '43,252,003,274 billion',
    invented: '1974',
    largestCube: '17x17x17'
};
const {possiblePermutations, invented, largestCube} = rubikCube;
```

## `this` Keyword
`this` refers to a method's calling object. It can be used to access properties belonging to that object.
Example to access the cat's name: 
```javascript
const cat = {
    name: "NuoMi",
    age: 8,
    whatName() {
        return this.name
    }
}
console.log(cat.whatName());
```

If a function is defined inside an object, `this` refers to the object itself.
If a funciton is defined outside of an object, `this` will refer to the global object (`window` in a browser, `global` in Node.js). <br> 

### Arrow Function `this` Scope
arrow functions **do NOT** have their own `this` context. 
Thus, they are a poor choice for writing object methods. 
```javascript
const obj = {
    data: 'abc', 
    loggerA: ()=> { console.log(this.data);}, // this doesn't work
    loggerB() {console.log(this.data);},
}
```

## Getters and Setters
JavaScript object properties are not private or protected. 
We use getters and setters to implement more restrictive interactions. 
Typically, the internal value is initated with an underscore `_`.
```javascript
const myCat = {
    _name: "NuoMi",
    get name() {
        return this._name;
    },
    set name(newName) {
        this._name = newName;
    }
}
// invoke getter
console.log(myCat.name);
// invoke setter
myCat.name='Star';
```

Getters and setters can also implement additional logic before performing changes. 
