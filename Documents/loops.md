### JavaScript Loops
Looping, or iterating, over a list of things and performing a task for each result is a very common programming practice.

Imagine a list (or an array) of all your Twitter followers or a page of Amazon search results and needing to find the username or to add formatting to every item on the list; with the correct code, you can tell your JavasScript program to examine each iterm individually and to perform some action for each.

#### For Loops
Say that you have a simple array, named **colors**:
```
let colors = ["red","blue","green","yellow","orange"];
```

The simplest loop is a **for** loop, which will perform some action for each item in the list while also giving you an index number each time you traverse the loop:
```
let count;

for(count = 0; count < colors.length; count++) {
  console.log(colors[count]);
}
```

This code starts by creating a variable named "count" to act as placeholder for a number that is incremented each time the loop is iterated. In this case, the **count** variable is declared outside of the loop with no initial value.

The for loop begins by listing a series of conditions:
- set the value of **count** to 0, as computers always start counting at 0
- continue to run as long as the value of count is less than the number of items in the colors[] array (which is accessed through the arrayname.length property)
- increment the number by one each time you go through the loop so that you start with the following array item the next time

In plain English, this loop says "Start with the number zero, use that to access an item from the array by its index number, then log the value to the console. Then start the loop again, add one to the counter, and check the next index of the array. Keep doing this so long as the counter number is less than the number of items in the array".

So the first time through the loop, the value of **count** is zero, and **colors[0]** (red) will be printed to the console. The next time through the value of **count** is 1, so **colors[1]** (blue) is printed. The value of colors.length is 5, so this will happen five total times. On the sixth time, the value of count would be equal to 5 (since computers start counting at 0). Since 5 is not less than 5, the loop would stop.

#### Using array.forEach()
If the items that you want to loop through are in an an array, you can use the forEach() array method to do something for every item:
```
colors.forEach(tempName => console.log(tempName));
```

This is simpler in many ways, but doesn't provide you with a number indicating how many times you've gone through the loop (though there are ways to make this happen). The word "tempName" is arbitrary; you can use any valid JavaScript variable name to refer to each item while inside of the loop.

#### Nested Loops
Say you have a multidimensional array, like this:
```
let universities = [
	['Michigan State','East Lansing'],
	['University of Michigan','Ann Arbor'],
	['Wayne State University','Detroit'],
	['Michigan Technological University','Houghton']
];
```

If you wanted to print out all the values from here, you would have to loop through the inner array for every item in the outer array. This requires setting two counting variables, one for the outer array and one for the inner.

This example uses **i** and **j** as counter variables; **i** is commonly used for a loop counting variable name, and when multiple arrays are used **j** often comes next. This is just tradition and not a requirement.

```
var i;
var j;

for(i = 0; i < universities.length; i++) {
  for(j = 0; j < universities[i].length; j++) {
    console.log(universities[i][j]);
  }
}
```

Doing this with a forEach() would look like this:
```
universities.forEach(university => 
  university.forEach(properties => console.log(properties))	
);
```
