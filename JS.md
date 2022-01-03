# Javascript CheatSheet

## Main brackets

- `{ }`: aka Braces aka curly braces is mainly used for `grouping statements and declarations. Also the contents of a class/interace are enclosed here. Method and consutrctor bodies are enclosed in here. if statements, loop and control structures like functions are there.`
- **Basically this is to define a scope**.
- e.g. of things we have seen so far:
- function exampleFunction = (empty or where parameters go) => {function statement 1; function statement 2}
- class ExampleClass {here stick the rest of the code defining your this.keys and optionally your constructor and super if you want to insert parameters externally}
- if (condition of any kind) = {what will happen if you condition is true} else {what will happen if your condition is false}
#

- `( )`: aka parentheses are mainly used for `two things: control order of math operations, and supply parameters to a constructor or method`
- **Basically this is to feed parameters to other stuff**
- **This also activates functions or methods, to tell it to actually do the stuff** If you don't include these parenthesis 
- console.log() <= whatever you're going to put in this parenthesis is a parameter.

#
- `[ ]`: aka square brackets are mainly used for `index into arrays`
- **This is exclusive to arrays and is only here to index stuff.**
- e.g. let thisIsAnArray = [itemInIndex0, itemInIndex1]
- btw you also use the [] when you want to summon a specific item in an index. so Console.log(thisIsAnArray([0])) means you are summoning whatever is in index 0 (the first position of an array).

## Javascript Basics

**Comments**

Comments in javascript are in the following format

```js
/* This 
is
a 
multiline
comment */

// this is a single line comment
```

**Variables and constants**

Let and const allow you to create stuff in Javascript.



variables -> `let`
`let`: for variables
- Variables can be easily changed and revised/redefined later down the code.

`const`: for constants
- Stuff you create through const can never be revised later. That means you can't manually redefine it.
- They can still intake parameters (parameters = inputs) for the constant to do something, like a function created through const. 
- Also one exception: arrays created through const can still have elements pe pushed in or popped out of existence.

```js
// to create a new variable
let Object = something;
// to create a new constant
const somethingyouneverwantchanged = 5;
```

**Main Types:**

```js
// Number:
let a = 5;

// String:
let b = "This is quite literally a bunch of text";
BTW Javascript is so flexible, if you put a number as a 
string, which is literally text, Javascript can understand it as a number.

// Boolean:
let c = true;
Booleans come in two type: the literals which are true and false.
Logical operators. && means AND. || means OR. 
! means the opposite of. So literally put ! before anything and then JS will interpret it as the opposite.
!function(parameter) means literally do the opposite of that function with the parameter we put.
!= means not equal.

```

**Print**
To print out on the console

```js
// 1. printing string
Console.log("Hello World"); // -> Hello World
BTW console logging only shows the developer the messages. IRL settings, console log will not be shown to users!

The quotations marks "" make stuff be string, as in literal text.

If you didn't put quotation marks, you'd be telling javascript to log something called Hello World that you'd have needed to define before.

You would know it's a function or a method if it was Hello World() because even if the parenthesis is empty, you're telling JS to make something do something.

// 2. printing values inside stored variables or constant
const pi = 3.14;
console.log(pi); // 3.14

// 3. printing more than one element,
const x = 5;
const y = 10;
console.log(x+" Hello World "+y); // 5 Hello World 10
SYNTAX TIME!
Plus "+" here means you are combining elements. You are telling javascript "first conosle log x, then console log this string, then console log y. Because x and y are objects, and you are calling the object, rahter than directly what it is manually, you use plsu.

// 4. console.log adds one line after it finishes
console.log("\n"); // will just print an empty new line
```

### Basics

#### Strings

Anything in javascript between `" "` or `' '` or back ticks ` `` ` is called a string.
Every text should be between quotation marks.

- Choose any but ` ` are typically better because they'll allow certain special stuff to happen within strings that you don't want to be literal text.

**SYNTAX TIME!!**
- Not everything you put in quotation marks will appear as is. If you are typing string in quotations here are some stuff that won't be interpreted as literal text:
- \ and a letter. The "\" or backslash is key here.
- ${ } will make appear something from a code or something else.
- If you begin and end with a set of quotation marks of your choice, any other types of quotations you choose to put in that same string will be interpreted as that string.


