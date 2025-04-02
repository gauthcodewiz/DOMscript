# Introduction
You don't need any special software to run JavaScript, it is run by standard browser when *attached* to an HTML file.

# Syntax
Syntax is to code as grammar is to English. All languages have a syntax, some lose some strict. JavaScript, although completely different from Java, shares some similarities in the standardized syntax, but JavaScript itself allows for multiple ways to write the same code. A line of code read by JavaScript is called a statement, and the following three are equivalent ways of writing two statements in Javascript:

1. New line between two statements
```
first statement
second statement
```

2. Semicolons at the end of statements
```
first statement; second statement;
```

3. **Recommended:** Semicolon and new line
```
first statement;
second statement;
```

## Comments
Not all lines of code are read as *code*, some lines can be comments to document the code for readability and accessibility. 

1. Double forward slash for single line comments
```
statement; 
// This line is a comment
// This is another comment

statement; // this line is also a comment
```

2. HTML comment format using `<!-` which is same as `//` in JavaScript
```
statement; <!- Comment->
statement; <!- Also Comment
```

**Note:** Although HTML requires opening tag `<!-` and closing tag `->`, JavaScript only requires the opening tag `<!-` which is same as a double forward slash `//`

3. Multiline comments between `/*` and `*/`
```
/* This is a
   multiline comment */
```

Comment lines are ignored by the web browser so these don't affect the code.

## Variables

Like statements and comments, there are multiple ways to *declare* and *assign* variable in JavaScript:

1. Declaring empty variable without assigning value
```
var mood;
var age;
```

2. Declaring multiple empty variables
```
var mood, age;
```

3. Declaring and assigning values to variables simultaneously
```
var mood = 'happy';
var age = 29;
```

4. Directly assinging variables to values
```
mood = 'happy';
age = 20;
```

## Data Types
Certain languages are strogly typed, requiring each variable to be assigned the type of value it holds, and not changing it later. JavaScript is loosely typed, variables can be declared without assinging any value or type, called empty or undefined variables, and variables can be reassigned values of different types.

```
var x = 24; // x is assigned a Number type value of 24
x = 'new' // x is reassigned a String type value of 'new'
```

### Strings
Strings consist of zero or more *characters* and can be placed between single or double quotes:
```
var mood = 'happy';
var mood = "happy";
```

If you have single quotes within your string, it is placed between double quotes:
```
var mood = "don't ask";
```

This can also be written between single quotes using a backslash:
```
var mood = 'don\'t ask';
```

When the String contains both single and double quotes, use either and backslash as required:
```
var height = 'about 5\'10" tall';
var height = "about 5'10\" tall";
```

### Numbers
Numbers and decimals (called floating-point numbers) are easily declared in JavaScript:
```
var temperature = 23;
var score = 35.57;
var difference = -20;
var answer = -49.88;
```

### Boolean Values
Boolean data has two possible values, `true` and `false`.

```
var fact = true;
var lie = false;
```

There are some intricacies to boolean in JavaScript which can be explored later.

### Arrays
Arrays are a list of data. An array of length 4 is declared as follows:
```
var ants = Array(4);
```

An array can also be declared without assigning a length:
```
var new = Array();
```

An array *index* starts from 0 and goes as 0, 1, 2, 3, ... and the index value is called as `array[index]`
```
var names = ['heena', 'Sam', 'ritwika'];
console.log(names[0]); // output -> heena
console.log(names[1]); // output -> Sam
console.log(names[2]); // output -> ritwika
```

The array can also be defined sequentially:
```
var names = Array(3);
names[0] = "heena";
names[1] = "Sam";
names[2] = "ritwika";
```

An array can hold, strings, numbers, decimals, and boolean variables and values, and even functions and object, about which we will learn later.
```
var independence = ['India', 1947, true];
var info = ['states', 32, false];
```

Previously, we have declared *numeric arrays*, arrays can also be *associative* where the index is a string, and not a number:
```
var independence = Array();
independence['country'] = 'India';
independence['year'] = 1947;
independence['status'] = true;
```

Further, one can also explore multidimentional numeric and associative arrays.

