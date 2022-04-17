# Final Project: Quantified Self

## DUE: Monday 4/29 by 5:00 pm

The goal of this project is for you to construct a story of yourself, using computational tools that you had learned this semester. You will log, collect, organize and make sense of data about yourself to develop a personal narrative that highlights patterns and insight in your own habits and daily life. 

Tracking and understand how you spend your time in day can be helpful (beyond just completing this project) and provide the following benefits:

- Gaining better control over your time time
- Developing and understanding how to be more realistic and organized
- You can get better at estimating how long your tasks take
- It can lead to being more productive
- You can learn how to single-task (vs. being distracted all the time by multitasking)

There are 3 parts of this assignment with each with its own deliverables.  All are required for complete submission.

## Part 1: Data Logging

To begin this project you will be first asked to collected data on yourself. This information will be used for the subsequent parts of the project, hence doing this properly will yield better results for analyses and reflection. 

Over this next week you should maintain a log your daily activities. You can do this in a notebook with pen/pencil or using Google Sheets on your phone. There is no optimal tool and you should decided what works best for your. Whichever way you decided to log your activities, I recommendation using a something that is easily accessible and something you can carry with you at all times. Some might prefer a small notebook that fits in their pocket or for most their phone works best. Either way make sure to log everything in the moment as things happen i.e. do not wait until the end of the day to recall the events of your day. You memory will fail you and you will be left with faulty data. Remember the point here is to discover new insights in your own behavior and so your data should be as true as a possible. 

You must maintain this log for at least 4 days, although I recommend doing it ever longer. Having more data to work with will give you better insights in yourself. You may pick any 4 days, but ensure you do this first before moving onto the next parts of the assignment. 

### How and What to log?

You should capture your data in 24 hours periods that are broken down in 1 hour intervals, beginning from 12: 00 AM and ending at 11:00 PM. 

You will log the following 4 activities throughout the day:

1. Amount of Water consumed
2. Your physical location
3. Sleep Time
4. Misc. : Choose any other aspect of your day that you would like to track. For example:
    - Cell phone use: text or call etc.
    - TV/Movie/YouTube Watch time
    - Exercise Time
    - Study Time...etc.

Record each activity in your log for each hour. Depending on the activity you are tracking you will enter the values next to the appropriate hour mark. For example for  **tracking water** you will enter the amount. In my example below I am tracking in ounces.  For **location** you will put name of the place where you were physically present during that hour mark and finally for **sleep** it would be a **yes or no**.  Here is a example log made in Google Sheets. Feel free to modify this as per your own needs:

