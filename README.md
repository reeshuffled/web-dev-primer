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

## Numeric Operators
There are many types of operators in JavaScript, but we will only focus on two main ones, arithmetic operators and assignment operators.

The arithmetic operators look just like the ones you would use in your math class.
```js
const four = 2 + 2; // Addition
const two = 5 - 3; // Subtraction
const eight = 4 * 2; // Multiplication
const three = 6 / 2; // Division
const one = 5 % 2; // Modulus (Remainder)
```
You have already seen the most basic assignment operator which is just the equals sign, but you can also combine the equals sign with an arithmetic operator to utilize different assignment operators that help save the amount of typing you have to do.
```js
let count = 5;

count += 4;
count -= 3;
count *= 1;
count /= 2;
```
If you are just adding or subtracting one from a variable, there are additional shorthand operators to help you.
```js
let count = 0;

count++;
count--;
```

## Array Operations
Array elements can be accessed using the square-brackets syntax. Array indices start at zero in JavaScript.
```js
let myArray = ["Hello", 45, true];

myArray[1]; // = 45
```

In JavaScript, arrays are mutable and of variable length.
```js
myArray.push(5.0); // add as last element
someVar = myArray.pop(); // Remove last element

myArray.length; // = 3
```