### Operators
Besides varible assignment, JavaScript supports common operations like addition `+`, subtraction `-`, multiplication `*`, and division `/`. Further there are operations like comparison (for example `>`, `<`, `>=`, `<=`, and `==`), logical (`&&` AND, `||` OR, `!` NOT), and string concatenation - adding two strings by joining them, and even Binary Operations. There are a whole lot more operations in JavaScript and these can be found online. The Math is really fun to explore. However, you won't be requiring many of those in regular coding.

### Conditional Statements
Conditional Statements, or simply conditionals, help the script make decisions based on the condition provided. If the condition is found as `true`, then the statements are run by the web browser:
```
if (condition) {
   statement one;
   statement two;
}
```

If only a single statement is to be run based on the condition, one can avoid the curly braces:
```
if (x>10) console.log('x is greater than 10');
```

Further one can utilize if-else blocks:
```
if (condition) {
   statement;
} else {
   statement;
}
```

### Looping Statements

There are three looping statements in JavaScript

1. `while` loop
```
while (condition) {
   statements;
}
```
Statements in `while` block are only run by the web browser if the condition is `true`. Another example is shown below:
```
var count = 1;
while (count < 11) {
alert (count);
count++;
}
```


2. `do`...`while` loop
```
do {
   statements;
} while (condition);
```
Statements in the `do` block are run atleast once before the condition is checked to be `true`.

Looping statements are great for several purposes, but it is important to check the loop-ending or terminating conditions so that the computer doesn't run into a *forever loop*.

3. `for` loop
The `for` loop is especially useful. The following two are equivalent ways of writing the same code:

- Using `while` block:
```
initialize;
while (condition) {  // check condition
   statements;       // run statements
   increment;        // increment or change parameters
}
```

- Using `for` block:
```
for (initialize; check condition; change parameters) {
   statements;
}
```

### Functions
If the same code is to be run multiple times, even with some parameter changes, then functions are here to help you. In general, you would declare a function before invoking it to avoid any errors.

Here is a simple function `call_names` that alerts all the names in the array `names` one by one:
```
function call_names () {
   var names = Array('heena', 'Sam', 'ritwika');
   for(var count = 0; count < names.length; count++) {
      alert(names[count]);
   }
}
```

The previous function does not take any *arguements*, a function that requires an input has arguements in its declaration:
```
function name(arguements) {
   statements;
}
```

The following function takes two numbers as arguements and alerts the product of the two numbers:
```
function multiply (num1, num2) {
   var product = num1 * num2;
   alert(product);
}
```

Now the function can be called anytime in the script after it is declared by writing statements such as `multiply(2, 5)` or `multiply(4, -19)`.

### Objects
Objects are self-contained collection of data. This data comes in two forms, **properties** and **methods**:
```
object.property;
object.method();
```

A **property** is a variable belonging to an object.
A **method** is a function that the object can invoke.

To define an object, `new` keyword is used.
```
var Sam = new Person;
```

But this would require `Person` object to be defined earlier. There are many ways to make user-defined objects.

1. Literal Objects
```
const person = {
  name: "Sam",
  age: 25,
  greet: function() {
    console.log(`Hello world, my name is ${this.name}`);
  }
};
person.greet(); // Output: Hello world, my name is Sam
```

2. `new Object()` constructor:
```
const person = new Object();
person.name = "Sam";
person.age = 25;
person.greet = function() {
  console.log(`Hello, my name is ${this.name}`);
};
person.greet();
```

3. Constructor functions:
```
function Person(name, age) {
  this.name = name;
  this.age = age;
  this.greet = function() {
    console.log(`Hello world, my name is ${this.name}`);
  };
}
const Sam = new Person('Sam', 25);
Sam.greet(); \\ Output: Hello world, my name is Sam
```

4. ES6 Classes
```
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello world, my name is ${this.name}`);
  }
}
const Sam = new Person('Sam', 25);
Sam.greet();      // Output: Hello world, my name is Sam
```

JavaScript allows for *user-defined* objects and *Native* Objects such as `Array()` and `Date()`:
```
var current_date = new Date();
var today = current_date.getDay();
```

Besides this, there are also *Host* objects such as Form, Image, and Element, which can be used to get information about forms, images, and form elements withing a web page. Our focus is going to be on the **document** object.