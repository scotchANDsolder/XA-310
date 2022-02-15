### Creating House Objects
**DUE 2/23**

You have just been hired as a web developer at [Trulia](www.trulia.com). Congratulations! As your first task at your new job you must prove to your team that you have a good understanding of JavaScript Objects.

#### The Problem

Create an object for a House listing that might be listed on Trulia's webpage. 

1. The object must contain the following **_properties_**:
  - Current Price (number)
  - Size in square footage  (number)
  - Address (string)
  - Year Built (date)
  - Number of Rooms (array of  3 numbers signifying bedrooms, bathrooms & garage, in that order)
```
//example:
var rooms = [3,2,0] // means 3 bedrooms, 2 bathrooms and 0 garage)
```
  - Date of last improvements (date)
  - History of date sold and selling price (2d array of date sold and corresponding price)
```
//example:
var sellingHistory = [ [ 2/23/1990, 120000] , [ 8/19/2003 , 150000] ] 
``` 
  - Is the house currently on the market? (boolean i.e. yes/no or 1/0)
  - Any landmarks (string)

2. Additionally the object must contain the following **_methods_**:
  - displayHouse(): This function prints out to the console the features of the house in the following order:
    - Current Price is $X
    - Number of rooms (e.g. There are 3 bedrooms, 2 bathrooms and 1 garage etc.)
    - Size
    - Last selling price and date
    - Landmarks
  - sellHouse(): This function accepts a new selling price as an argument and checks:
    - If the house is on the market then:
      -  Update the Current Price to the new selling price 
      -  Updates the selling history accordingly
      -  Takes the house off the market
    -  If the house is off the market then print out "Not accepting offers at this time"
  - houseImproved(): This function accepts 2 arugments. The first is the name of a room ( ie. 'bedroom', 'bathroom' or 'garage') and a number (i.e. the number of rooms to added to the house) and does the following:
    - Increases the Current Price of the house. Each bedrooms adds $2,000, each bathroom adds $1,000 and each garage adds $5,000 to the price.
    - Updates the date of last date of improvement.



#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

1. Create an HTML document, named "yourlastname_05.html"
2. Inside a <script> tag, create a JavaScript program that does the following:
   - Create a House object with properties and methods as described above. Feel free to make up the values of each of the variables (Set the currentlyonMarket ver
   - Verify that the _displayHouse()_ function works properly
   - Add 2 bedrooms
   - Call _displayHouse()_ to verfiy the bedrooms were added
   - Add 1 garage
    - Call _displayHouse()_ to verfiy the garage was added
    - Sell the house. You can put any selling price.
    - Call _displayHouse()_ to verfiy the house was sold
  

  You must submit your HTML file by uploading it to D2L before class on the due date

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code with proper comments that showcase your process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..
