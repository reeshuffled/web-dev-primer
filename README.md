# web-dev-primer
A modern guide of the useful parts of HTML, CSS, and JS to get quickly started with web development.

# JavaScript
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
### Objects
A more advanced type of JavaScript variables are something called objects. They are just like "dictionaries" or "maps" in other languages: an unordered collection of key-value pairs.
```js
let myObj = { key1: "Hello", key2: "World" };
```

You can get object attributes with the bracket or dot syntax.
```js
const myKey = "key1";

// Bracket syntax (especially helpful when you have a variable containing the key name
myObj["key1"]; // = "Hello"
myObj[myKey]; // = "Hello"

// ... or using the dot syntax, provided the key is a valid identifier.
myObj.key2; // = "World"
```
### Arrays
A special type of object in JavaScript is the array. Arrays are ordered lists of values, of any type.
```js
let myArray = ["Hello", 45, true];
```
Array elements can be accessed using the square-brackets syntax. Array indices start at zero in JavaScript.
```js
let myArray = ["Hello", 45, true];

myArray[1]; // = 45
```

In JavaScript, arrays are mutable and of variable length.
```js
myArray.push(5.0); // Add as last element
myArray.pop(); // Remove last element

myArray.length; // = 3
```
**Further Reading:** [MDN Article on the Array object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

## Operators
There are many types of operators in JavaScript, but we will only focus on three main ones, arithmetic operators, assignment operators, and comparison operators.

### Arithmetic Operators
The arithmetic operators look just like the ones you would use in your math class.
```js
const four = 2 + 2; // Addition
const two = 5 - 3; // Subtraction
const eight = 4 * 2; // Multiplication
const three = 6 / 2; // Division
const one = 5 % 2; // Modulus (Remainder)
```

### Assignment Operators
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

### Comparison Operators
Comparison operators are for comparing two values.
```js
const num = 4;

// Equality is ==
1 == 1; // = true
2 == 1; // = false
num == 3 // = false

// Inequality is !=
1 != 1; // = false
2 != 1; // = true
num != 3 // = true

// More comparisons
1 < 10; // = true
1 > 10; // = false
2 <= 2; // = true
2 >= 2; // = true
```
**Further Reading:** [MDN Article on Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)

## Conditionals
If, else-if, and else statements are just as you'd find them in any other C-style language.
```js
let count = 1;
if (count == 2){
    // evaluated if count is 2
} 
else if (count == 3){
    // evaluated if count is 3
} 
else {
    // evaluated if it's neither 2 nor 3
}
```
**Advanced Reading**: [MDN Article on the Ternary Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)

## Loops
While, do-while, and for loops are just as you'd find them in other C-style languages as well.
```js
while (true){
    // An infinite loop!
}

// Do-while loops are like while loops, except they always run at least once.
let input;
do {
    input = prompt("What is your name?");
} while (input != "");

// The for loop follows a familiar format:
// initialization; continue condition; iteration
for (let i = 0; i < 3; i++){
    // will run 3 times
}

// The for-in loop allows for the iteration of properties (keys) of an object
const myObj = { key1: "Hello", key2: "World" };
for (let key in myObj) {
  console.log(myObj[key]); // would print every value in the object
}

// The for-of loop allows for the iteration over an iterable object (like an Array or String)
const arr = [1, 2, 3, 4];
for (let num of arr) {
	console.log(num);
}
```
**Further Reading**: [For vs. For-in vs. For-of vs. forEach](https://thecodebarbarian.com/for-vs-for-each-vs-for-in-vs-for-of-in-javascript)
