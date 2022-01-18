### Making Decisions
**DUE 1/26**

Congratulations you have just been elected a the Chief of the Transportation for the [House Atreides](https://dune.fandom.com/wiki/House_Atreides)! As you assume command of the space fleet, it dawns on you that with great power comes great responsibility. 

Leto Atreides, the head of 
House Atreides needs you to determine a way to ship all supplies needed for the settlement on planet Arrakis as quickly and efficiently as possible. You must not let him down!

Your head of Logistics Col. Sheila Lamar knows that this will be difficult task. Mainly because your fleet has many different ships with many different carrying capacities. She has requested that you create a calculator for each ship crew so that they can determine what can safely be loaded and transported to Arrakis.

#### The Problem

Given the load capacity of a particular ship, write a program that prints out its Cargo Manifest i.e. a list of all items that can be carried safely on board. Each item has a specific weight so you must ensure that your do not overload the ship!

You will use variables and conditionals to complete this assignment. 

#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

Detail this strategy and your logic using pseudo-code before you begin writing actual JavaScript.

1. Create an HTML document, named "yourlastname_01.html"
2. Inside a <script> tag, create a JavaScript program that does the following:
   - Begin by declearing the ship load capacity varible (see below) 
   - Create your own variables for all the items to be shipped. Set them as either 1 or 0 depending on whether you want to put them on the ship or not.
   - Using multiple if statements check if an item is loaded on the ship or not and print the name of the item to the console
   - Add all the weights of the loaded supplies.
   - If the total weight is *less* than load capacity of the ship then print "Items loaded safely and ready to depart" to the console
   - If the total weight is *more* than load capacity of the ship then print "Overloaded, try again" to the console.
    - You may try again by changing the variables for items to 1 and/or 0  

  You must submit your HTML file by uploading it to D2L by 5pm on the due date

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code with comments that show your process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..

#### The variables:

Ship load capacity in the Atreides fleet. These weights are in **metric tons**

```
const ImperialTransporterCapcaity = 5 // metric tons

```

List of items to be shipped & their weights. These weights are in **kgs** 

- Food: 1500 kgs 
- Weapons: 1900 kgs
- Ammos: 750 kgs  
- Building Constructions Supplies: 2400 kgs  
- Zero Gravity Basket Ball Supplies: 100 kgs
- Transport Rover: 1200 kgs
- Backup Power Generators: 1500 kgs
- 
  
