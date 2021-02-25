# web-dev-primer
A modern guide of the useful parts of HTML, CSS, and JS to get quickly started with web development. This guide assumes knowledge of at least one other programming language and some basic concepts of Computer Science.

# Table of Contents
1. [HTML](#html)
    1. [Structure of an HTML Document](#structure-of-an-html-document)
    2. [Text Content Tags](#text-content-tags)
    3. [List Tags](#list-tags)
    4. [Text Formatting Tags](#text-formatting-tags)
    5. [Tables](#tables)
    6. [Forms](#forms)
2. [CSS](#css)
    1. [CSS Selectors](#css-selectors)
    2. [CSS Properties](#css-properties)
    3. [Inline Styling](#inline-styling)
    4. [Responsive Design](#responsive-design)
4. [JavaScript](#javascript)
    1. [Declaring Variables](#declaring-variables)
        1. [Objects](#objects)
        2. [Arrays](#arrays)
        3. [Strings](#strings)
        4. [Template Strings](#template-strings)
    2. [Operators](#operators)
        1. [Arithmetic Operators](#arithmetic-operators)
        2. [Assigment Operators](#assignment-operators)
        3. [Comparison Operators](#comparison-operators)
    3. [Conditionals](#conditionals)
    4. [Loops](#loops)
    5. [Functions](#functions)
        1. [Default Parameters](#default-parameters)
        2. [Immediately Invoked Function Expressions](#immediately-invoked-function-expressions)
        3. [Passing Functions as Arguments](#passing-functions-as-arguments)
        4. [Arrow Function Expression](#arrow-function-expressions)
        5. [Uses for Arrow Functions](#uses-for-arrow-functions)
6. [JavaScript-HTML Interaction](#javascript-html-interaction)
7. [Credits](#credits)

# HTML
Hypertext Markup Language or HTML, is as the name suggests, not a programming language, but a markup language. This means that you have a series of tags that you can use to wrap other tags or text to mark the text as certain entities. This is in turn interpreted by the browser to show the elements that you are used to (which are then styled by CSS which is covered later). Element tags consist of an open tag and a close tag, a close tag being the same as an open tag, but with a `/` before the tag name.

## Structure of an HTML Document
Everything in an HTML document needs to be wrapped in the `<html>` tag. The `<head>` tag is used for things that are not visible, like information about the page that is useful to the browser, but that is not visualized. This includes stylesheet imports, title, metadata, and other things of that nature. The `<body>` tag is where the meat of the page is, all the things that are seen by the user. Make sure the `<head>` on top of the `<body>` just like in humans.

```html
<html>
    <head>
        <title>My First Page</title>
    </head>
    
    <!-- This is a comment -->
    <body>
        <h1>My First Page</h1>
        <p>This is my first page.</p>
        
        <h2>A secondary header.</h2>
        <p>Some more text.</p>
    </body>
</html>
```

## Text Content Tags
A lot of what a page consists of is text, and these are the most common text formatting tags.

Headings go from 1-6 in decreasing order. Think of them as titles and subtitles used in textbooks.
```html
<h1>Largest</h1>
<h2>Second Largest</h1>
<h3>Third Largest</h1>
<h4>Third Smallest</h1>
<h5>Second Smallest</h1>
<h6>Smallest</h1>
```

## List Tags
HTML adds bullets and numbers to the lists automatically, you just need to use the proper tags. `<li>` stands for "list item" and is used in both unordered and ordered lists.
```html
<!-- Unordered List (think bulleted list) -->
<ul>
    <li>Bacon</li>
    <li>Eggs</li>
</ul>

<!-- Ordered list (think numbered list) -->
<ol>
    <li>Wake up</li>
    <li>Brush teeth</li>
</ol>
```

## Text Formatting Tags
You can add text formatting via CSS, but sometimes you want that information to exist in the HTML document.
```html
<b>Bold</b>
<i>Italics</i>
<u>Underlined</i>

<sup>Superscript</sup>
<sub>Subscript</sub>
```
**Further Reading:** [W3Schools Article on HTML Text Formatting](https://www.w3schools.com/html/html_formatting.asp)

## Tables
To make a table, wrap everything in a `<table>` tag first and foremost. Then each row should be in a `<tr>` "table row" tag. Table headers should be in `<th>` "table header" tags and other table cells should be in `<td>` "table data" tags.
```html
<table>
    <tr>
        <th>First Name</th>
        <th>Last Name</th>
    </tr>
    
    <tr>
        <td>Tom</td>
        <td>Hanks</td>
    </tr>
    
    <tr>
        <td>Margot</td>
        <td>Robbie</td>
    </tr>
</table>
```
**Further Reading:** [MDN Article on Tables](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)

## Forms
Forms are an important part of web development because it allows us to collect data from the user in a structured way and send it to a server (if necessary).
```html
<form>
    <input type="text">Name</input>
    <input type="number">Age</input>

    <button type="submit">Submit Data</button>
</form>
```
**Further Reading:** [MDN Article on Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)  
**Further Reading:** [W3Schools Article on HTML Input Types](https://www.w3schools.com/html/html_form_input_types.asp)

# CSS
Cascading Stylesheets or CSS, is a way to style your HTML. A stylesheet is a set of one or more CSS rules. A CSS rule consists of a selector (what the rule is applied to) and a set of CSS properties (what is applied to the selected elements).
```html
<p>This is some text</p>
```

```css
p {
    color: white;
    background-color: red;
}
```

## CSS Selectors
In the example above, all `<p>` elements are selected by the CSS selector, and the properties that are being modified are the text color and the background color.

**Further Reading:** [W3Schools Article on CSS Selectors](https://www.w3schools.com/cssref/css_selectors.asp)

## CSS Properties
There are too many CSS properties to go over in this guide, so Google is your friend.

**Further Reading:** [MDN CSS Properties Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)

## Inline Styling
In HTML you can easily set CSS properties on individual elements, if you don't feel like using a stylesheet or if you just want to affect a specific element.
```html
<p style="color: white; background-color: black;">Hello, World!</p>
```

## Responsive Design
Nowadays everything has a web browswer, meaning that a website is viewed on all kinds of screen sizes, meaning that you have to make sure that your elements are sized properly so that it doesn't mess up on certain devices. Often times web developers rely on CSS frameworks to do a lot of the responsive design work.

**Further Reading:** [MDN Article on Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)  
**Further Reading:** [Bootstrap CSS Framework](https://getbootstrap.com/)

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

### Strings
Strings kind of act like arrays in JavaScript, but they're not actually arrays.
```js
// Strings can be declared with single or double quotes 
// (this only matters when you have one of these characters in between the two quotes and need to escape it)
let myString = "Hello";
let otherString = 'Hello';

// Strings can be concatenated with + and += (you'll learn more about those operators below)

// Strings have a .length property like arrays
myString.length; // = 5

// You can access characters at a particular index with the brackets like in arrays
myString[1]; // = "e"

// However, strings are immutable so you can't change anything with the brackets like in arrays
myString[0]; = "J" // this does nothing
```

### Template Strings
Template strings are a cool way to interpolate variables into your strings in a readable format.
```js
let favoriteNum = 5;

// You use backticks and surround a JavaScript variable or expression in the ${} symbols
let statement = `My favorite number is ${favoriteNum}!`;
let otherStatement = `My favorite number is ${3 + 2}!`; // prints the same thing as above
```
**Further Reading:** [MDN Article on Template Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

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
**Advanced Reading:** If you want to make an object iterable, you can use [Object.entries/values/keys()](https://javascript.info/keys-values-entries)

## Functions
You define functions in JavaScript with the `function` keyword and you invoke functions with `()` just like in most other languages. If you need to return a value, the `return` keyword is used. Since this is a dynamically typed language, you don't need to declare parameter or return types.
```js
function myFunction() {
    console.log("Hello, World!");
}

myFunction();

// Function with parameters
function addTwoNumbers(numOne, numTwo) {
    return numOne + numTwo;
}
```

### Default Parameters
You can also set default parameters in JavaScript.
```js
function printString(str="Foo") {
    console.log(str);
}

printString("Hello") // prints "Hello"
printString(); // prints "Foo"
```
**Further Reading:** [MDN Article on Default Parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)

### Immediately Invoked Function Expressions
Something cool that you can do in JavaScript is an Immediately Invoked Function Expression (IIFE). Essentially you define a function and call it at the same time.
```js
// This function is also an anonymous function, it has no name
// This function could not be called anyway because the parenthesis around the function that create a closure
(function() {
    console.log("Hello, World!");
})();
```
**Further Reading:** [MDN Article on IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)  
**Further Reading:** [MDN Article section on Anonymous Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions#the_function_expression_function_expression)  
**Further Reading:** [MDN Article on Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)

### Passing Functions as Arguments
You can pass functions as arguments to other functions, which becomes useful in many cases.
```js
// prints "Hello" every five seconds"
setInterval(function() {
    console.log("Hello");
}, 5000);

// waits 3 seconds, then prints "World"
setTimeout(function() {
    console.log("World");
}, 3000);
```
**Further Reading:** [W3Schools Article on Timing Event](https://www.w3schools.com/js/js_timing.asp)

### Arrow Function Expressions
There is another way to create functions, which are called arrow functions. These are a special type of functions that don't bind to `this` which means they can't be used in all situations. They are always anonymous, but can be assigned to a variable and can be used like any other function.
```js
// Much more compact!
setTimeout(() => {
    console.log("World");
}, 3000);

// Parameters are in the same format you would expect in another function expression
const addTwoNumbers = (numOne, numTwo) => {
    return numOne + numTwo;
};

addTwoNumbers(3, 4); // returns 7

// One line arrow functions can omit the brackets
const printString = (str) => console.log(str);

printString("Hello"); // prints "Hello"

// If an arrow function is one line and returning something, the return keyword is not necessary
const addTwo = (num) => num + 2;

addTwo(2); // returns 4
```
**Further Reading:** [MDN Article on Arrow function expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### Uses for Arrow Functions
Arrow functions are predominately used with functions associated with "functional programming" so `map`, `filter`, and `reduce`.
```js
const arr = [1, 2, 3, 4, 5];

// map applies a function to each value in the array and then returns a new array
const doubled = arr.map(num => num * 2); // returns [2, 4, 6, 8, 10]

// filter applies a function to each value in the array and keeps the values where
// the function returns true
const evens = arr.filter(num => num % 2 == 0); // returns [2, 4]

// reduce applies a function to each value and keeps an "accumulator" variable which it
// returns at the end
const sum = arr.reduce((acc, num) => acc + num); // returns 15
```
**Further Reading:** [Map, Filter, and Reduce](https://medium.com/poka-techblog/simplify-your-javascript-use-map-reduce-and-filter-bd02c593cc2d)

# JavaScript-HTML Interaction
HTML is represented as a tree and is accessible to JavaScript via the DOM (Document Object Model) API.

**Further Reading:** [MDN Article on DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Using_the_W3C_DOM_Level_1_Core)

All that you really need to know is that you can get a reference to an HTML element via JavaScript and then call functions on it like you would any other JavaScript object.
```html
<p id="numClicks">0</p>
<button id="myButton">Click me!</button>
```

```js
// get the element with the id "myButton" and store in the variable
const button = document.getElementById("myButton");

const numClicksEl = document.getElementById("numClicks");

// whenever the button is clicked by the user in the browser,
// the onclick function is called, and we just bound a function to it
button.onclick = () => {
    // + will work as concatentation with a string, so we need to convert to a number
    numClicksEl.innerText = parseInt(numClicksEl.innerText, 10) + 1;
}

// this would have the same effect as the code above, but usually .onclick is cleaner
// to write
button.addEventListener("click", () => {
    // + will work as concatentation with a string, so we need to convert to a number
    numClicksEl.innerText = parseInt(numClicksEl.innerText, 10) + 1;
});
```
**Further Reading:** [Article on DOM Manipulation](https://www.hongkiat.com/blog/dom-manipulation-javascript-methods/)

# Credits
Some code examples and explanations in the JavaScript section were taken and modified from [Learn JavaScript in Y minutes](https://learnxinyminutes.com/docs/javascript/), except they were updated to use a more modern form of JavaScript (ES6).
