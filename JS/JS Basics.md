#javascript #basic

## Variables

**JavaScript variables** are containers for data.
JavaScript variables can be **declared** in 4 ways:
- Using **let
- Using **const
- using **var (not recommended)
- Automatically (not recommended)

### Using let

```js
//camel case best for js variables

let numberOfStudents = 30;
let numberOfAvailableCourses = 8;
let currentBalance;

currentBalance = 3,500.50;
```
### Using const

Always use const when the variable doesn't change.

```js
// capitalize for global variables
const PI = 3.1415;
const HOURS
```

### Using var

Hoisting is JavaScript's default behavior of moving declarations to the top.
```js
x = 5; // Assign 5 to x  
  
elem = document.getElementById("demo"); // Find an element  
elem.innerHTML = x;                     // Display x in the element  
  
var x; // Declare x
```

Variables defined with `let` and `const` are hoisted to the top of the block, but not _initialized_.

Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared. Using a `let` variable before it is declared will result in a `ReferenceError`.
This causes an error:
```js
carName = "toyota";
let carName;
```

### Automatically

Just use it. ;)









## Scope

Basically, the thing "inside" can see "outside" but "outside" can't see inside. This works for function and blocks of code(anything in curly braces). 





## Functions

### Function definition

```js
// function expressions vs function declarations

const functionOne = function() {
    console.log("This is function one.");
};

function functionTwo() {
    console.log("This is function two.");
}

  
// the Function constuctor

const myFunction = new Function("a", "b", "return a * b");

  

functionOne(); // Outputs: This is function one.
functionTwo(); // Outputs: This is function two.  
console.log(myFunction(4, 5)); // Outputs: 20
```

### Closures

A closure is a function that has access to the parent scope, after the parent function has closed.

```js
//closure example

function myCounter() {
  let counter = 0;
  return function() {
    counter++;
    return counter;
  };
};

const add = myCounter();
add();
add();
add();
console.log(add()); // Output: 4

```




## Classes, Objects and Arrays

### Classes

```js
class Car {
  constructor(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
  }

  getDetails() {
    return `${this.year} ${this.make} ${this.model}`;
  }

  updateYear(newYear) {
    this.year = newYear;
  }
}

const myCar = new Car('Toyota', 'Corolla', 2020);
console.log(myCar.getDetails()); // Output: 2020 Toyota Corolla
```

#### Getters and Setters

```js
// use underscore to separate the name of the getter setter and the property
class Car {
	constructor(make, model){
		this._make = make;
		this._model = model;
	}
	
	get make() {
		return this._make;
	}
	set make(make) {
		return this._make = make; 
	}
}

const myCar = new Car("Tesla", "Model 3");
conole.log(myCar.make) // returns Tesla
myCar.make = "BMW"; // calls the set make method
```

#### Inheritance

```js
class Car {
  constructor(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
  }

  getDetails() {
    return `${this.year} ${this.make} ${this.model}`;
  }

  updateYear(newYear) {
    this.year = newYear;
  }
}

class ElectricCar extends Car {
  constructor(make, model, year, batteryCapacity) {
    super(make, model, year);
    this.batteryCapacity = batteryCapacity; // in kWh
  }

  getDetails() {
    return `${super.getDetails()} with a battery capacity of ${this.batteryCapacity} kWh`;
  }
}

const myCar = new ElectricCar('Toyota', 'Corolla', 2020, 50);
console.log(myCar.getDetails()); // Output: 2020 Toyota Corolla with a battery capacity of 50 kWh
myCar.updateYear(2021);
console.log(myCar.getDetails()); // Output: 2021 Toyota Corolla with a battery capacity of 50 kWh
```

#### Static

```js
class Car {  
  constructor(name) {  
    this.name = name;  
  }  
  static hello() {  
    return "Hello!!";  
  }  
}  
  
const myCar = new Car("Ford");  
  
// You can call 'hello()' on the Car Class:  
document.getElementById("demo").innerHTML = Car.hello();  
  
// But NOT on a Car Object:  
// document.getElementById("demo").innerHTML = myCar.hello();  
// this will raise an error.
```

### Objects

There are a few ways to create objects:
- Using an Object Literal
- Using the `new` Keyword(look above)
- Using an Object Constructor
- Using `Object.assign()`
- Using `Object.create()`
- Using `Object.fromEntries()`

#### Object Literals
are literal objects :)
```js
const myCar = {
	make: "tesla",
	model: "model T"
}
```



## The remaining
        
- Destructuring
    
- Spread & rest operators
    
- Promises / async–await
    
- Modules (import/export)

