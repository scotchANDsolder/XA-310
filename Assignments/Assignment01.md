### Your First JavaScript Program

#### The Problem

Given an array of 50 US states and a separate array of 13 Canadian provinces, create a new third array that only shows items from each list that are 8 characters or longer; print this third array, sorted alphabetically, to the console.

You will use functions, loops, conditionals, and arrays to complete this.

#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

Detail this strategy and your logic using pseudo-code before you begin writing actual JavaScript.

1. Create an HTML document, named "yourlastname_01.html"
2. Inside a <script> tag, create a JavaScript program that:
   - Contains the two arrays below - one for the states, one for the provinces
   - Loops through each array
   - Calls a function for each item. The function should accept two arguments:
      - The name of a third array, where matches are stored
      - The length of the string needed for a match (in this case, the number 8)
    - If the string is **greater or equal to** eight characters, add the item to a new array
    - If the string is **less than** 8 characters, print "The string XXX is less than 8 characters" to the console
    - When finished with the loop, print out the list of matches, sorted alphabetically.

  You must submit your HTML file by uploading it to D2L by 5pm on the due date

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code and a document (preferably PDF) with your process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..

#### The Arrays:

```
const provinces = ["Alberta", "British Columbia", "Manitoba", "New Brunswick", "Newfoundland and Labrador", 
  "Northwest Territories", "Nova Scotia", "Nunavut", "Ontario", "Prince Edward Island", "Quebec", "Saskatchewan", "Yukon"]
```
  ```
  const states = ["Alabama", "Alaska", "Arizona", "Arkansas", "California", "Colorado", "Connecticut", "Delaware", 
  "Florida", "Georgia", "Hawaii", "Idaho", "Illinois", "Indiana", "Iowa", "Kansas", "Kentucky", "Louisiana", "Maine", 
  "Maryland", "Massachusetts", "Michigan", "Minnesota", "Mississippi", "Missouri", "Montana", "Nebraska", "Nevada", "New Hampshire", 
  "New Jersey", "New Mexico", "New York", "North Carolina", "North Dakota", "Ohio", "Oklahoma", "Oregon", "Pennsylvania", 
  "Rhode Island", "South Carolina", "South Dakota", "Tennessee", "Texas", "Utah", "Vermont", "Virginia", "Washington", 
  "West Virginia", "Wisconsin", "Wyoming"];
  ```
