# Variable Scope

## Block Scoped Variables
`const` and `let` are block scoped variables. 
They are only accessible in their block. <br>
For example, printing `statusMsg` will result in an error.
```javascript
if(isLoggedIn == true) {
    const statusMsg = 'user is logged in';
}
console.log(statusMsg); // results in error
```

