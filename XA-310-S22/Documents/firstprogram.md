## Getting Started With JavaScript
According to Wikipedia:

> JavaScript (often abbreviated as JS), is a high-level, interpreted programming
language. It is a language which is also characterized as dynamic, weakly
typed, prototype-based and multi-paradigm. Alongside HTML and CSS, JavaScript
is one of the three core technologies of World Wide Web content engineering. 

### What does all that mean?
The description above means that JavaScript, as a programming language, is:

- high-level, or very abstracted from the internal workings of the computer
- interpreted and dynamic, meaning the code is executed at runtime by an interpreter instead of being compiled into machine language, and can add new code or otherwise extending itself while being interpreted
- weakly typed, meaning that variables (named containers that refer to values that might change throughout the program) might be strings of text, decimal numbers, or other JavaScript code without having to be declared up front

### What can JavaScript do?
JavaScript is primarily used to augment the behavior of web pages, and can be used to do things like:

- React to a user's actions, like clicking on a button or link.
- Change any aspect of a document's CSS, including color, size, position, visibility, etc.
- Check HTML form elements to see if they meet certain criteria before they are submitted.
- Add or remove HTML elements from a document.
- Change the content of HTML documents.
- Gather remote data and incorporate it into your HTML.
- Determine what browser a user is using, what their screen resolution is, of if they are using a Mac or PC.

More recently, JavaScript has moved beyond the confines of web pages and can be used to create dynamic web sites that interact with data or to automate behaviors in the Adobe Creative Suite, for example.

JavaScript, like all programming languages, uses concepts like variables to stand for values that might change, conditional statements to determine if certain conditions are met and perform particular actions based on those conditions, and functions which are reusable blocks of code that can perform specific actions.

### Creating A JavaScript Program

For our purposes, JavaScript code will be used within HTML documents and interpreted by a web browser. JavaScript can be used in other contexts, but this method makes it easier to implement with a limited set of tools - all you need are a text editor and a web browser.

To start, you must create a blank HTML page. Any file saved with ".html" as the file extension will work, even without any actual HTML code in it (though your browser might generate warnings about missing elements).

JavaScript code can be added directly to the HTML document, inside of a <script> tag:
```
<script>
	/* javascript goes here */
</script>
```

Or you can also reference an external JavaScript file:
```
<script src="javascriptfile.js"></script> 
```

### Your First JavaScript Program
The traditional first program in most languages is to print the phrase "Hello World". To do this with JavaScript, you can use the console.log() function - this is a built-in tool that simply prints a value to the browser's built-in web console, accessible through Chrome or Firefox's developer tools.

```
console.log("Hello World");
```

### Comments
Most programming languages allow you to to insert comments into your code. Comments allow you to leave notes for yourself or others, and to temporarily hide parts of your code so it won't be interpreted (which is very useful if something isn't quite working).

In JavaScript you can use comments in two ways.

For a single line comment, you can use two forward slash characters:
```
this code WILL be run 
// this code will NOT be run
this code will ALSO be run
```
To comment large areas of a program, you can use the slash-star / star-slash format:
```
this code WILL be run

/*
this code, and any thing that happens between the characters above and the ones
below will NOT be run, no matter how long much text there is
*/
```
