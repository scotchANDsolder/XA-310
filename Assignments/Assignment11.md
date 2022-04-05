### Data Visualization
**DUE 4/13**

#### The Problem

Given a dataset of parking citations in New York city, create a data visualization that plots geographically the location of each parking ticket.

You will use the CSV file hosted here: https://raw.githubusercontent.com/scotchANDsolder/XA-310/main/Documents/parkingCitations.csv

This dataset contains the following columns:
- Borough: Queens, Manhattan, Staten Island, Brooklyn and Bronx
- Latitude: Ranging from 40.477399 to 40.969485
- Longitude: Ranging from -74.329001 to -73.669821

Each parking ticket location should displayed as a tiny circle and spatially located based on its Latitude and Longitude. The circle of each color should also correspond to the Borough the parking ticked was issued in. For example: Queens can be yellow, Bronx can be blue ...etc.

The final output should look something like this:

![image](https://user-images.githubusercontent.com/70717743/161852969-2c13d971-503c-4b69-abdf-a7d897c9f0d7.png)



#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

1. For this assignment you will be coding in the **sketch.js** file.
2. Read in the  CSV file by using the following command:
```
table = loadTable('https://raw.githubusercontent.com/scotchANDsolder/XA-310/main/Documents/parkingCitations.csv', 'csv', 'header');
```
3. Read in the Borough, Latitude and Longitude columns to create 3 separate arrays. 
4. Loop through these arrays and plot circles in the following way:
   - Scale the latitude data from its orignal values to the width of your canvas. HINT: [We did this in our class example](Documents/dataviz.md#another-example).
   - Scale the longitude data from its orignal values to the height of your canvas.
   - Check which Borough the particular data belongs to and assign it a color
   - Draw a circle accordingly  
  
You must submit your HTML file by uploading it to D2L before class on the due date
