### What are variables?
Most programming languages use the idea of a variable to represent different types of data.

Think of a variable as a container - you can put something into it, and then refer to it later by name, like a shorthand. The contents of the container might change, but the variable name remains.

Before you can use a variable, you must declare it, so JavaScript knows that it exists. Trying to reference a variable before it is declared:
```
console.log(variableName);
```

will result in a **ReferenceError: variable is not defined** error.

### Creating Variables
You can declare a variable in three ways - using the JavaScript keywords var, let, or const:
```
var firstname;
let firstname;
const firstname;
```
Each of these results in a variable with the name *firstname*, though each is slightly different in terms of *where* in your program it can be referenced (called the *scope* of a variable) and how it can be reassigned with a new value.

- *var* is valid anywhere in your program after it is declared, and can be reassigned at any point
- *let* is only valid within the current scope, such as inside a loop, if/else statment, or a function
- *const* is valid anywhere, but cannot be reassigned (because it is a constant)

The current trend is to define most variables using the **const** declaration - this is useful for defining configuration attributes of the program that will exist throughout, 
like URLs that are referenced later on. The **let** declaration is used inside of loops where something like a counting integer only needs to exist inside that loop.

You can always use **var** for either of these as long as you are careful about where you make changes to the values, but please note that a lot of example code will use const.

If you declare a variable without giving it a value, it's value will be undefined; const values must be given a value when they are created.

You can define variables right away like this:
```
var firstname = "Zebulon";
let phoneNumber = 7345059234;

```

### Types of Variables
These are two different types of variables - a string and a number. Strings are just lists of characters, and numbers are, well, numbers.

You can perform all sort of operations to combine these in different ways:

```
let addition = 5 +  5		// addition = 10
```
```
let subtraction  = 5 - 1 	// subtraction = 4
```
```
let concatenation =  "String One" +  " " + "String Two"

// concatenation  =  String One String Two
```

JavaScript can switch how it understand these values as needed. For example, trying to divide a word by a number will result in a **NaN** or 'not a number' error:
```

var firstname = "Zebulon";
let phoneNumber = 3000;

console.log(firstname / phoneNumber); // NaN Error

```

But trying to add these two causes JavaScript to treat the number 101 as a string of text, and it will concatenate the values:

```

console.log(firstname + phoneNumber); // prints 'Zebulon3000'


```
