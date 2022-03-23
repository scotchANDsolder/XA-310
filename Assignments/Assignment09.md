### Student Objects
**DUE 3/30**

#### The Problem
For this assignment, you will need to create a JavaScript object contrustor that abstracts various properties and methods of a student at MSU. 

The Student object constructor must contain the following properties:
-  A string for their name
-  A string for their major
-  A string for their college standing i.e. Freshman, Sophomore, Junior or Senior
-  Date of birth: Date() object
-  Current Class Load: Array of string that are names of classes. For example: ["XA 310","ENG 101","STA 419"]

The Student object constructor must contain the following methods:
- CurrentAge: Determined by calculating years passed since their year of birth.
- YearsLeftToGraduate: Determined by calculating years left based on their college standing. Assume everyone will graduate in 4 years.
- CurrentCredits: Determined by number of classes. Assume each class is 3 credits 



#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

1. Create an HTML document, named "yourlastname_09.html"
2. Inside a <script> tag, create a JavaScript program that does the following:
   - Create a Student _object constructor_ with properties and methods as described above
   - Create 10 MSU student by [instantiating](Documents/MoreObjects.md) with the Student object constructor. Feel free to make up all the properties in the constructor.
   - Add these 10 MSU student objects to an array
   - Loop through the array and print out the following:
      - Names of students who are 20 years or older
      - Names of students who have 3 years left to gradaute
      - Names of students who are enrolled in 9 credits or more
  
  
  
  

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code with proper comments that showcase your process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..
