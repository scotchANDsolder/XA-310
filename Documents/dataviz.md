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
Example of [CSV file](username.csv) that shows usernames and names of people. 


Some data sources
