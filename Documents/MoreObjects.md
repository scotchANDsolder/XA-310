# More on Objects

![image](https://user-images.githubusercontent.com/70717743/159571305-c9cd1794-534c-4e39-9aff-bc619a4a3b8c.png)


Objects are elements of abstraction - they can be used to generalize (finding the similarities between items) 
things while allowing for specialization (focusing only on the meaningful differences).

A classic example relates objects to cars - there are many styles of cars, but they all share values like "color", "make", "model", "number of seats", "miles per gallon", and methods like "drive forward", "drive backwards", "steer right", "wash the windshield", and so on.

### Object Constructors
There are several ways to create objects.

One way is to use a template of sorts called a constructor. This is a function that can create (or instantiate) new objects with set properties and methods, and can be used to create a number of similar types of data.

```
function Person(first,last) {
    
  this.firstname = first;
  this.lastname = last;

  this.pet = function(){
    let pets = ["Dog","Cat","Hamster","Fish"];
    return pets[Math.floor(Math.random()*pets.length)];
  }  
}
```

This function is named Person, with an uppercase first letter - this is customary in JavaScript when naming constructor functions.

This particular function accepts two parameters - a first name, and a last name. These are assigned to properties of the new object that is created using the this keyword followed by a dot and the property to assign the value to. What this means is the constructor doesn't need to know or care about the name of the resulting object when it gets created - it creates it, then uses this to mean 'the object currently being created'.

Our function also contains one method, named pet(). This uses an internal array of pet names and returns one at random.

### So How Do You Use This?
To create, or **instantiate**, a new object, you use the new keyword with the name of the object you want to make, followed by any required parameters in parentheses:
```
const personOne = new Person("Barack","Obama");
const personTwo = new Person("Michelle","Obama");
```

This creates two new objects that are floating around in your program's memory. You can access individual parts of these objects once they've been created:

```
console.log(personOne.firstname);
console.log(personOne.lastname);
console.log(personOne.pet());

console.log(personTwo.firstname);
console.log(personTwo.lastname);
console.log(personTwo.pet());

```
