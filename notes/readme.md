
# How to start the server:

```bash
npm start
```

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

## Class

```java

// simple class:

	// to create a class we use the word "class" and the class neme the first letter musth by with uppercase by convention
	class Car {

	}

	// Declare and instanciate the class created 
	let car = new Car();
```

```java

// class constructor:
	
	class Car{
		constructor(id){
			this.id = id;
		}
	}

	let car = new Car(123);
	console.log(car.id);
```

```java

// Methods

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

```java

// Inheritance

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

## Modules

### Exporting modules

Create a new file and paste the following code

```java
	export class Car{
		constructor(id){
			this.id = id;
		}
	}
```

"export" word will do the job

### Importing modules

In other file paste the following:

```java
import { Car } from "<YOUR_PATH_HERE>";

let car = new Car(123);
console.log( car.id );
```

- The path could either relateive or absolute
- The word "Car" in curly braces is the function to import from the other file

## The window object
### Timers

#### setTimeout
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

#### setInterval
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

### DOM elements

#### Selecting DOM elements

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
#### Modifying DOM elements
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

