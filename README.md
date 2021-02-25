# web-dev-primer

## Declaring Variables
In JavaScript, you can have a variable that changes value (mutable) or one that does not change value (immutable). For mutable variables, you use let and for immutable variables, you use const.
```js
const myName = "Rees";

let myAge = 19;
```
There is also the `var` keyword, but there is hardly occasion to use it when you can use `const` or `let`, so just don't use it.

**Further Reading:** [MDN Article on the let keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#examples)

JavaScript is dynamically typed, which means that a variable with the same name can change the type of data at any moment during the program's runtime. With some other languages, you have to specify the type when you create the variable, but JavaScript is much more flexible in this regard.
```js
let myVariable = 5; // Number
myVariable = "blah"; // String
myVariable = false; // Boolean
myVariable = [1, 2, 3]; // Array
```

A more advanced type of JavaScript variables are something called objects. Objects are instances of classes which contain properties and/or functions designated to make certain tasks easier and safer through co-locating data and data actions.
```js
const today = new Date();
```

A special type of object in JavaScript is the array. Arrays are ordered lists of values, of any type.
```js
let myArray = ["Hello", 45, true];
```