Source:  [https://docs.google.com/spreadsheets/d/1QU214TazPp6f3P8aO77FWJkt7gwZsFqKD7ZVZaQ_5uo/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1QU214TazPp6f3P8aO77FWJkt7gwZsFqKD7ZVZaQ_5uo/edit?usp=sharing)

![Untitled](Final%20Proj%208f0d8/Untitled.png)

You will notice that I am using “Home” , “Campus” and “Restaurant” as possible options for the location column. You can create you own categories that you might find more suitable. Additionally for my Misc. activity I choose to track the times I was working on or using my laptop, which is captured as a “yes” or “no”.

### Deliverable

Log your activities for 4 days and create a table that shows this data. Submit a PDF of these table. You can format the tables in away you want as long as the required information is clearly indicated.

## Part 2: Sorting your Data

Once you have logged your data for 4 days, now you must transcribe it in to JavaScript for sorting and further analyses. In order to do this you will be ‘cleaning up’ your tables so that they can used in your JavaScript code.  We will converting this data into [JSON](https://www.w3schools.com/js/js_json_intro.asp), a data format that works exactly as [objects](https://github.com/scotchANDsolder/XA-310/blob/main/Documents/objects.md) in JavaScript.  Once we have our data in JSON format, we will be able to write algorithms for making inferences on our data. 

### Cleaning up the Data

Follow the steps outlined below to convert you data in JSON:

1. Tabulate Data: Begin by creating a table in either Google Sheet or MS Excel. If you have been gathering your data digitally you should already have it, but if you have been using a notebook ensure you have your data in a digital format.
2. Column Headings: In order of us to use JSON properly we must first clean up the headings for each of our column. Each column must contain only **one** word with no numbers, spaces or special characters. For example, in my example I will change my second column ‘Water (oz)’ to ‘water’. Additionally I will also change my time values from 12 hour format to 24 hour format. I will also update these values so they are represented by simple numbers ‘12:00 AM’ to ‘0’ , ‘1:00 AM’ to ‘1’......’1:00 PM’ to ‘13’ , ‘2:00 PM’ to ‘14’......etc. Here is example of before and after you have cleaned up the table

| **BEFORE** | **AFTER** |
| ------------- | ------------- |
| ![Untitled](Final%20Proj%208f0d8/Untitled%201.png)  | ![Untitled](Final%20Proj%208f0d8/Untitled%202.png) |

                                



                         



3. Converting to JSON: Select all the columns and rows in your table, including your column headings (each day should be done separately) and copy/paste it to this website: [https://csvjson.com/csv2json](https://csvjson.com/csv2json). This website will automatically generate a JSON for your table.  

![Untitled](Final%20Proj%208f0d8/Untitled%203.png)

4. Importing JSON: Copy and paste the generate JSON into a new JavaScript tag in an HTML file. Note that I am creating a variable to for this data. You will do this for all 4 years separately. 

![Untitled](Final%20Proj%208f0d8/Untitled%204.png)

5. Using JSON: Once you copy the JSON data in your text editor that it is a long array. Notice the square bracket in the beginning and end of the data. JSON is essentially a giant array of objects. And because it an an array you can access the data by calling on the array index and object key value. For example:

```jsx
console.log(day1[0]) // This will print the data for 12:00 AM

console.log(day1[0].location) // This will print 'Home' i.e. you location at 12:00 AM

console.log(day1.length) // This will print 24 i.e. the total hour of your data
```

I would recommend testing the you have correctly converted your data out before moving on to the next step.  You can test it by using the code examples in step 5.

6. At the end of this part you should have 4 giant object arrays (or JSON) i.e. day1, day2, day3 and day4 will all your logged activities.

### Making sense of your data

The next step is to write simple algorithms to make certain inferences on your data and more importantly about your behavior and daily habits. Remember your data is an array of objects and because it is an array, you can loop through the array and use the object key values to access the data.

### Deliverable

Write JavaScript code that computes the following:

1. Average water consumed per day
2. Average hours of sleep per day 
3. Average hours spent away from home, per day
4. Average hours when at home and not sleeping, per day
5. Location with most water comsuption over 4 days
6. Name of _most time spent at location_ outside of home

Additionally develop 3 other queries for your data based on the misc. activity you decided to log in Part 1. For example, in my case I chose to track the times I was working on or using my laptop. So my 3 additional questions could be:

1. Average computer usage
2. Average computer usage at home
3. Location with most computer usage

Just as for other assignments, create an HTML document named "yourlastname_01.html" and put all your code in the <script> tags. Ensure provide appropriate comments in the code that indicate your understanding of the logic of your program. 

## Part 3: Finding Patterns in yourself

Based on your findings from Part 2, write a min. 500 word analyses of what you found in your data. 

- Did you learn anything about yourself through this activity? Did you gain any insights in your daily habits?
- What were your observation about each of the 4 activities you logged for this project? Did anything stand out?
- Did you see any correlations between the various activities? Can you make any interesting inferences?

Additionally answers the following reflective questions:

- What were some limitation of this process?
- Do you think your computational results accurate represent your personal experience? if yes, how so? if no, why not?
- What could you do to get more accurate results and inferences?
- If you were to repeat this activity, what would you do differently?

## Submission Requirements

Zip all the documents listed below and upload on D2L by the due date

- PDF of logged activities from Part 1
- JavaScript Code from Part 2
- PDF of written analyses from Part 3
