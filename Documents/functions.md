### Functions
From https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions, the "official" Javascript reference:
> Generally speaking, a function is a "subprogram" that can be called by code external (or internal in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function, and the function will return a value.

Functions are blocks of code that can be called by other code. You can pass values, also known as **parameters** or **arguments**, to the function for it to use internally.

A function is created using the **function** keyword:
```
function functionName() {
  // here is where you put all
  // the code you want the function to do
}
```

Parameters can be passed to the function by listing them in the parentheses.

To access the values passed to this function, you use the arbitrary variable names you make up - in this example, 'parameter1' and 'parameter2':
```
function functionName(parameter1,parameter2) {
  // again, put your code here
}
```

Functions can return values, variables, or other information. All this one does is to add two parameters together and return them:
```
function addNumbers(one,two) {
  return one + two;
}
```

Finally to call our function **addNumbers**, we can do the following:
```
var sum;
sum = addNumbers(10,4);
console.log(sum); //This will pring out 14 i.e. the output of our function
```

This example works but has a couple of issues to be aware of - mostly, how do you know if the parameters are actually numbers? JavaScript won't complain if they aren't and will combine them together regardless, possibly returning a string instead of a number.

Writing any code means thinking about what could possible go wrong and to try to allow for any possible situations that might occur. A better example for something named "addNumbers()" is to make sure all the parameters are actually numbers:
```
function addNumbers(one,two) {
  if(isNaN(one) || isNaN(two)) {
    return "Error: Parameters must be numbers"
  }
  else {
    return one + two;
  }
}
```

This function now has an if statement that uses the built-in JavaScript "isNaN()" function to see if either parameter one or parameter two is not a number.

If either value is not a number, it returns an error message; otherwise it adds the two numbers and returns the sum.

Functions are incredibly useful because they can simplify programming by isolating and abstracting common tasks that can be used over and over by other aspects of the program.

The internal workings of a function can be irrelevant to a programmer, as long as they know what parameters to pass, and what values to expect in return.

These internal workings can be fine-tuned, reconfigured, or played with in any number of ways to improve the program and as long as the parameters and return values work the same, all will be fine.

Functions can call other functions:

```
function randomRGBNumber() {
  let number = Math.floor(Math.random() * 256);
  return number;
}

function rgb() {
  return "rgb + randomNumber() + "," + randomNumber() + "," + randomNumber() + ");";
}
```

This example shows a function named ***rgb()*** that generates a random RGB value by calling another function three times to get a random number between 0 and 255.

Instead of having to write 'Math.floor(Math.random() * 256)' over and over, you can just ask that function to do the calculation for you and build a valid RGB string by adding the necessary commas and parentheses.


#### Some helpful Functions
- [prompt()](https://www.w3schools.com/jsref/met_win_prompt.asp) : Asks for an input from the user
- [parseInt()](https://www.w3schools.com/jsref/jsref_parseint.asp): Converts String to Integers. Very helpful when taking inputs from the user
- [Math.random()](https://www.w3schools.com/js/js_random.asp): Returns a random number between 0 and 1
- [Math.floor()](https://www.w3schools.com/jsref/jsref_floor.asp): This rounds a number DOWNWARDS to the nearest integer, and returns the result.
  - Math.random() used with Math.floor() can be used to return random integers. 
 
