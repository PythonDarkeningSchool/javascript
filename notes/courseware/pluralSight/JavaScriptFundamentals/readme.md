# Table of contents

- [Tools](#tools)
  * [NodeJS](#nodejs)
  * [Development environment webpack](#development-environment-webpack)
    + [How to start the server:](#how-to-start-the-server)
- [Variables](#variables)
- [Rest Parameters examples:](#rest-parameters-examples)
- ["forEach" method is useful for iterate over a list](#foreach-method-is-useful-for-iterate-over-a-list)
- [Destructuring Arrays examples](#destructuring-arrays-examples-square-brackets)
- [Destructuring objects examples](#destructuring-objects-examples-curly-braces)
- [Spread Sintax examples:](#spread-sintax-examples)
- [IIFE's pattern development](#iife-s-pattern-development)
- [Arrow Functions](#arrow-functions)
- [Interpolation](#interpolation)
- [JSON](#json)
  * [Convert to JSON (JSON to string)](#convert-to-json--json-to-string)
  * [Parse to JSON (string to JSON)](#parse-to-json--string-to-json)
- [Arrays](#arrays)
  * [Array Iteration](#array-iteration)
  * [Array Filtering](#array-filtering)
  * [Array Finding](#array-finding)
- [Class](#class)
  * [simple class](#simple-class)
  * [class constructor](#class-constructor)
  * [Methods](#methods)
  * [Inheritance](#inheritance)
- [Modules](#modules)
  * [Exporting modules](#exporting-modules)
  * [Importing modules](#importing-modules)
- [The window object](#the-window-object)
  * [Timers](#timers)
    + [setTimeout](#settimeout)
    + [setInterval](#setinterval)
  * [DOM elements](#dom-elements)
    + [Selecting DOM elements](#selecting-dom-elements)
    + [Modifying DOM elements](#modifying-dom-elements)
- [Errors in JavaScript](#errors-in-javascript)
  * [try, catch and finally](#try--catch-and-finally)
  * [Developer Defined Errors](#developer-defined-errors)
- [HTTP Requests](#http-requests)
  * [Pre-setup](#pre-setup)
  * [Using JQuery](#using-jquery)
    + [Install JQuery using terminal](#install-jquery-using-terminal)
    + [Verify that JQuery was installed](#verify-that-jquery-was-installed)
    + [Import JQuery module into the JavaScript code](#import-jquery-module-into-the-javascript-code)
    + [Creates a local variable to handle it as a promise](#creates-a-local-variable-to-handle-it-as-a-promise)
      - [GET method](#get-method)
      - [POST method](#post-method)
    + [Setup the handlers for the promise](#setup-the-handlers-for-the-promise)
- [Forms](#forms)
  * [Preventing form submission](#preventing-form-submission)
  * [Accessing form fields](#accessing-form-fields)
  * [Showing validation errors](#showing-validation-errors)
  * [Posting to webserver with a form](#posting-to-webserver-with-a-form)
    + [with JQuery](#with-jquery)
- [Security and Building for Production](#security-and-building-for-production)
  * [Application Data Security](#application-data-security)


# Tools

## NodeJS

| For npm commands

- [nodejs](https://nodejs.org/en)

## Development environment webpack

In order to run the development environment quickly install webpack

- [webpack official webpage](https://webpack.js.org)
- [webpack code in github](https://github.com/wbkd/webpack-starter)

### How to start the server:

```bash
npm start
```

# Variables

- "let" is for block scope and is prefered over "var" to create variables
- Constants needs to be initialize

# Rest Parameters examples:

Definition: collects a set of elements and store them in an array 

"..." in a function is used to converts params into a list

```java
// Example 1:
	function sendCards(...allCardsIds)

	sendCards(10, 20, 30)

	// Note: a "Rest Parameter" must be the last parameter in the list
```

# "forEach" method is useful for iterate over a list

# Destructuring Arrays examples (square brackets):
	
```java
// Example 1:
// Note: "this is also known as unpacking elements in other languages as python"

// create a list with values
let carIds = [1, 2, 5];

// Destructuring Arrays (unpacking elements) into a varibles
let [car1, car2, car3] = carIds;
```

```java
// Example 2 (using "Rest Parameters"):

// create a list with values
let carIds = [1, 2, 5];

// declaring only the variables withour initialize them
let car1, remainingCars;

/* 	Destructuring the array
	car1 = this variable will contains the first element in the array "carIds"
	remainingCars = this variable will contains the remaining elements in the arrat "carIds" as a list
*/
[car1, ...remainingCars] = cardIds;
```

```java
// Example 3:

// Destructuring the array skipping the first element with a "comma"
[, ...remainingCars] = cardIds;

// Note: you can have many commmands as you like to skip any elements as you like
```

# Destructuring objects examples {curly braces}:

```java
// Example 1:
	// create a simple object(dictionary) call "card" 
	let card = {id: 5000, style: "convertible"};

	/* 	Destructuring the object
		(declaring and initializing the variables)
	*/
	let {id, style} = card;
```

```java
// Example 2:

	/* 	Destructuring the object
		(declaring the variables)
	*/
	let id, style;

	/* 	initializing the variables (this is the correct way to do it)
		we use the "parenthesis" to avoid an error with the compiler, since the curly braces are also uses to declare a "code block"
	*/
	({id, style} = car);
```

# Spread Sintax examples:

Definition: this is the opposite to "Rest Parameters", Spread Sinxtax spread them out in too several parameters

```java
// Example 1:

function startCars(car1, car2, car3){
	console.log(car1, car2, car3);
}

let carIds = [100, 300, 500];
startCars(...carIds);
```

# IIFE's pattern development

stands for (Immediately Invoked Function Expression)	

```java
	Example 1:

	(function(){
		console.log("in function");
	})();

	// the above function it's going to be call right away
```

# Arrow Functions
	
1. The simbol of the arrow functions is: =>
2. Arrow functions does not have their own "this" value
    2.1 "this" refers to the enclosing context

```java
// Example 1:

	let getId = () => 123;

	console.log(getId()); // 123

	// structure:

		let variableName = parameter => returnFunction

		// where returnFunction can be anything

		/* Note: if the function only has one parameter it does not need
		the parenthesis surrounding the parameters, otherwise yes */
```

```java
// Example 2:

	let getId = (prefix, suffix) => prefix + 123 + suffix;
	console.log( getID("ID: ", "!") );  // ID: 123!
```

```java
// Example 3:

	let getId = (prefix, suffix) => {
        return prefix + 123 + suffix;
	};

	// Note: within the curly braces the "return" is needed, otherwise no
```

```java
// Example 4:

    let getId = _ => 123;

    /* Note: "underscore" stands for not parameters, is the same that the use of
    parenthesis*/
```

# Interpolation

```java
    // Example 1:

        let var1 = "some";
        let var2 = "text";
        console.log(`${var1} in ${var2}`);

        // I guest the variables needs to stay in the same context ??
```

# JSON

JSON stand for "JavaScript Object Notation"

## Convert to JSON (JSON to string)

```java
// Example 1:

    let car = {
        id: 123,
        style: "convertible"
    };

    console.log(JSON.stringify(car)); // {"id":123,"style":"convertible"}
```

## Parse to JSON (string to JSON)

```java
// Example 1:

        let jsonIn =
            `
            [
                {"carId": 123},
                {"carId": 456},
                {"carId": 789}
            ]
        `;

        let carIds = JSON.parse(jsonIn);

        console.log(carIds);
```

# Arrays

##  Array Iteration

```java

// Example 1:
    let carIds = [
        {carId: 123, style: "sedan"},
        {carId: 456, style: "convertible"},
        { carId: 789, style: "sedan" }
    ];

    carIds.forEach(car => console.log(car)); // print every element in the list
    carIds.forEach((car, index) => console.log(car, index)); // print every element in the list with their index

    // Note: "forEach" it is a method that has the list to iterate over their content
    // Notice that in each "forEach" loop the arrow function are being called without variable assignment
```

## Array Filtering
   
```java 
// Example 1:

    let carIds = [
        {carId: 123, style: "sedan"},
        {carId: 456, style: "convertible"},
        { carId: 789, style: "sedan" }
    ];

    let convertibles = carIds.filter(
        car => car.style === "convertible"
    );

    console.log(convertibles);
```

## Array Finding

Return the first element to match with the condition

```java

// Example 1:

    let carIds = [
        {carId: 123, style: "sedan"},
        {carId: 456, style: "convertible"},
        { carId: 789, style: "sedan" }
    ];

    let car = carIds.find(
        car => car.carId > 500
    );

    console.log(car);
```

# Class

## simple class

```java

	// to create a class we use the word "class" and the class neme the first letter musth by with uppercase by convention
	class Car {

	}

	// Declare and instanciate the class created 
	let car = new Car();
```

## class constructor

```java
	class Car{
		constructor(id){
			this.id = id;
		}
	}

	let car = new Car(123);
	console.log(car.id);
```

## Methods

```java
	class Car{
		constructor(){
			this.id = id;
		}

		identify(suffix){
			return `Car Id: ${this.id} ${suffix}`;
		}
	}

	let car = new Car(123);
	console.log(Car.identify("!!!"));
```

## Inheritance

```java

	// "extends" words is used for inheritance

	class Vehicle{
		constructor(){
			this.type = "car";
		}

		start(){
			return `Starting: ${this.type}`;
		}
	}

	class Car extends Vehicle{

	}

	let car = new Car();
	console.log(car.type); // car 

```

# Modules

## Exporting modules

Create a new file and paste the following code

```java
	export class Car{
		constructor(id){
			this.id = id;
		}
	}
```

"export" word will do the job

## Importing modules

In other file paste the following:

```java
import { Car } from "<YOUR_PATH_HERE>";

let car = new Car(123);
console.log( car.id );
```

- The path could either relateive or absolute
- The word "Car" in curly braces is the function to import from the other file

# The window object
## Timers

### setTimeout
setTimeout(), it is a JavaScript function to acccessible globally and it will execute the function
at one time in the future


```java

// Example:

let timeoutId = setTimeout( function(){
	console.log("1 second passed");
}, 1000)


// if need to cancel uncomment the code below
clearTimeout(timeoutId);
```

In the above example "setTimeout" function receives two params:
1. a function
2. a number in miliseconds to wait before execute the function

### setInterval
setInterval(), execute the function repeatedly and works equal than the previos function, with
the same number/type of arguments

```java
// Example:

let intervalId = setInterval( function(){
	console.log("1 second passed");
}, 1000)


// if need to cancel uncomment the code below
clearTimeout(intervalId);
```

## DOM elements

### Selecting DOM elements

```java
document.getElementById("elementId");
document.getElementByClassName("className");
document.getElementByTagName("tagName");

```

Example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <title>JavaScript Fundamentals</title>
</head>
<body>
    <h1>JavaScript Fundamentals</h1>
    <p id="first" class="p1">First Paragraph </p>
    <p name="name1" class="p1">Second Paragraph</p>
    <p class="p3">Third Paragraph</p>
</body>
</html>
```

```java
let element = document.getElementById("first");
console.log(element);
```
### Modifying DOM elements
In order to modify DOM elements first we need to select the element, e.g:

```java
let element = document.getElementById("elementId");
```

After this we can access to some properties or methods on it, e.g:

```java
element.textContent = "new text content";
element.setAttribute("name", "nameValue");
element.classList.add("myClassName");
element.style.color = "blue";
```

# Errors in JavaScript
## try, catch and finally

E.g of throwing an error due to an undefined variable

```java

try{
	let car = new Car;
}
catch(error){
	console.log("error: ", error); // ReferenceError: newCar is not defined
}
finally{
	console.log("this code always be executed");
}
```

## Developer Defined Errors

In the following example, the object `new Error` will be set to `error` variable in
the catch block

```java

try{
	// code here ...
	throw new Error("my custom error");
}
catch(error){
	console.log("error: ", error); // ReferenceError: newCar is not defined
}
finally{
	console.log("this code always be executed");
}
```

# HTTP Requests

## Pre-setup

| Mockapi is a webserver

1. Goto `https://www.mockapi.io`
2. Login with `Github`
3. Create a new project in order to get an `end-point`

end-point e.g:
```text
http(s)://5c6b15cbe85ff400140854da.mockapi.io/:endpoint
```

## Using JQuery

### Install JQuery using terminal

```bash
npm install jquery
```

### Verify that JQuery was installed

1. Open package.json
2. Search for "jquery" and their version

### Import JQuery module into the JavaScript code

```java
import $ from "jquery";
```

### Creates a local variable to handle it as a promise

#### GET method

```java
let promise = $.get("http://5c6b15cbe85ff400140854da.mockapi.io/api/v1/users");
```

#### POST method

```java
let user = {
    name: "someUser",
    avatar: "someFile.jpeg"
};

let promise = $.post(
	"http://5c6b15cbe85ff400140854da.mockapi.io/api/v1/users", user
);
```

### Setup the handlers for the promise

| Setup a handlers with arrows functions

```java
promise.then(
	data => console.log("success", data),
	error => console.log("error", error)
);
```

# Forms

## Preventing form submission

Form `html` template

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <title>JavaScript Fundamentals</title>
</head>
<body>
    <h3>JavaScript Fundamentals</h3>
    <form action="/somepath" method="post" id="user-form">
        <input name="user" placeholder="User Name" />
        <span id="user-error"></span>
        <br>
        <input name="avatar-file" placeholder="Avatar File" />
        <span id="avatar-error"></span>
        <br>
        <button type="submit">Submit</button>

    </form>
</body>
</html>
```

JavaScript code

```java
let form = document.getElementById("user-form");

form.addEventListener("submit", event => {
    // prevent the browser from submitting the form
    event.preventDefault();
});
```

## Accessing form fields

```java
let form = document.getElementById("user-form");

form.addEventListener("submit", event => {
    // accessing form fields
    let user = form.elements["user"];
    let avatarFile = form.elements["avatar-file"];

    console.log(user.value, avatarFile.value);
    // prevent the browser from submitting the form
    event.preventDefault();
});
```

## Showing validation errors

```java
let form = document.getElementById("user-form");

form.addEventListener("submit", event => {
    // accessing form fields
    let user = form.elements["user"];

    // accessing user error
    let userError = document.getElementById("user-error");

    if (user.value.length < 4) {
        userError.textContent = "Invalid Entry";
        userError.style.color = "red";
        userError.border.color = "red";
        user.focus();

    }
    // prevent the browser from submitting the form
    event.preventDefault();
});
```
## Posting to webserver with a form

### with JQuery

```javaimport $ from "jquery";

let form = document.getElementById("user-form");

form.addEventListener("submit", event => {
    // accessing form fields
    let user = form.elements["user"];
    let avatarFile = form.elements["avatar-file"];

    // create a dictionary to post to server grabbing the values from the form
    let posting = {
        user: user.value,
        avatarFile: avatarFile.value
    };

    // posting the data to the server
    let promise = $.post("someUrl", posting);

    // handle the server outputs with a promise
    promise.then(
        data => console.log("sucess: ", data),
        error => console.log("error: ", error)
    );

    // prevent the browser from submitting the form
    event.preventDefault();
});
```
# Security and Building for Production

## Application Data Security
- Don't store passwords, secrets or other sensitive information
- Don't use global variables
- Assume hackers can read your JS code and access all data sent to a browser

A tip is to convert the code with the following online tool

[JavaScript Obfuscator](http://javascriptobfuscator.com)
