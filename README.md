# Console methods

[TOC]

## console.assert()

Writes an *error* message to the console if the assertion is false. If the assertion is true, nothing happens.

```javascript
console.assert(false, 'this failed');
// This will print the following:
// Assertion failed: this failed

console.assert(true, 'this failed');
// This will not print anything because
// the first parameter did not fail
```

[^assertion]: a declaration that something is the case

## console.warn()

Outputs a warning message to the *Web Console*.

```javascript
console.warn('this is a warning message');
```

------



# Prototyping

[TOC]

## Constructor

The ``constructor`` method is a special method for creating and initializing an object created within a `class`.

## Super

A constructor can use the `super` keyword to call the constructor of a parent class.

The **super** keyword is used to access and call functions on an object's parent.

When used in a constructor, the `super` keyword appears alone and must be used before the `this` keyword is used. The `super` keyword can also be used to call functions on a parent object.

*Syntax*:

```javascript
super([arguments]); // calls the parent constructor.
super.functionOnParent([arguments]);
```

------



# JavaScript Fundamentals

[TOC]

## Functions

Generally speaking, a function is a "subprogram" that can be *called* by code external (or internal in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the *function body*. Values can be *passed* to a function, and the function will *return* a value.

In JavaScript, functions are first-class objects, because they can have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called. In brief, they are `Function` objects.

## Call stack

A data structure that tracks the active executing functions of a program.

## Async Functions

### Function.prototype.call()

*Immediate invoke*

The `call()` method calls a function with a given `this` value and arguments provided individually.

```javascript
function.call(thisArg, arg1, arg2, ...)
```



### Function.prototype.apply()

*Immediate invoke*

The `apply()` method calls a function with a given `this` value, and `arguments` provided as an array (or an array-like object).

```javascript
function.apply(thisArg, [argsArray])
```



### Function.prototype.bind()

*Delayed invoke*

The `bind()` method creates a new function that, when called, has its `this` keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

```javascript
function.bind(thisArg)
```

## Lambda

The use of function as first-class object

[TOC]

## Performance

### performance.now()

Able to find the difference in time from when the program start and end

```javascript
var t0 = performance.now();
doSomething();
var t1 = performance.now();
console.log(`Time Elasped: ${(t1 - t0) / 1000} seconds`);
```



## Basic data types

- Six data types that are primitive
  - Boolean
  - Null
  - Undefined
  - Number
  - String
  - Symbol (new in ES6)
- and Object

## Character

### charCodeAt()

The `charCodeAt()` method returns an integer between 0 and 65535 representing the UTF-16 code unit at the given index.

```js
str.charCodeAt(index)
```

**Example**

```javascript
var str = "h";
str.charCodeAt(0);
// returns 104
```



## NaN

Not a Number

- *NaN* is a special number representing: Not a Number
- Result of undefined or erroneous operations
- Toxic: any arithmetic operation with *NaN* as an input will have *NaN* as a result
- *NaN* is not equal to anything, including *NaN*

## While & Do While loops

### While loop

```javascript
var n = 0;

while (n < 5) {
    n++;
    console.log(`n = ${n}`);
}
// It will check for condition first before executing
```



### Do While loop

```javascript
var i = 0;

do {
    i++;
    console.log(`i = ${i}`);
} while (i < 5);
// it will execute the code first before checking 
// condition
// so even if i === 100, it will run the code at least 
// once
```

#### continue

```javascript
var n = 0;

while (n < 5) {
    n++;
    if (n === 3) continue; // this will skip anything below this line and move out of the loop to run the next iteration
    console.log(`n = ${n}`);
}
// returns n = 1
// n = 2
// n = 4
// n = 5
```

#### break

```javascript
var n = 0;

while (n < 5) {
    n++;
    if (n === 3) break; // this will break out of the loop and stop running all together
    console.log(`n = ${n}`);
}
// returns n = 1
// n = 2
```



# Common methods

[TOC]



## Number Function

```javascript
Number(value)
```

- Converts the value into a number
- It produces *NaN* if it has a problem
- Similar to + prefix operator

## parseInt function

```javascript
parseInt(value, 10)
```

- Converts the value into a number
- It stops at the first non-digit character
- The radix (10) should be required, it will convert in base 10

```javascript
parseInt("08") === 0  //Javascript reads the first 0 and think the number is in octal(base 8) and will conver the whole string into octal

parseInt("08", 10) === 8 // For base 10
```

## Math

- Math object is modeled after Java's Math class
- It contains
  - **Math.abs(x)**  --- absolute value
  - **Math.floor(x)** --- get the integer
  - **Math.log(x)** --- natural logarithm (base `e`) of the given number. If the number is negative, `NaN` is returned
  - **Math.max(a, b, c, ...)** --- return the largest of the given numbers. If at least one of the arguments cannot be converted to a number, `NaN` is returned
  - **Math.pow(base, exponent)** --- return a number representing the given base taken to the power of the given exponent
  - **Math.random()** --- return a floating-point, pseudo-random number between `0` (inclusive/including) and `1` (exclusive/excluding)
  - **Math.round(x)** --- return the value of the given number rounded to the nearest integer (negative *-5.6* would round to *-6*)
  - **Math.sin(x)** --- return the sine of the given number
  - **Math.sqrt(x)** --- return the square root of the given number. If the number is negative, `NaN` is returned

## Strings

- String is a global object in JavaScript
- Sequence of 0 or more 16-bit characters
  - UCS-2, not quite UTF-16
  - No awareness of surrogate pairs
- No separate character type
  - Characters are represented as strings with a length of 1 instead of having the type `char` like other languages
- Strings are immutable
- Similar strings are equal (==)
- String literals can use single or double quotes
- **String.length:** the *length* property determines the number of 16-bit characters in a string (not necessary the same has number of Unicode characters)
- **String(value)** --- converts value to a string

### String Methods

- charAt()
- https://www.youtube.com/watch?v=v2ifWcnQs6M   19:12

------





# Classes

A blueprint for creating objects with pre-defined properties and methods

```javascript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

## Constructor

The `constructor` method is a special method for creating and initializing an object created with a `class`. There can only be one special method with the name "constructor" in a class. A `SyntaxError` will be thrown if the class contains more than one occurrence of a `constructor` method.

A constructor can use the `super` keyword to call the constructor of the super class.

## Static

The `static` keyword defines a static method for a class. Static methods aren't called on instances of the class. Instead, they're called on the class itself. These are often utility functions, such as functions to create or clone objects.



# Object methods

## Delete

The JavaScript `delete` **operator** removes a property from an object; if no more references to the same property are held, it is eventually released automatically.

```javascript
delete object.key
delete object['key']
```



## Object.keys()

The `Object.keys()` method returns an array of a given object's own property `names` , in the same order as we get with a normal loop

**Big O:** *O(n)*

```javascript
Object.keys(obj)
```

**Examples**

```javascript
// simple array
var arr = ['a', 'b', 'c'];
console.log(Object.keys(arr)); // log: ['0', '1', '2']

// objects
var obj = {a: '0', b: '2', c: '3'};
console.log(Object.keys(obj)); // log: ["a", "b", "c"]
```

## Object.values()

The `Object.values()` method returns an array of a given object's enumerable property values, in the same order as that provided by a `for...in` loop (the difference being that a for-in loop enumerates properties in the prototype chain as well)

**Big O:** *O(n)*

**Examples**

```javascript
var obj = { foo: 'bar', baz: 42 };
console.log(Object.values(obj)); // ['bar', 42]

// array like object
var obj = { 0: 'a', 1: 'b', 2: 'c' };
console.log(Object.values(obj)); // ['a', 'b', 'c']

// array like object with random key ordering
// when we use numeric keys, the value returned in a numerical order according to the keys
var an_obj = { 100: 'a', 2: 'b', 7: 'c' };
console.log(Object.values(an_obj)); // ['b', 'c', 'a']

// getFoo is property which isn't enumerable
var my_obj = Object.create({}, { getFoo: { value: function() { return this.foo; } } });
my_obj.foo = 'bar';
console.log(Object.values(my_obj)); // ['bar']

// non-object argument will be coerced to an object
console.log(Object.values('foo')); // ['f', 'o', 'o']
```

## Object.entries()

The `Object.entries()` method returns an array of a given object's own enumerable property `[key, value]` pairs, in the same order as that provided by a `for...in` loop

**Big O:** *O(n)*

**Examples**

```javascript
const object1 = { foo: 'bar', baz: 42 };
console.log(Object.entries(object1)[1]);
// expected output: Array ["baz", 42]

const object2 = { 0: 'a', 1: 'b', 2: 'c' };
console.log(Object.entries(object2)[2]);
// expected output: Array ["2", "c"]

const result = Object.entries(object2).sort((a, b) => a - b);
console.log(Object.entries(result)[1]);
// expected output: Array ["1", Array ["1", "b"]]
```

## .hasOwnProperty()

The `hasOwnProperty()` method returns a Boolean indicating whether the object has the specified property as its own property (as opposed to inheriting it)

**Big O:** *O(1)*

```javascript
const object1 = new Object();
object1.property1 = 42;

console.log(object1.hasOwnProperty('property1'));
// expected output: true

console.log(object1.hasOwnProperty('toString'));
// expected output: false

console.log(object1.hasOwnProperty('hasOwnProperty'));
// expected output: false
```

## Set

The `Set` object lets you  store unique values of any type, whether primitive values or object references.

| Set Methods | Syntax                                                       |
| ----------- | ------------------------------------------------------------ |
| .add()      | animals.add('🐷');                                            |
| .has()      | animals.has('🐷'); // true                                    |
| .size       | animals.size // size of the set                              |
| .forEach()  | animals.forEach(animal => {<br/>console.log(`Hey ${animal}!`);
}); |
| .delete()   | animals.delete('🐷');                                         |
| .clear()    | animals.clear();                                             |

**Examples**

1.

```javascript
let animals = new Set();

animals.add('🐷');
animals.add('🐼');
animals.add('🐢');
animals.add('🐿');
console.log(animals.size); // 4
animals.add('🐼');
console.log(animals.size); // 4

console.log(animals.has('🐷')); // true
animals.delete('🐷');
console.log(animals.has('🐷')); // false

animals.forEach(animal => {
  console.log(`Hey ${animal}!`);
});

// Hey 🐼!
// Hey 🐢!
// Hey 🐿!

animals.clear();
console.log(animals.size); // 0
```

2.

```javascript
let myAnimals = new Set(['🐷', '🐢', '🐷', '🐷']);

myAnimals.add(['🐨', '🐑']);
myAnimals.add({ name: 'Rud', type: '🐢' });
console.log(myAnimals.size); // 4

myAnimals.forEach(animal => {
  console.log(animal);
});


// 🐷
// 🐢
// ["🐨", "🐑"]
// Object { name: "Rud", type: "🐢" }
```



------

[TOC]

# Array Methods

## Sort

`array.sort(compareFunction)`

**Big O**: *O(n log n)*

| Parameter         | Description                                                  |
| ----------------- | ------------------------------------------------------------ |
| *compareFunction* | Optional. A function that defines an alternative sort order. The Function should return a negative, zero, or positive value, depending on the arguments, like:<br /> - function(a,b){return a-b}<br />When the sort() method compares two values, it sends the values to the compare function, and sorts the values according to the returned (negative, zero, positive) value.<br />**Example**:<br />When comparing 40 and 100, the sort() method calls the compare function(40,100).<br />The function calculates 40-100, and returns -60 (a negative value).<br />The sort function will sort 40 as a value lower than 100. |



```javascript
array.sort(function(a, b){return a-b}); //Ascending number

array.sort(function(a, b){return b-a}); //Descending number

array.sort(function(a, b){return a<b}); //Ascending alphabet

array.sort(function(a, b){return a>b}); //Descending alphabet
```



## Search

### .indexOf()

The `indexOf()` method returns the first index at which a given element can be found in the array or returns `-1` if it is not present

**Big O**: *O(n)* - Linear Search

**Examples**

```javascript
var beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// expected output: 1

// start from index 2
console.log(beasts.indexOf('bison', 2));
// expected output: 4

console.log(beasts.indexOf('giraffe'));
// expected output: -1
```



### .includes()

The `includes()` method determines whether an array includes a certain value among its entries, returning `true` or `false` as appropriate

**Big O**: *O(n)* - Linear Search

**Examples**

```javascript
var array1 = [1, 2, 3];

console.log(array1.includes(2));
// expected output: true

var pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false

```



### .find()

The `find()` method returns the **value** of the **first element** in the array that satisfies the provided testing function. Otherwise `undefined` is returned

**Big O**: *O(n)* - Linear Search

**Examples**

```javascript
var array1 = [5, 12, 8, 130, 44];

var found = array1.find(function(element) {
  return element > 10;
});

console.log(found);
// expected output: 12

```



### .findIndex()

The `findIndex()` method returns the **index** of the **first element* in the array that satisfies the provided testing function. Otherwise, it returns `-1`, indicating no element passed the test



**Examples**

```javascript
var array1 = [5, 12, 8, 130, 44];

function findFirstLargeNumber(element) {
  return element > 13;
}

console.log(array1.findIndex(findFirstLargeNumber));
// expected output: 3

```

## Array.from()

Can be use to create a new set of tuples

```javascript
let container = Array.from({length: 10}, () => []);
console.log(container);
/* 
(10) [Array(0), Array(0), Array(0), Array(0), Array(0), Array(0), Array(0), Array(0), Array(0), Array(0)]
0: []
1: []
2: []
3: []
4: []
5: []
6: []
7: []
8: []
9: []
*/
```

## .concat()

The `concat()` method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array

**Concat tuples:**

```javascript
// How to concat a tuple
let tuple = [[1,2], [3, [4,5]]];
tuple = [].concat(...tuple);
// It'll need to be run again because of the nested tuple at [4,5]
tuple = [].concat(...tuple);
```

## .flat()

The `flat()` method creates a new array with all sub-array elements concatenated into it recursively up the specified depth

```javascript
var newArray = arr.flat([depth]); 
// defaults to depth of 1
```



------



[TOC]



# Instagram Scaling Backend

Source: https://youtu.be/hnpzNAPiC0E

## Canary

*Also known as: canary test, canary deployment*

In canary testing, a small subset of end users servers as a test group for updates. If anything in the updates causes problems, it alerts the IT team before a large group of users feel the effects. (e.g. 95% of the users retain old versions of the product while 5% of the users are using the new versions of the product).

![canary_testing](https://cdn.ttgtmedia.com/rms/onlineImages/canary_testing.jpg)

# Comparison Sorting Algorithms

A **comparison sort** is a type of [sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm) that only reads the list elements through a single abstract comparison operation (often a "less than or equal to" operator or a [three-way comparison](https://en.wikipedia.org/wiki/Three-way_comparison)) that determines which of two elements should occur first in the final sorted list. 

------

Sorting is the process of rearranging the items in a collection (e.g. an array) so that the items are in some kind of order

**Examples**

- Sorting numbers from smallest to largest
- Sorting names alphabetically
- Sorting movies based on release year
- Sorting movies based on revenue

## Bubble Sort

Bubble sort is a sorting algorithm where the largest values bubble up to the top until it is sorted

**Big O:** *O(n^2)*  
*Note: if you know the list is nearly sorted it'll be O(n)*

![Bubble Sort GIF](https://upload.wikimedia.org/wikipedia/commons/c/c8/Bubble-sort-example-300px.gif)

**Pseudocode:**

```javascript
// 1. Start looping from a variable called 'i' from the end of the array towards the beginnng
// 2. Start an inner loop with a variable called 'j' from the beginning until 'i' - 1
// 3. If arr[j] is greater than arr[j + 1], swap those two values!
// 4. Return the sorted array
```



## Selection Sort

Similar to bubble sort, but instead of first placing large values into sorted position, it places small values into sorted position.

**Big O:** *O(n^2)*

![Selection Sort GIF](https://codingconnect.net/wp-content/uploads/2016/09/Selection-Sort.gif)

**Pseudocode:**

```javascript
// 1. Store the first element as the smallest value you've seen so far
// 2. Compare this item to the next item in the array until you find a smaller number
// 3. If a smaller number is found, designate that smaller number to be the new "minimum" and continue until the end of the array
// 4. If the "minimum" is not the value (index) you initially began with, swap the two values
// 5. Repeat this with the next element until the array is sorted
```



## Insertion Sort

Builds up the sort by gradually creating a larger left half which is always sorted

**Big O:** *O(n^2)*

*Note: Since insertion sort has 1 side already sorted, it can continue to work as new stream of data gets inputted*

![Insertion Sort GIF](https://upload.wikimedia.org/wikipedia/commons/9/9c/Insertion-sort-example.gif)

**Pseudocode:**

```javascript
// 1. Start by picking the second element in the array
// 2. Now compare the second element with the one before it and swap if necessary
// 3. Continue to the next element and if it is in the incorrect order, iterate through the sorted portion(i.e. the left side) to place the element in the correct place
// 4. Repeat until the array is sorted
```



## Merge Sort

Merge sort works by decomposing an array into smaller arrays of 0 or 1 elements, then building up a newly sorted array

**Big O:** *O(n log n) with space complexity of O(n)*

![Merge Sort GIF](https://codepumpkin.com/wp-content/uploads/2017/10/MergeSort_Avg_case.gif)

**Pseudocode:**

Part 1: Merging/Comparing Arrays

```javascript
// 1. Create an empty array, take a look at the smallest values in each input array
// 2. While there are still values we haven't looked at...
//    a. If the value in the first array is *smaller* than the value in the second
//       array, push the value in the first array inbto our results and move on to the 
//       next value in the first array.
//    b. If the value in the first array is *larger* than the value in the second
//       array, push the value in the second array into our results and move on to the
//       next value in the second array.
//    c. Once we exhaust one array, push in all remaining values from the other array.
```

Part 2: Splitting arrays

```javascript
// 1. Break up the array into halves until you have arrays that are empty or have one
//    element
// 2. Once you have smaller sorted arrays, merge those arrays with other sorted arrays
//    until you are back at the full length of the array
// 3. Once the array has been marged back together, return the merged (and sorted!)
//    array
```



## Quick Sort

Quick sort work by selecting one element (called the "pivot") and finding the index where the pivot should end up in the sorted array. Once the pivot is positioned appropriately, quick sort can be applied on either side of the pivot

**Big O:** *O(n log n) with space complexity of O(log n)*

![Quick Sort GIF](https://www.tutorialspoint.com/data_structures_algorithms/images/quick_sort_partition_animation.gif)

------

[TOC]

# Integer Sort

**Integer sorting** is the algorithmic problem of [sorting](https://en.wikipedia.org/wiki/Sorting_algorithm) a collection of data values by numeric keys, each of which is an [integer](https://en.wikipedia.org/wiki/Integer). 

## Radix Sort

Radix sort is a special sorting algorithm that works on lists of numbers. It never makes comparisons between elements! It exploits the fact that information about the size of a number is encoded in the number of digits. More digits means a bigger number!

**Big O:** *O(nk) Note: because of how computers store numbers in memory, radix sort is theoretically O(n log n)*

*Source: [Efficiency](https://en.wikipedia.org/wiki/Radix_sort#Efficiency)*

