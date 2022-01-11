### Conditionals

A very common thing to do in programming languages is to make decisions about what to do based on the current conditions.

The simplest test is the "if" statement:
```
if (true) {
	console.log("This Is True");
}
```

In this example, I only log something to the console if the statment is **true**; in this case it is always *true*;

&nbsp;
&nbsp;

A more complex example is to compare the value of something, using the == comparison operator; in Javascript, the = sign is used to assign value to something, and the == sign to test or compare a condition.
```
let blah = 1;

if (blah == 1) {
	console.log("blah is equal to 1");
}
```

&nbsp;

More complex is the if/else statement:

```
let test = "Zulu";

if (test == "Tango")  {
	console.log("Zulu IS equal to Tango");
}
else {
	console.log("Zulu is NOT equal to Tango");
}

```

&nbsp;

Even more complicated is the if/elseif/else:

```
let number = 20;

if (number < 1) {
	// do this if 20 is less than 1
}
else if (number < 10) {
	// do this if 20 is less than 10
}
else {
	// do this in all other cases
}

```