**Special Characters**

```js
console.log("your text here and then put... in your quotation\n"); // prints a new line
console.log("your regular text here and then... \t to tab!"); // prints a tab   space
console.log("blabla text and then... \\ literally type double backslash since a single backslash is telling JS that even though this is literal text, you want to do some formatting."); // prints a single back slash \
console.log(`"`); // prints a single quotation mark "
```

**String Interpolation**
To add values inside a string we use the back tics `` `TEXT ${VARIABLE or COMPUTATION} TEXT` ``

```js
const x = 1;
const y = 100;
console.log(`x:${x}, y:${y}`); // prints: x:1, y:100
console.log(`${y+x}`); // prints: 101
```

**Mathmatical operations**

```js
// addition
10 + 5

// subtraction
10 - 5

// multiplication
10 * 5

// division
10 / 5

// remainder: The remainder of the division
10 % 5
PROTIP!!
Want odds or even?

if x % 2 = 0, that means the number is even
if X % 2 != 0 that means the number is odd. FYI != means not equal.

```

#### If statement

**Logical operations**

```js
// Equals
"5" == 5 // returns true
SYNTAX TIME!!
If you had put just one equal symbol, you're telling javascript to define "5" as...5. The same way you'd be telling javascript let cookies = "tasty" or something (but with wrong syntax).

This is why for the math expression of equals when not inside an object already, you want two equal signs.

// Strictly Equals (Better usage: returns true if same value, same type)
"5" === 5 // returns false

// doesn't equal
5 != 5 // returns false

// doesn't strictly equal
5 !== 5 // returns false


// greater than
10 > 5 // returns true

// greater than or equal
10 >= 10 // returns true

// less than
10 < 5 // returns false

// less than or equal
10 <= 5 // returns false

SYNTAX TIME!!
When doing the greater/less or equal stuff, put the symbol first then the equal sign.

// connects 2 booleans, both of them should be true to make the final result true
10 > 5 && "Hello" == "Hi" // returns false, because the second one is false

// connects 2 booleans, one of them should be true to make the final result true
10 > 5 || "Hello" == "Hi" // returns true, because the first one is true
```

**If Statement**

```js
// The condition inside the () should return either true or false
const x = 5;
if (x === 5){
  // statement that will be executed if the condition was true
  console.log("The if statement returned true!")
}


// You can link the if statement with else to execute if the condition was false

const x = 5;
if(x!=5){
  // do job 1
   console.log("The if statement returned true! This was the first job to do assuming the statment was true")
}
____{
  // do job 2
  // This code will only be execute if only the condition inside the if didn't work
  // you don't put a condition after the else statement
  console.log("The if statement returned false. This was the first job to do assuming the statment was false")
}

// In this if chain, only one of the following jobs will be executed
if(CONDITION){
  // job 1
}
____ __(CONDITION 2){
  // job 2
}
____ __(CONDITION 2){
  // job 3
}
else{
  // job 4
}
```

There are some rules for the if chain

1. You can only have `else if`s between if and else
2. You cannot add `else` after `else`
3. One job only the if chain will be executed, even if the other `else if`s conditions where true

**Reminder %**
We use the reminder `%` for couple of usages, most importantly, knowing even or odd numbers.
Even numbers will return true on the following statement

```js
const x = ???
// if you want to check if x is even, you do the following condition
if(___________){
  // will only be executed if x was event
}
```

---

# Functions

You deal with functions in 2 main things

1. Function creation
2. Function execution (invoking)

```js
// 1. function creation
________ functionName(){
  // This code will be executed when you call the function
}

// 2. To invoke the function
functionName()
```

**parameters and arguments**

- We call them parameters from the outside when we call the function
- We call them arguments from the inside when we create the function

```js
// 1. Function that takes multiple arguments
function foo_________{
}

// 2. Calling the function and passing multiple parameters
______________________


```

**Return**
A function can return using the command `_______` by the end of the function

```js
// this function for example returns the square of any number you plug it
function square(x){
  ______ x * x;
}
console.log(square(4)) // this will log 16
```

> **COMMON MISTAKE**
> When we return, we use the console.log to log the returned value. Lots of times, we do the mistake of trying to console.log inside the function.

---

# Arrays

You can put groups of elements

```js
// New array
let numbers = ___ADD_ANY_NUMBER_HERE___;
```

**Accessing elements**

```js
const array = [100, 90, 80, 40];

