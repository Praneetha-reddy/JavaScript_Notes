### Call back functions
Callback functions are a fundamental concept in javascript which allow to pass another function as an argument. The function which receives the another function as an argument calls it in later point of time.
#### Here's how callback functions work
1. Create a function which performs some specific task.
2. When calling another function, pass this first function(the callback) as an argument.
3. The function called receives the first function as an argument and then executes the callback at later point of time.
   It may happen
   
     **a. After receiving function finishes its task.**
     
     **b. When an event occurs and triggers the call back function.**

_**Example Code**_
```javascript
const greet = function(){
   console.log("Welcome to Javascript learnings");
}
document.querySelector(".button").addEventListener("click", greet); //Here greet is callback
```
addEventListener triggers greet function when button with classname button is clicked.

### First Class and Higher order functions
1. Javascript treats functions as first-class citizens.
2. That means functions are simply values.
3. Functions are just another type of Object.
   
_**Example Code**_
```javascript
   const greet = function(){
   console.log("Welcome to Javascript learnings"); //Functions can be stored as values.
}
```
```javascript
const lufthansa = {
     airline: 'Lufthansa',
     iataCode: 'LH',
     bookings: [],
      book: function(flightNum, name) {
         console.log(
         `${name} booked a seat on ${this.airline} flight ${this.iataCode}${flightNum}`
       );
      }   //Can be stored in properties.
 };
```
And function can be passed as an argument to the another function. Please refer example code of callback function.

### Higher order functions.
A function that receives another function as an argument, returns another function, or both.
_**Example_code:**_
```javascript
document.querySelector(".button").addEventListener("click", greet); //Here addEventListener is a higher order function which receives greet function as an argument.
```
_**Example_code**_
```javascript
const greet = function(){
   return function(){
      console.log("Welcome to Javascript Learnings"); //greet function returns another function
   }
}
const greetings = greet(); //which inturn received by greetings variable.
greetings();
```
### Call and Apply Method
#### Call method:
Using Call method is a advanced way of calling method which explictly assign object reference to **this** key inside the method.

**Syntax:**
_[function_name].call([object_name], arg1, arg2,.....,arg3)_

_**Example Code**_:

```javascript
const lufthansa = {
     airline: 'Lufthansa',
     iataCode: 'LH',
     bookings: [],
      book: function(flightNum, name) {
         console.log(
         `${name} booked a seat on ${this.airline} flight ${this.iataCode}${flightNum}`
       );
      }   //Can be stored in properties.
 };

const eurowings = {
   airline: 'Eurowings',
   iataCode: 'LH',
   bookings: []
}

const book = lufthansa.book;
book.call(eurowings, '123', 'ABC');  //this keyword inside book method points to the eurowings object.
```
This can be useful when you want to use a function defined for one object with another object.

#### Apply method:
Apply method is similar to call method. The key difference lies in passing arguments.

In apply method we pass arguments as an array.

**Syntax:** _[function_name].call([object_name], [arg1, arg2,.....,arg3])_

object_name: the object which **this** keyword should refer inside the method.

[[arg1, arg2,.....,arg3]: an array of arguments are passed.

The usage of apply method can be replaced with call method by using spread operator.

### Bind method
It returns a new function, allowing you to pass any number of arguments.

**Syntax:**

bind(thisArg)

bind(thisArg, arg1)

bind(thisArg, arg1, arg2)

bind(thisArg, arg1, arg2, /* …, */ argN)

_**Example code:**_
```javascript
//Creating two different objects.
const book1 = {
   Name: 'The power of five',
   Author: 'Anthony Horowitz'
}
const book2 = {
   Name: 'The Monk who sold his Ferrari',
   Author: 'Robin Sharma'
}
const bookDetails = function(){
   console.log(`The book ${this.Name} was written by ${this.Author}`)
}

const detailsBook1 = bookDetails.bind(book1); 
const detailsBook2 = bookDetails.bind(book2); 
detailsBook1();  // this keyword inside the function always points to the book1 object.
detailsBook2();  // this keyword inside the function always points to the book2 object.
```
 

















