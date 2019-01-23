- [Console methods](#console-methods)
  - [console.assert()](#consoleassert)
  - [console.warn()](#consolewarn)
- [Prototyping](#prototyping)
  - [Constructor](#constructor-NaN)
  - [Super](#super)
- [JavaScript Fundamentals](#javascript-fundamentals)
  - [Functions](#functions)
  - [Call stack](#call-stack)
  - [Async Functions](#async-functions)
    - [Function.prototype.call()](#functionprototypecall)
    - [Function.prototype.apply()](#functionprototypeapply)
    - [Function.prototype.bind()](#functionprototypebind)
  - [Lambda](#lambda)
  - [Performance](#performance)
    - [performance.now()](#performancenow)
  - [Basic data types](#basic-data-types)
  - [Character](#character)
    - [charCodeAt()](#charcodeat)
  - [NaN](#nan)
  - [While & Do While loops](#while--do-while-loops)
    - [While loop](#while-loop)
    - [Do While loop](#do-while-loop)
      - [continue](#continue)
      - [break](#break)
- [Common methods](#common-methods)
  - [Number Function](#number-function)
  - [parseInt function](#parseint-function)
  - [Math](#math)
  - [Strings](#strings)
    - [String Methods](#string-methods)
- [Classes](#classes)
  - [Constructor](#constructor-NaN)
  - [Static](#static)
- [Object methods](#object-methods)
  - [Delete](#delete)
  - [Object.keys()](#objectkeys)
  - [Object.values()](#objectvalues)
  - [Object.entries()](#objectentries)
  - [.hasOwnProperty()](#hasownproperty)
  - [Set](#set)
- [Array Methods](#array-methods)
  - [Sort](#sort)
  - [Search](#search)
    - [.indexOf()](#indexof)
    - [.includes()](#includes)
    - [.find()](#find)
    - [.findIndex()](#findindex)
  - [Array.from()](#arrayfrom)
  - [.concat()](#concat)
  - [.flat()](#flat)
- [Instagram Scaling Backend](#instagram-scaling-backend)
  - [Canary](#canary)
- [Comparison Sorting Algorithms](#comparison-sorting-algorithms)
  - [Bubble Sort](#bubble-sort)
  - [Selection Sort](#selection-sort)
  - [Insertion Sort](#insertion-sort)
  - [Merge Sort](#merge-sort)
  - [Quick Sort](#quick-sort)
- [Integer Sort](#integer-sort)
  - [Radix Sort](#radix-sort)
- [Data Structures](#data-structures)
  - [Linked Lists](#linked-lists)
    - [Singly Linked Lists](#singly-linked-lists)
      - [Push](#push)
      - [Pop](#pop)
      - [Shift](#shift)
      - [Unshift](#unshift)
      - [Get](#get)
      - [Set](#set-1)
      - [Insert](#insert)
      - [Remove](#remove)
      - [Reverse](#reverse)
    - [Doubly Linked List](#doubly-linked-list)
      - [Push](#push-1)
      - [Pop](#pop-1)
      - [Shift](#shift-1)
      - [Unshift](#unshift-1)
      - [Get](#get-1)
      - [Set](#set-2)
      - [Insert](#insert-1)
      - [Remove](#remove-1)
  - [Stacks](#stacks)
  - [Queue](#queue)
  - [Trees](#trees)
    - [Binary Search Tree](#binary-search-tree)
      - [Insert](#insert-2)
      - [Find](#find-1)
    - [Tree Traversal](#tree-traversal)
      - [Breadth First Search →](#breadth-first-search-)
      - [Depth First Search ↓](#depth-first-search-)
        - [DFS - PreOrder](#dfs---preorder)
        - [DFS - PostOrder](#dfs---postorder)
        - [DFS - InOrder](#dfs---inorder)
  - [Binary Heap](#binary-heap)
    - [Storing Heaps in Array](#storing-heaps-in-array)
    - [Max Binary Heap](#max-binary-heap)
      - [Insert](#insert-3)
      - [Remove](#remove-2)
- [Priority Queue](#priority-queue)
- [Hash Tables](#hash-tables)
  - [Hashing function](#hashing-function)
  - [Collisions Handling](#collisions-handling)
    - [Separate Chaining](#separate-chaining)
    - [Linear Probing](#linear-probing)
- [Graph](#graph)
  - [Undirected Graph](#undirected-graph)
  - [Directed Graph](#directed-graph)
  - [Weighted Graph](#weighted-graph)
  - [Unweighted Graph](#unweighted-graph)

# Console methods

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

[TOC]



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

```javascript
class Cow {
    constructor(color){
        this.color = color;
    }
    static moo() { 
        return 'meow!!';
        // this method stays with the class 
        // and won't be passed on to the new instances created 
        // (won't be passed on to the children)
    }
}

var brownCow = new Cow('yellow');

Cow.moo();
// returns 'meow!!'

brownCow.color;
// returns 'yellow'

brownCow.moo();
// brown.moo is not a function
```



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

**Big O:** *O(n \* k) Note: because of how computers store numbers in memory, radix sort is theoretically O(n log n)*

*Source: [Efficiency](https://en.wikipedia.org/wiki/Radix_sort#Efficiency)*

[TOC]

# Data Structures

**Data structure** is a particular way of organizing *data* so that it can be used efficiently

## Linked Lists

A data structure that contains a **head**, **tail** and **length** property.

Linked Lists consist of nodes, and each **node** has a **value** and a **pointer** to another node or null

<Lists are a linear>

[Useful Slides](https://cs.slides.com/colt_steele/singly-linked-lists#/)

### Singly Linked Lists

- Singly Linked Lists are an excellent alternative to arrays when **insertion** and **deletion** at the beginning are frequently required
- Arrays contain a built in index whereas Linked Lists do not
- The idea of a list data structure that consists of nodes is the foundation for other data structure like **Stacks** and **Queues**

------

#### Push

Adding a new **node** to the end of the Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. This function should accept a value
2. Create a new node using the value passed to the function
3. If there is no head property on the list, set the head and tail to be the newly created node
4. Otherwise set the next property on the tail to be the new node and set the tail property on the list to be the newly created node
5. Increment the length by one
6. Return the linked list
```

------

#### Pop

Removing a **node** from the end of the Linked List

**Big O: ** *O(n)*

**Pseudocode**

```
1. If there are no nodes in the list, return undefined
2. Loop through the list until you reach the tail
3. Set the next property of the 2nd to last node to be null
4. Set the tail to be the 2nd to last node
5. Decrement the length of the list by 1
6. Return the value of the node removed
```

------

#### Shift

Removing a **node** from the beginning of the Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. If there are no nodes, return undefined
2. Store the current head property in a variable
3. Set the head property to be the current head's next property
4. Decrement the length by 1
5. Return the value of the node removed
```

------

#### Unshift

Adding a new **node** to the beginning of the Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. This function should accept a value
2. Create a new node using the value passed to the function
3. If there is no head property on the list, set the head and tail to be the newly created node
4. Otherwise set the newly created node's next property to be the current head property on the list
5. Set the head property on the list to be that newly created node
6. Increment the length of the list by 1
7. Return the linked list
```

------

#### Get

Retrieving a **node** by it's position in the Linked List

**Big O: ** *O(n)*

**Pseudocode**

```
1. This function should accept an index
2. If the index is less than zero or greater than or equal to the length of the list, return null
3. Loop through the list until you reach the index and return the node at that specific index
```

------

#### Set

Changing the **value** of a node based on it's position in the Linked List

**Big O: ** *O(n)*

**Pseudocode**

```
1. This function should accept a value and an index
2. Use your .get() function to find the specific node
3. If the node is not found, return false
4. If the node is found, set the value of that node to be the value passed to the function and return true
```

------

#### Insert

Adding a node to the Linked List at a **specific** position

**Big O: ** *O(n)*

**Pseudocode**

```
1. Define a function that accept an index and value
2. If the index is less than zero or greater than the length, return false
3. If the index is the same as the length, push a new node to the end of the list
4. If the index is 0, unshift a new node to the start of the list
5. Otherwise, using the .get() method, access the node at the index - 1
6. Set the next property on that node to be the new node
7. Set the next property on the new node to be the previous next
8. Increment the length
9. Return true
```

------

#### Remove

Removing a node from the Linked List at a **specific** position

**Big O: ** *O(n)*

**Pseudocode**

```
1. Define a function that accepts an index
2. If the index is less than zero or greater than or equal to the length, return undefined
3. If the index is the same as the length - 1, use .pop()
4. If the index is 0, use .shift()
5. Otherwise, using the .get() method, access the node at the index - 1
6. Set the next property on that node to be the next of the next node
7. Decrement the length
8. Return the value of the node removed
```

------

#### Reverse

Reversing the Linked List **in place**

[Useful Slides](https://cs.slides.com/colt_steele/singly-linked-lists#/29)

**Big O: ** *O(n)*

**Pseudocode**

```
1. Swap the head and tail
2. Create a variable called next
3. Create a variable called prev
4. Create a variable called node and initalize it to the head property
5. Loop through the list
6. Set next to be the next property on whatever node is

```

------

### Doubly Linked List

**Almost** identical to Singly Linked Lists, except every node has another pointer, to the previous node!

Doubly Linked List will be *more flexible* compare to Singly Linked List at the cost of using *more memory*

------

#### Push

Adding a node to the **end** of the Doubly Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. Create a new node with the value passed to the function
2. If the head is property is null set the head and tail to be the newly created node
3. If not, set the next property on the tail to be that node
4. Set the previous property on the newly created node to be the tail
5. Set the tail to be the newly created node
6. Increment the length
7. Return the Doubly Linked List
```

------

#### Pop

Removing a node from the **end** of the Doubly Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. If there is no head, return undefined
2. Store the current tail in a variable to return later
3. If the length is 1, set the head and tail to be null
4. Update the tail to be the previous Node
5. Set the newTail's next to null
6. Set oldTail's prev to null
7. Decrement the length
8. Return the value removed
```

------

#### Shift

Removing a node from the **beginning** of the Doubly Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. If length is 0, return undefined
2. Store the current head property in a variable (old head)
3. If the length is 1, set the head and tail to be null
4. Update the head to be the next of the old head
5. Set the head's prev property to null
6. Set the old head's next to null
7. Decrement the length
8. Return old head
```

------

#### Unshift

Adding a node to the **beginning** of the Doubly Linked List

**Big O: ** *O(1)*

**Pseudocode**

```
1. Create a new node with the value passed to the function
2. If the length is 0, set the head and tail to be new node
3. Otherwise
	- Set the prev property on the head of the list to
	be the new node
	- Set the next property on the new node to be the
	head property
	- Update the head to be the new node
4. Increment the length
5. Return the list
```

------

#### Get

Accessing a node in a Doubly Linked List by it's position

**Big O: ** *O(n/2)*

**Pseudocode**

```
1. If the index is less than 0 or greater or equal to the length, return null
2. If the index is less than or equal to half the length of the list
	- Loop through the list starting from the head and
	loop towards the middle
	- Return the node once it is found
3. If the index is greater than half the length of the list
	- Loop through the list starting from the tail and
	loop towards the middle
	- Return the node once it is found
```

------

#### Set

Replacing the value of a specified node in a Doubly Linked List

**Big O: ** *O(n/2)*

**Pseudocode**

```
1. Create a variable which is the result of the .get() method at the index passed to the function
	- If the .get() method returns a valid node, set
	the value of that node to be the value passed to the 
	function
	- Return true
2. Otherwise, return false
```

------

#### Insert

Adding a node in a Doubly Linked List by a certain position

**Big O: ** *O(1)*

**Pseudocode**

```
1. If the index is less than zero or greater than or equal to the length, return false
2. If the index is 0, unshift
3. If the index is the same as the length, push
4. Use the .get() method to access the index - 1
5. Set the next and prev properties on the correct nodes to link everything together
6. Increment the length
7. Return true
```

------

#### Remove

Removing a node in a Doubly Linked List by a certain position

**Big O: ** *O(1)*

**Pseudocode**

```
1. If the index is less than zero or greater than or equal to the length, return undefined
2. If the index is 0, shift
3. If the index is equal to length - 1, pop
4. Use .get() to retrieve the node to be removed
5. Update the next and prev properties to remove the to be removed node from the list
6. Set the next and prev to null on the removed node
7. Decrement the length
8. Return the removed node
```

------

## Stacks

A **LIFO** data structure
The last element added to the stack will be the first one to be removed

*Example usages:*

- Managing function invocations (e.g. call stacks)
- Undo / Redo
- Routing (the history object, e.g. browser history)

**Big O:** 

```
Insertion - O(1)
Removal - O(1)
Searching - O(n)
Access - O(n)
```

## Queue

A **FIFO** data structure
The first element added to the queue will be the first one to be removed

*Example usages:*

- Background tasks
- Uploading resources
- Printing / Task processing

**Big O:** 

```
Insertion - O(1)
Removal - O(1)
Searching - O(n)
Access - O(n)
```

------

## Trees

A data structure that consists of nodes in a **parent / child** relationship

<Trees are nonlinear>

*Examples*

- *HTML DOM*
- *Network Routing*
- *Abstract syntax tree*
- *Artificial Intelligence - Decision Tree*
- *Folders in Operating system - File system*

[Useful Slides](https://cs.slides.com/colt_steele/trees#/)

- **Root** - The top node in a tree
- **Child** - A node directly connected to another node when moving away from the Root
- **Parent** - The converse notion of a child
- **Siblings** - A group of nodes with the same parents
- **Leaf** - A node with no children
- **Edge** - The connection between one node and another

------

### Binary Search Tree

- Every parent node has at most **two children**
- Every node to the left of a parent node is **always less** than the parent
- Every node to the right of a parent node is **always greater** than the parent

------

#### Insert

**Big O:** *O(log n) - O(n) when tree is one sided like a linked list* 

**Pseudocode**

```
1. Create a new node
2. Starting at the root
	A. Chceck if there is a root, if not - the root now becomes the new node
	B. If there is a root, check if the value of the new node is greater than or less than the value of the root
	C. If it is greater
		- Check to see if there is a node to the right
			- If there is, move to that node and repeat these steps
			- If there is not, add that node as the right property
	D. If it is less
		- Check to see if there is a node to the left
			- If there is, move to that node and repeat these steps
			- If there is not, add that node as the left property
```

------

#### Find

**Big O:** *O(log n) - O(n) when tree is one sided like a linked list* 

**Pseudocode**

```
1. Starting at the root
	A. Check if there is a root, if not return false
	B. If there is a root, check if the value of the new node is the value we're looking for
		- If found, return true
	C. If not, check to see if thte value is greater than or less than the value of the root
	D. If it is greater
		- Check to see if there is a node to the right
			-- If there is, move to that node and repeat these steps
			-- If there is not, return false
	E. If it is less
		- Check to see if there is a node to the left
			-- If there is, move to that node and repeat these steps
			-- If there is not, return false
```

------

### Tree Traversal

Going through each of the nodes in a tree data structure

------

#### Breadth First Search →

Visit all sibling nodes before visiting their children nodes

**Implementation**

```
Iterative solution
1. Create a queue and a variable to store the values of nodes visited
2. Place the root node in the queue
3. Loop as long as there is anything in the queue
	- Dequeue a node from the queue and push the value of the node into the variable that stores the node
	- If there is a left property on the node, dequeued - add it to the queue
	- If there is a right property on the node, dequeue - add it to the queue
4. Return the variable that stores the values
```

------

#### Depth First Search ↓

Traverse vertically down to the end of the tree before visiting next sibling nodes

------

###### DFS - PreOrder

Collect from Top to Bottom

*Advantage: Get a structured copy of the tree, used to export & reconstruct*

**Implementation**

```javascript
// Depth First Search
  preOrder() {
    var visited = [];
    (function traverse(node) {
      visited.push(node.val);
      if (!node.left && !node.right) return;
      if (node.left) {
        traverse(node.left);
      }
      if (node.right) {
        traverse(node.right);
      }
    }(this.root));
    return visited;
  } // End of PreOrder
```

------

######  DFS - PostOrder

Collect from Bottom Left - Bottom Right to Top

**Implementation**

```javascript
postOrder() {
    var visited = [];
    (function traverse(node) {
      if (node.left) traverse(node.left);
      if (node.right) traverse(node.right);
      visited.push(node.val);
    }(this.root));
    return visited;
  }
```

######  DFS - InOrder

Collection from bottom left to bottom right (sorted)

*Advantage: Get a sorted list of the tree*

**Implementation**

```javascript
inOrder() {
      var visited = [];
      (function traverse(node) {
        if (node.left) traverse(node.left);
        visited.push(node.val);
        if (node.right) traverse(node.right);
      }(this.root));
      return visited;
    }
```

### Binary Heap

**Very** similar to a binary search tree, but with some different rules!

In a **MaxBinaryHeap,** parent nodes are always larger than child nodes. In a **MinBinaryHeap,** parent nodes are always smaller than child nodes

Binary Heaps are used to implement Priority Queues, which are **very** commonly used data structures

They are also used quite a bit, with **graph traversal** algorithms

##### Storing Heaps in Array

- For any index of an array `n` ...
- The **left** child is stored at `2n + 1`
- The **right** child is stored at `2n + 2`
- For any index of a child: It's parent is at index `Math.floor((n - 1) / 2)`

**Big O:** 

```
Insertion - O(log n)
Removal - O(log n)
Search - O(n)
```

------

##### Max Binary Heap

- Each parent has at most two child nodes
- The value of each parent node is **always **greater than its child nodes
- In a max Binary Heap, the parent is greater than the children, but there are no guarantees between sibling nodes
- A binary heap is as compact as possible. All the children of each node are as full as they can be and **left children are filled out first**

###### Insert

- Add to the end
- Bubble up

**Pseudocode**

```
1. Push the value into the values property on the heap
2. Bubble the value up to its correct spot by comparing it to it's parent node
```

------

###### Remove

- Remove the root

- Replace with the most recently added

- Adjust (Sink down)

[TOC]

# Priority Queue

A data structure where each element has a priority. Elements with higher priorities are served before elements with lower priorities

![Priority Queue in an ER](https://puu.sh/CxSmV/2885bdc827.png)

**Implementation**

```
1. Write a Min Binary Heap - lower number means higher priority
2. Each Node has a value and a priority number. Use the priority to build the heap
3. Enqueue() method accepts a value and priority, make a new node, and put it in the right spot base off of it's priority
4. Dequeue() method removes root element, returns it, and rearranges heap using priority
```

# Hash Tables

Hash tables are used to store *key-value* pairs.
They are like arrays, but keys are not ordered.

Unlike arrays, has tables are fast for all of the following operations:

- finding values
- adding new values
- removing values

**Big O**

```
Insertion - O(1)
Deletion - O(1)
Access - O(1)
```



## Hashing function

Adding in a prime number is usually good in making the hash function output more distributed results

A good hash should be fast, distribute keys uniformly, and be deterministic (same input should yield the same output every time)

## Collisions Handling

------

#### Separate Chaining

With separate chaining, at each index in our array we store values using a more sophisticated data structure (e.g. an array or a linked list)

This allows us to store multiple key-value pairs at the same index
![Hash Table - Separate Chaining](https://puu.sh/CxMPL/fd7ecd51c0.png)

Simply loop through the nested array to find 'Salmon'

------

#### Linear Probing

With linear probing, when we find a collision, we search through the array to find the next empty slot

Unlike with separate chaining, this allow us to store a single key-value at each index

![Hash Table - Linear Probing](https://puu.sh/CxMSF/06ae28cb9e.png)

# Graph

[Useful Slides](https://cs.slides.com/colt_steele/graphs#/)

![Graph](https://puu.sh/CxOff/df1988f0b0.png)

Graphs can be use for:

- Social Networks
- Location / Mapping
- Routing Algorithms
- Visual Hierarchy
- File System Optimizations
- Recommendations engine (People also watched, also bought, etc)
- **EVERYWHERE!**

**Understanding Graphs**

- **Vertex** - a node
- **Edge** - connection between nodes
- **Weighted/Unweighted** - values assigned to distances between vertices
- **Directed/Undirected** - directions assigned to distanced between vertices

## Undirected Graph

Two way connection, like Facebook friends (e.g. user A can see user B's page and user B can see user A's page)

![Undirected Graph](https://puu.sh/CxSiG/c1e266761b.png)

A good example better shown below

![Facebook Friends Graph](https://puu.sh/CxSp0/f8a2476c7d.png)

## Directed Graph

Contains a direction, like a one-way street as oppose to undirected graph that acts as a two way street

![Directed Graph](https://puu.sh/CxSks/02c70dae3e.png)

An example would be like how Instagram following works

![Instagram Followers Graph](https://puu.sh/CxSqD/00a5c85c49.png)

## Weighted Graph

When values are assigned to the edges(connections), it becomes a weighted graph

![Weighted Graph](https://puu.sh/CxSuI/4187490599.png)

A good example would be locations from point Town A to Town B requires 8km of distance

## Unweighted Graph

An unweighted graph is just a graph without any value attached to the edges(connections)	

![Unweighted Graph](https://puu.sh/CxSyS/fff4c1aa57.png)

## Adjacency Matrix

Using a matrix to store the connection between vertices

![Adjacency Matrix](https://puu.sh/CxUE4/ed01615020.png)

## Adjacency List

Could be stored on a hash table with the value being an array of all the connected vertices

![Adjacency List](https://puu.sh/CxUK4/9f3acc32ba.png)

## Adjacency List vs Adjacency Matrix

![AList vs AMatrix](https://puu.sh/CxUQN/ce5ce28ede.png)

![vs](https://puu.sh/CxUV5/c571d89dcf.png)

### Adding A Vertex

**Implementation**

```
1. Write a method called addVertex, which accepts a name of a vertex
2. It should add a key to the adjacency list with the name of the vertex and set its value to be an empty array
```

### Adding An Edge

**Implementation**

```

```

## Graph Traversal

[Useful Slides](https://cs.slides.com/colt_steele/graphs#/44)

*Example Uses:*

- Peer to peer networking
- Web crawlers
- Finding "closest" matches / recommendations
- Shortest path problems
  - GPS Navigation
  - Solving mazes
  - AI (shortest path to win the game)

### Depth First  Graph Traversal

# Dijkstra's Shortest Path Algorithm

# Dynamic Programming

A method for solving a complex problem by breaking it down into a collection of simpler subproblems, solving each of those subproblems just once, and storing their solutions

*Dynamic programming only works on problem with:*

- Optimal Substructure
- Overlapping Subproblems

"Using past knowledge to make solving a future problem easier"

## Overlapping Subproblems

A problem is said to have **overlapping subproblems** if it can be broken down into subproblems which are reused several times

*Example:*

- Fibonacci Sequence

![Overlapping subproblem](https://puu.sh/CBeWU/6c9ee0ddb4.png)

But

![Not overlapping subproblem](https://puu.sh/CBf1m/257221da22.png)

## Optimal Substructure

A problem is said to have **optimal substructure** if an optimal solution can be constructed from optimal solutions of its subproblems

![](https://puu.sh/CBfv0/fa6fc3b988.png)

## Memoization

Storing the results of expensive function calls and returning the cached result when the same input occur again

![](https://puu.sh/CBgu8/ec369a8960.png)

## Tabulation

Storing the result of a previous result in a "table" (usually an array)

Usually done using **iteration**

Better **space complexity** can be achieved using tabluation

![](https://puu.sh/CBh5O/3043baf951.png)

```javascript
function fib(n) {
    if(n <= 2) return 1;
    var fibNums = [0,1,1];
    for(var i = 3; i <= n; i++) {
        fibNums[i] = fibNums[i-1] + fibNums[i-2];
    }
    return fibNums[n];
}
```