// To access the first element
array____;

// To access the second element
array____;
//
```

**Length**

```js
const array = [100, 90, 80, 40];

array._____; // returns number of elements in the array
console.log(array.____); // prints number of elements in the array
//
```

**Length usages: Getting the last element in the array**

```js
const array = [100, 90, 80, 40];

// to get the last element in the array
array[__________];
```

**push and pop**

```js
array._____; // adds a new element
array._____; // removes the last element
//
```

# Loops

There are 2 main loops

1. `____` loop
2. `____` loop

```js
____(condition){
  // keeps looping while the condition is true
}

___(let i=0; i<10; i++){
  // initializes a counter
  // keeps looping while the condition is true
  // and increments on every loop
}
```

# Iteration Methods And Arrow Functions

### Arrow functions

```js
// the function way
function foo() {}
// the arrow function way
___________;
___________;
___________;
```

### Iteration Methods

- Iteration methods work on **\*\***\_\_\_\_**\*\*** only!
- All iteration methods go over evrey single element of the array
- Iteration methods take a function that has a parameter of the current value of the array. Preferred to use arrow function inside it.

```js
array.SOME_ARROW_FUNCTION((element) => {
  // Whatever action you want to perform on every element
  // Most arrow functions will require you to return something
});
```

The following are the main iteration methods

1. `._______`: just goes over all the elements, doesn't return anything, and doesn't require you to pass a function that returns anything
2. `.____`: returns a filtered copy of the array that is based on a condition that you return from the function you pass it.
3. `.____`: returns a transformed copy of the array that is based on a returned shape of every element that you return from the function you pass it
4. `.____`: looks exactly like `.filter`, but it only returns the first element that matches the condition
5. `.____`: looks exactly like `.find`, but it only returns true if it finds 1 element that matches the condition
6. `.____`: returns a single value that is compiled throught the whole array using `previous` and `current` values being passed in passed function. We usually use it to get the sum

```js
const array = [10, 20, 30, 40, 50, 60];
array.___((e) => e / 10); // returns a transformed array equals to [1,2,3,4,5]
array.___((e) => e <= 30); // returns a filtered array equals to [10, 20, 30]
array.___((e) => e === 20); // returns 20
array.___((e) => e === 20); // returns true
array.___((prev, current) => prev + current); // returns the sum of the array (210)
```

# Objects

The structure of object is a pair of `_______:_______`

```js
// To create an object
const object = _
PROPERTY_NAME: VALUE,
"PROPERTY NAME 2": VALUE, // if there are spaces, you can use the quotation marks
_

// to access one element of the object, we have couple of ways
object.PROPERTY_NAME
object["PROPERTY_NAME"]
```

## Accessing the object dynamically

```js
const someObj = {
  key1: "value1",
  key2: "value2",
};
const keyName = "shade of red";
console.log(someObj___keyName___);
```

## Adding new proprties to the object

```js
const someObj = {
  key1: "value1",
  key2: "value2",
};
someObject_____;
```

# Classes

Classes only have 2 main things to write inside them

1. **Methods**: They are just functions inside a class
2. **Properties**: They are just variables or constants
   You can't execute a function inside the class body, it should only be inside methods.

```js
// to create a new class
____ ClassName{


}

// creating object
const object = ____ ClassName();

// Adding properties to the class (without a constructor)
class ClassName{
  name = "Ali";
  age = 3;
}
```

### Creating Methods

```js
class ClassName {
  // the ordinary function way
  _________;

  // the arrow function way
  _________;
}
```

### Constructor

A constructor is just a special **method** that has the following features

1. It gets executed when you create an object from the class using the `new` keyword
2. It's used to initialize the properties
3. It has no name

```js
// creating the constructor
class ClassName {
  __________(name, age, interests) {
    _____.name = name;
    _____.age = age;
    _____.interests = interests;
  }
}
```

### Inheritance

```js
class ParentClassName{}
class ChildClassName _______ ParentClassName{}
```

//final advice to myself: create a lexicon and a word pattern recognition for javascript, like primitive types, reference types, what objects are exactly.... Primitive types copy values, but objects do not. Primitive types are immutable, objects will change. All objects are references.