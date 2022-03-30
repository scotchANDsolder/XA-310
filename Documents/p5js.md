# Intro to p5.js

### What is p5.js?
From their [website](https://p5js.org/)....
> p5.js is a JavaScript library for creative coding, with a focus on making coding accessible and inclusive for artists, designers, educators, beginners, and anyone else! p5.js is free 
and open-source because we believe software, and the tools to learn it, should be accessible to everyone.


Some examples of what is possible with p5.js:
- [Open Processing](https://openprocessing.org/browse/#)
- [Happy Coding](https://happycoding.io/examples/p5js/)
- [From p5.js](https://p5js.org/examples/)

### Why use p5.js?
p5.js is designed for coders who want to create interactive, visual programs that run directly in a web page. It’s designed for creative coding, and it sits 
right at the intersection of coding and art.

Behind the scenes, p5.js is a JavaScript library, which runs inside of an HTML web page.


### How to use p5.js?

In order to use p5.js you will have to reference the library in your html file. 

1. Create an **index.html** file and copy and paste the following code:
```
<html>
  <head>
    <script src="https://cdn.jsdelivr.net/npm/p5@1.4.1/lib/p5.js"></script>
    <script src="sketch.js"></script>
  </head>
  <body>
    <main>
    </main>
  </body>
</html>
```

You will notice a url in the first script tag. This is a link to the p5.js that is hosted online. Next you will notice a file name i.e. _sketch.js_ in the second script tag. This is a new file you will create where your p5.js code will go.

2. Create a **sketch.js** file and copy and paste the following code:
```
function setup(){
  createCanvas(200,200)
}

function draw(){
  rect(100,100,50,80)
}
```

3. Ensure both files are in the same folder. Then open the index.html file in the browser. If everything was done correctly, you should see a rectangle with a width of 50  pixels and a height of 80 pixels.

### Anatomy of a p5.js sketch

p5.js programs are often called sketches to evoke the feeling of doodling on a piece of paper. Just like you don’t have to know what the end result will look like when you start doodling, you don’t have to know what the end result will look like when you start coding.

p5.js has its own syntax, which at times can be very similar to JavaScript. You will notice that there are 2 functions in the sketch.js file i.e. **setup()** and **draw()**. These functions
are needed for p5.js to work properly and without them you might get the expected result. 

What are these functions? 
(from: https://medium.com/comsystoreply/introduction-to-p5-js-9a7da09f20aa)
> The setup() function is called once when the program starts. It’s used to define initial environment properties such as screen size and background color and to load media such as images and fonts as the program starts.
Called directly after setup() , the draw() function continuously executes the lines of code contained inside its block until the program is stopped […].

![image](https://user-images.githubusercontent.com/70717743/160692775-86c20902-31d1-4606-9413-a5e15ff7a2d7.png)


You will also see a command **createCanvas(200,200)**. This commands creates a blank canvas of 200 pixels by 200 pixels (just like a painter would) in the HTML webpage on which we can create all kinds of graphics. The first number in function is the width of the canvas, while the second number is the height. [More here](https://p5js.org/reference/#/p5/createCanvas).

In p5.js the coordinate systems of pixels begins in the top left corner of the screen. For example: 
![image](https://user-images.githubusercontent.com/70717743/160693787-385f84e9-0056-4dcf-87d7-8a7ead1a6bec.png)

You can also understand how the coordinate system works by changing the numbers in the rect() command. It has the following syntax:
- rect(x,y,width, height)

<img src="https://user-images.githubusercontent.com/70717743/160696530-a940d397-6290-4699-9a71-389754f44df0.jpg" width="50%">

All p5.js commands can be found in the [refrence section](https://p5js.org/reference) of the p5.js website. 

### Your first p5.js sketch!
- Try adding some of these [shapes](https://p5js.org/reference/#group-Shape)
- Adding Color:
  - [Colors](https://p5js.org/learn/color.html) in p5.js are represented by 3 number i.e. Red, Green and Blue. Combing these 3 numbers in different ways you can have virtually any color 
  - The following commands are helpful when using color:
    - background(r,g,b) - Sets the color of the canvas
    - fill(r,g,b) sets the color used to fill shapes
    - noFill() disables filling
    - stroke(r,g,b) sets the color used to draw lines and borders around shapes
    - noStroke() disables drawing the stroke
    - strokeWeight(x) sets the width of the stroke used for lines, points, and the border around shapes (in pixels)


