# Sorting & Searching Algorithms

A common method for understanding differences between algorithms is to examine sorting and searching methods. 
There are a surprising number of ways to sort and search for a given set of items into a certain order, usually numerically or alphabetically.

[These sorting algorithms](https://en.wikipedia.org/wiki/Sorting_algorithm) - with names such as selection, insertion, bubble, heap, merge, quick, bucket - are all 
used for different reasons based on their complexity and efficiency and the type and amount of data being sorted.

Similarly, there are numerous [search algorithms](https://en.wikipedia.org/wiki/Search_algorithm) can be used for everything from retrieving a record from a database, finding the 
maximum or minimum value in a list or array or finding the [shortest path for navigation](https://en.wikipedia.org/wiki/Travelling_salesman_problem). 

Internally, JavaScript's [.sort()](https://tc39.es/ecma262/#sec-array.prototype.sort) method does not actually specify a particular algorithm, and apparently uses different algorithms for based on the operating system or browser, the size of the array, the type of data, and so on.

### Computational Complexity 

The efficiency of any algorithm can be analyzed to determine its computational complexity, which is a measure of how much time and memory storage it takes to complete a task given a certain number of items. Programmers will often want to know the best, worst, or average case scenarios for how an algorithm performs so these resources can be allocated appropriately.

For example, algorithm one might perform slightly worse in terms of time and resource use when compared to algorithm two if the data set contains than 100 items. Since it's much easier to implement algorithm one, the performance cost is negligible.

However, with a very large set of data the differences might be much more dramatic as the resource usage for algorithm one grows exponentially while the algorithm two grows in a linear manner. In this scenario it is worth the initial effort to implement the more complex algorithm.

### Measuring Performance
In computing, the performance of algorithms can be described using a mathematical notation called [Big O notation](https://en.wikipedia.org/wiki/Big_O_notation). The "o" refers to the order of magnitude of a function, indicating a worst-case scenario of an algorithm's performance based on the number (n) of inputs.

For example, the notation O(1) describes a algorithm that will always execute in the same amount of time, regardless of the size of the input. This would be something like accessing a single element of an array by index in JavaScript, which by definition only works on one thing.

An O(n) algorithm is said to be linear, meaning that it would take you, at most, 10 iterations to find a page in a 10 page book and 1000 iterations to find one in a 1000 page book.

For operations where you might have to loop through nested sets of data, you might end up with a O(n2), where the execution time is determined by the square of the number of items. Something like a bubble sort is this type of algorithm.

There are other types of performance types - cubic, logarithmic, exponential - all of which might have benefits and drawbacks in particularly applications.

## Some examples of sorting algorithms

#### Bubble Sort

Bubble sort is considered the simplest sorting algorithm. It goes through an entire array and compares each neighboring number. It then swaps the numbers and keeps doing this until the list is in ascending order.

![image](https://miro.medium.com/max/600/1*1MiLjMYgr2r2fDORCJn89w.gif)

JavaScript implementation:

```
function bubbleSort(inputArray) {
		let length = inputArray.length;
		for (let i = 0; i < length; i++) {
			for (let j = 0; j < length; j++) {
				if (inputArray[j] > inputArray[j + 1]) {
					let tmp = inputArray[j];
					inputArray[j] = inputArray[j + 1];
					inputArray[j + 1] = tmp;
				}
			}
		}
		return inputArray;
	};
  
  
// This is our unsorted array
var arr = [234, 43, 55, 63,  5, 6, 235, 547];
//Prints out sorted array
console.log(bubleSort(arr));
```



#### Insertion Sort

Insertion sort involves going through a pile, taking one item, comparing it to the first, swapping places if one item is larger than another and continuing this process until the minimum item is in the correct location.

![image](https://miro.medium.com/max/1102/1*krA0OFxEDgi8hVHJffCi4w.gif)


#### Merge Sort

Imagine having to take a deck of cards, split it in two halves and continue splitting those piles in halves, and halves again until all you have is 52 piles of 1 card. Then, you regroup the piles in pairs again but this time, sort them in ascending order. This is essentially how Merge Sort works.

![image](https://miro.medium.com/max/600/1*bmfRxyIQZEK0Iu5T6YV1sw.gif)




