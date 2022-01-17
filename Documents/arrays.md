### Arrays
Imagine you have a collection of chemical elements. If there were only a few, you could make variables for each:
```
let element1 = "Hydrogen";
let element2 = "Helium";
let element3 = "Lithium";
let element4 = "Beryllium";
```

But there are actually 118 elements, and it would be nice to store them together as a group (because they are all related conceptually), and allow you to access them individually or to perform a task for ever item in the group.

In JavaScript (and many other programming languages), this data type is called an array. Arrays are another type of variable, but instead of holding a single value - like a boolean, string or number - it can hold any number of these items. You can access each item by its index, which is the order in which it appears in the array.

#### Creating Arrays
Arrays in JavaScript are created like other variables - by using let, or const - but include a set of **square brackets** around a list if items separated by commas:

An array from the values above might look like this:
```
let elements = ["Hydrogen", "Helium", "Lithium", "Beryllium"];
```
This is an array containing four strings of text, but arrays can contain any number of items of any number of types of data - strings, booleans, or numbers. Strings have to be wrapped in single or double quotes, other values do not.
```
let numberArray = [1,2,3]; // three numbers
let mixedArray = ["one",2,false]; // a string, number, and boolean
```

You can access elements in an array using the array's index, or the order in which it occurs in the array. Using the array's name with an index number in square brackets will give you the value stored at that index number.

One important fact to remember is that the array index (as well as a lot of situations using numbers in computing) begins at 0:
```
let elements = ["Hydrogen", "Helium", "Lithium", "Beryllium"];

console.log(elements[0]); // prints "Hydrogen"
console.log(elements[2]); // prints "Lithium"
```

##### Arrays Declared with const
Declaring variable names with const works with arrays - you can never re-declare any variable using the same name, but you can add and remove elements from the declared array with no issue.

#### Array Properties and Methods
There are a number of array *properties* that you can access and methods, or operations, that can be performed on arrays.

Properties are accessed by using *.propertyName* at the end of the array you are asking about, while methods use the *.methodName()* structure.

You often want to find out how many items are in an array, which can be accessed using the .length property:
```
let elements = ["Hydrogen", "Helium", "Lithium", "Beryllium"];
console.log(elements.length); // prints 4
```

You can add an element to the end of an array using the .push() method:
```
elements.push("Boron");

console.log(elements); 
// prints Array(5) [ "Hydrogen", "Helium", "Lithium", "Beryllium", "Boron" ]
```

You can remove the last element using .pop():
```
elements.pop();

console.log(elements); 
// prints Array(4) [ "Hydrogen", "Helium", "Lithium", "Beryllium"]

```

#### More Complex Arrays
Arrays can hold any number of any types of values - including other arrays. These are sometimes referred to as multidimensional arrays.

Using our elements from above, perhaps you want to store the element's atomic weight and abbreviation along with the name; you could use an array of arrays to do this:
```
let hydrogen = ['H', 1];
let helium = ['He', 2];
let lithium = ['Li', 3];
let berylium = ['Be', 4];

elements = [hydrogen,helium,lithium,berylium];
```
If you use console.log to display the elements array, it'll look like this:
```
(4) […]
0: Array [ "H", 1 ]
1: Array [ "He", 2 ]
2: Array [ "Li", 3 ]
3: Array [ "Be", 4 ]
length: 4
```

This is showing that each element in the array is itself an array, with two items in it.

To access these sub-arrays, you need to add an additional index to narrow things down. For example, to get array index 0 (the abbreviation) from the element in the second slot in the elements array, you would do this:
```
console.log(elements[1][0]);
```
This is saying "find the element from index 1 in the elements array (so, Helium), then tell me the value of index 0". This will print out "He" to the console.

#### More Information
There are many more array methods and properties to work with, for sorting, reversing, getting only a small section of the array, and many others:

- https://www.w3schools.com/js/js_array_methods.asp
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array
