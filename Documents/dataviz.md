## What is data visualization?

From [TechTarget.com](https://www.techtarget.com/searchbusinessanalytics/definition/data-visualization)...


>Data visualization is the practice of translating information into a visual context, such as a map or graph, to make data easier for the human brain to understand and pull insights from. The main goal of data visualization is to make it easier to identify patterns, trends and outliers in large data sets. The term is often used interchangeably with others, including information graphics, information visualization and statistical graphics.

> Data visualization is one of the steps of the data science process, which states that after data has been collected, processed and modeled, it must be visualized for conclusions to be made. Data visualization is also an element of the broader data presentation architecture (DPA) discipline, which aims to identify, locate, manipulate, format and deliver data in the most efficient way possible.

Some Examples of [Data Visualization](https://www.tableau.com/learn/articles/best-beautiful-data-visualization-examples)


## Displaying Data
NOTE: All the examples below are for p5.js i.e. you will be coding in the [sketch.js](p5js.md) file in either the draw or setup function.

### Simplest Data Visualization
As we’ve seen before,_ for loop_ helps to repeat actions in our programs. For the first example we are going to put our data in an array. 
This array can contain any set of data like population, age, location etc. For now we will just put random numbers. 

To read the value of an array, we can use the for loop to cycle through the data.
```
function setup() {
let num = [10,20,30,40]
  for(let i=0; i<num.length; i++){
      print(num[i])
    }
}
function draw() {
}
```
This code will print our data to the Console.

We can now display this data by creating circle of different sizes based on the value of the data in the array. Using the following code we will get:
```
function setup() {
  createCanvas(400, 400);
  background(220);
  let num = [10,20,30,40]
  for(let i=0; i<num.length; i++){
      circle(width/2, i*100 + 50, num[i])
    }
}
function draw() {
}

```

![image](https://user-images.githubusercontent.com/70717743/161839635-52f487f1-f309-43e3-aaf1-98ce33a5afbd.png)


### Reading data from CSV files
Majority of the time we do not put our data directly into our code instead we read them from files containing the dataset. In this example we will read data from a CSV file i.e. _common seperated value_ file.

Example of [CSV file](https://raw.githubusercontent.com/scotchANDsolder/XA-310/main/Documents/username.csv) that shows usernames and names of people. 

CSV files can be opened in MS Excel. Doing so shows you all the columns with all the data. To do so, click on the link above and then right click and select save-as. This should download the CSV file to your computer. 

To read the data in p5.js we will need the following commands:
```
let table = loadTable(“username.csv”, “csv”,”header”);

let numRows = table.getRowCount();

let fNAme = table.getColumn(“First name”);
```
[loadTable()](https://p5js.org/reference/#/p5/loadTable) will load the dataset from the CSV file into p5.js. While getRowCount() gets the number of rows in the file. We can also select specific data from the columns by calling getColumn(). In out example above _fName_ become an array contain all the elements in the _First name_ coloumn. 

### Another Example
Let's do a deep dive into the following code. We are using this [CSV file](data.csv) for this example: 

```
let table;

//load the CSV before the program runs
function preload() {
  table = loadTable('https://raw.githubusercontent.com/scotchANDsolder/XA-310/main/Documents/data.csv', 'csv', 'header');
}

function setup() {
  createCanvas(400, 400);
  background(220);

  //get the amount of rows in the CSV
  let numRows = table.getRowCount();
  print(numRows);
  //get all the Columns from the CSV file 
  let happyIndex = table.getColumn("Happy Index");
  let state = table.getColumn("State");
  let region = table.getColumn("Region");
  

  //iterate over the number of rows
  for (let i = 0; i < numRows; i++) {

    //use the value of i to move the rectangle down
    let mover = 20 + (i * 20);
    let newIndex = map(happyIndex[i], 0, 10, 10, 200);
   

    let col = 0;
    if (region[i] == "East") {
      col = color('#bab39e');
    } else if (region[i] == "West") {
      col = color(255, 0, 0);
    } 


    print(col);
    fill(col);
    //change the length of the rectangle 
    //based on the Happy Index
    rect(50, mover, newIndex, 10);

    //write the state name to the 
    //screen before each rectangle
    textSize(10);
    text(state[i], 20, mover + 10);

  }
}
```

- You will notice we are using a URL in the loadTable() function. This is because local CSV cannot be opended in the browser. So we must host our CSV file online somewhere so we can access it. In this example we are hosting our CSV file on Github. 
- We are also using a new function i.e [map()](https://p5js.org/reference/#/p5/map). This function changes the range of a particular data. In our example, the Happy Index ranges from 0 to 10 but we are scaling this to 10 to 200 so that we can draw the corresponding rectangle.

The visualization looks like this:

![image](https://user-images.githubusercontent.com/70717743/161847352-0670c4c1-d8af-4aa8-89d6-2ae26a36ed8b.png)

