### Working with Arrays
**DUE 2/16**

#### The Problem

Given a two dimensional array of 50 US states and the number of National Parks in each state (See below), create 3 new arrays which have the following:
- 1st Array: States with more than & equal to 4 National Park
- 2nd Array: States with 1 to 3 National Parks
- 3rd Array: States with no National Parks 

Sort each of these arrays alphabetically and print out their contents to the console, including how many states there are in each category.

For example:
- There are 4 states that have 4 or more National Parks. They are Alaska, California, Colorado and Utah

... etc.

You will use functions, loops, conditionals, and arrays to complete this.

#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

Detail this strategy and your logic using pseudo-code before you begin writing actual JavaScript.

1. Create an HTML document, named "yourlastname_03.html"
2. Inside a <script> tag, create a JavaScript program that:
   - Contains the state array below
   - Create 3 empty arrays for each category as described above
   - Loops through each item in the array
   - Calls a function for each item in the array. The function should accept 2 arguments:
      - The name of the state
      - The number of national parks in the state
    - In the function add items to the newly created arrays according to the logic described above
    - When finished print out the numbers of items in each array along with their contents, sorted alphabetically.

  You must submit your HTML file by uploading it to D2L before class on the due date

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code and a document (preferably PDF) with your process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..

#### The Arrays:

```
const states = [
 ["Virginia", 0],
 ["Nevada", 1],
 ["New Hampshire",0],
 ["Alabama",0],
 ["Maryland", 0],
 ["Massachusetts", 0],
 ["New Jersey", 0],
 ["New Mexico",2], 
 ["Utah",5], 
 ["Vermont",0], 
 ["Connecticut",0], 
 ["Delaware",0],
 ["Maine",1],
 ["Oklahoma",0], 
 ["Oregon", 1],
 ["Pennsylvania", 0],
 ["Rhode Island", 0],
 ["Arizona", 3],
 ["Arkansas",1], 
 ["California",9],
 ["Colorado",4], 
 ["Minnesota", 1],
 ["Illinois", 0],
 ["Indiana", 1],
 ["Iowa", 0],
 ["Kansas", 0],
 ["Florida", 3],
 ["Georgia", 0],
 ["Hawaii", 2],
 ["Michigan",1], 
 ["South Dakota", 2],
 ["Tennessee", 1],
 ["Texas", 2],
 ["Mississippi", 0],
 ["Missouri", 1],
 ["Montana", 1],
 ["Nebraska", 0],
 ["Idaho", 0],
 ["Washington", 3], 
 ["West Virginia", 1],
 ["Wisconsin", 0],
 ["Wyoming",2],
 ["New York", 0],
 ["North Carolina",1], 
 ["North Dakota", 1],
 ["Ohio", 1],
 ["Alaska", 8],
 ["South Carolina",1], 
 ["Kentucky", 1],
 ["Louisiana", 0]]
```

