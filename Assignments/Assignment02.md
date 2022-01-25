### The Guessing Game
**DUE 2/2**

#### The Problem

Create a game wherein the user has to guess a number, between 1 and 10 randomly picked by the computer. The user gets 3 tries to guess the number correctly. 
Additionally the computer gives the user some feedback as to how far the guess is from the actual number.

For example, let's say that the computer picks the number 8:
- If the user's first guess is 3, then the computer should reply "Too low, try again"
- If the user's second guess is 9, then the computer should reply "Too high, try again"
- If the user's third guess is 8, then the computer should reply "Bingo...correct guess! You win!"
- But if user's third guess is 6, then the computer should reply "Sorry you lost. My number was 8"

You will use functions and conditionals to complete this assignment.

#### Getting Started
Plan your strategy - decompose the problem into smaller, discrete parts that you can solve individually.

Detail this strategy and your logic using pseudo-code before you begin writing actual JavaScript.

1. Create an HTML document, named "yourlastname_02.html"
2. Inside a <script> tag, create a JavaScript program with the following:
    - Put a random number between 1 & 10 and assign it to a **const** variable
    - Create a function called **checkGuess()** that takes in 2 parameter i.e. the random number and the user's guess
      - This function will compare these 2 numbers and provide the apporiate feedback to the user using console.log (as shown above in the problem statement)
    - Use the **prompt()** function 3 times to get a reponse from the user and call the **checkGuess()** to verify the guesses
 3. **Bonus**: Can you stop the program if the users get the correct answer on the 1st or 2nd try?
    - HINT: You will have to use another varible that checks if the number has been guessed or not. If the user has guess it correctly, then there is no need to prompt the user again for an input.
   
You must submit your HTML file by uploading it to D2L *before class* on the due date

#### Submitting Your Work
You must submit a single HTML document containing your JavaScript code and a comment thoroughly to indicate your thought process - how you started to think of the problem, what steps you needed to take, what was important to focus on, etc..
