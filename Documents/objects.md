### JavaScript Objects

#### Object Basics

We've already discussed variables, which are 'containers' for values in the form of strings, numbers, and booleans (true/false, yes/no).

We've also talked about arrays, which are lists of items, ordered in a particular manner and accessible by their index number.

JavaScript also uses another data type called an **object**.

From the Mozilla Developer Network's [working with objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects) intro:

> JavaScript is designed on a simple object-based paradigm. An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. In addition to objects that are predefined in the browser, you can define your own objects.

In JavaScript, the concept of objects permeate basically everything; most things in JavaScript are, at some level, an object - like the Date object, the Math object, the String object the Array object. These all have **properties** and/or **methods** that can be modified or read from to help you write your code.

#### Real-World Objects

A very common analogy for Objects is to compare them to cars - there can be many different types of cars, but they all have very similar properties and methods.

Properties of a car might include:

- make
- model
- year
- color
- number of cylinders
- range on a full tank of gas / charge
- number of doors
- number of seats
- automatic or manual transmission
- horsepower
- tire pressure

Methods associated with cars might include:

- drive forward
- drive in reverse
- accelerate
- brake
- shift
- turn on left turn signal
- spray the blue stuff on your windshield
- turn on AC

Not all cars have all of these properties or methods - electric vehicles don't have any cylinders, older cars don't have air conditioning, etc. But every car can be describe with an ojbect.

#### Creating an Object in JavaScript
An object can be created using curly braces:
```
let testObject = { };
```

This creates (or instantiates) an object named **testObject**; checking the console displays this:
```
console.log(typeOf(testObject)); // prints "object"
```

Here is an object that contains information about a person:
```
const person = {
  firstname: "John",
  lastname: "Doe",
  previousCities: [
    "Detroit",
    "Denver",
    "Atlanta"
  ]
}
```

In this object, there are three different keys, each with an associated value.

The first two keys, **firstname** and **lastname**, have the values "John" and "Doe" (both strings) assigned to them, respectively. The last key **previousCities** - has an array of strings as its value.

#### Adding to an Object
You can add more key/value pairs to an object at any time:
```
person.middlename = "Kriss";
```

#### Differences From Arrays

So far, this isn't all that different from data structures that we've seen using arrays or multidimensional arrays, other than using a keyword to access properties instead of an array index.

Objects can have properties with values of any type - strings, numbers, booleans, arrays, other objects, etc.

The main difference is that objects can also use the output of a function to provide that value, meaning that value can be generated when the code is run and can change based on external parameters; in this case these functions are called _methods_:
```
person.age = function() {
  let currentDate = new Date();
  let currentYear = currentDate.getFullYear();
  let birthYear = 1984;
  return(currentYear - birthYear);
}
```
Hard-coding an age into the object would make no sense; it would work for a year, then never be correct again unless your code was updated. Using a method allows this value to change as other variables that determine the age change - in this case it uses the current year value to calculate the age.
