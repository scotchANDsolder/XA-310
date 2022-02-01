### The Math() and Date() Objects

Two of the most commonly used bulit-in JavaScript objects are **Math()** and **Date()**.

Remeber that in JavaScript, objects are simply collections of any number of properties and/or methods, which are internal functions that return a result.

#### Math()
The [Math()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math) object has a number of features that allow you to perform more complex mathematical operations than simple addition, subtraction, multiplication, and division.

This object contains properties for specific values - like **Math.PI** for **π** - and methods like **Math.round(x)** (which returns a value rounded to the nearest integer) and **Math.random()** (which returns a pseudo-random number between 0 and 1). There are dozens of other methods, for finding square roots, the length of a hypotenuse of a triangle, the absolute value of a number, and so on.

One common use for math is to generate a random value using **Math.random()**. For example, say I want to generarte a random number between 0 and 255 in order to create a random HTML color value in RGB format (rgb(255,0,0) for example).

To do this, you need to perform three steps:

1. Call Math.random() to generate a (pseudo) random number between 0 and 1
2. Multiply this number by 255
3. Call Math.floor() to round down to the nearest whole number
```
let randomRGB =  Math.floor(Math.random() * 255);
```

Check your console to see this in action.

#### Date()
Calling the built in [Date()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) object creates a representation of a single moment in time.

**Date()** can be called with no parameters and will return the current time as a string:
```
console.log(Date());
```

However, a new **Date()** object can be created, or instantiated, by invoking it with the 'new' keyword:
```
console.log(new Date());
```

This results in a **Date()** object, which contains a numer of methods that you can query:

These values return numerical values (with the count starting at 0); it's up to the user to translate that day of the week and month of the year into a text value, because names of months and days of the week differ by language.

```
let dateObj = new Date();
let days = ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday'];
let months = ['January','February','March', 'April','May','June','July', 'August','September','October', 'November','December'];

let dayOfWeek = dateObj.getDay();
let monthOfYear = dateObj.getMonth();

console.log("Day of Week: " + days[dayOfWeek]);
console.log("Month of Year: " + months[monthOfYear]);
```


Finally, you can also provide values when creating a new **Date()** object; this will allow you to figure out what day of the week, for example, a particular date falls on:
```
let birthday = new Date('March 29, 1992');
console.log(birthday);
console.log(birthday.getDay());
```
