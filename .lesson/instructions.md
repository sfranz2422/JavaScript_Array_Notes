# JavaScript Arrays


# Store Multiple Values in one Variable using JavaScript Arrays

With JavaScript array variables, we can store several pieces of data in one place.

You start an array declaration with an opening square bracket, end it with a closing square bracket, and put a comma between each entry, like this:
```js
const sandwich = ["peanut butter", "jelly", "bread"];
```
Modify the new array myArray so that it contains both a string and a number (in that order).
```js
// Only change code below this line
const myArray = [];

```
# Nest one Array within Another Array

You can also nest arrays within other arrays, like below:
```js
const teams = [["Bulls", 23], ["White Sox", 45]];
```
This is also called a multi-dimensional array.

# Exercise
Create a nested array called ```myArray```.

```js
// Only change code below this line
const myArray = [];

```


# Access Array Data with Indexes

We can access the data inside arrays using indexes.

Array indexes are written in the same bracket notation that strings use, except that instead of specifying a character, they are specifying an entry in the array. Like strings, arrays use zero-based indexing, so the first element in an array has an index of 0.

Example
```js
const array = [50, 60, 70];
console.log(array[0]);
const data = array[1];
```
The ```console.log(array[0])``` prints 50, and data has the value 60.


# Exercise
Create a variable called ```myData ```and set it to equal the first value of myArray using bracket notation.
```js

const myArray = [50, 60, 70];


```
# Modify Array Data With Indexes

Unlike strings, the entries of arrays are mutable and can be changed freely, even if the array was declared with const.

Example
```js
const ourArray = [50, 40, 30];
ourArray[0] = 15;
```
ourArray now has the value [15, 40, 30].

Note: There shouldn't be any spaces between the array name and the square brackets, like array ```[0]```. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

# Exercise
Modify the data stored at index 0 of myArray to a value of 45.

```js
// Setup
const myArray = [18, 64, 99];

// Only change code below this line


```
# Access Multi-Dimensional Arrays With Indexes

One way to think of a multi-dimensional array, is as an array of arrays. When you use brackets to access your array, the first set of brackets refers to the entries in the outer-most (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

Example
```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```
In this example, subarray has the value ```[[10, 11, 12], 13, 14]```, ```nestedSubarray``` has the value ```[10, 11, 12]```, and element has the value 11 .

Note: There shouldn't be any spaces between the array name and the square brackets, like array ```[0][0]``` and even this array ```[0] [0] ```is not allowed. Although JavaScript is able to process this correctly, this may confuse other programmers reading your code.

Using bracket notation select an element from myArray such that myData is equal to 8.

# Exercise

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[0][0];

```

# Manipulate Arrays With push()

An easy way to append data to the end of an array is via the ```push() ```function.

```.push()``` takes one or more parameters and "pushes" them onto the end of the array.

Examples:
```js
const arr1 = [1, 2, 3];
arr1.push(4);

const arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```
arr1 now has the value ```[1, 2, 3, 4]``` and arr2 has the value ```["Stimpson", "J", "cat", ["happy", "joy"]]```.

# Exercise

Push ```["dog", 3] ```onto the end of the myArray variable.
```js
// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line

```

# Manipulate Arrays With pop()

Another way to change the data in an array is with the ```.pop() ```function.

```.pop() ```is used to pop a value off of the end of an array. We can store this popped off value by assigning it to a variable. In other words, ```.pop()``` removes the last element from an array and returns that element.

Any type of entry can be popped off of an array - numbers, strings, even nested arrays.
```js
const threeArr = [1, 4, 6];
const oneDown = threeArr.pop();
console.log(oneDown);
console.log(threeArr);
```
The first console.log will display the value 6, and the second will display the value``` [1, 4]```.
# Exercise
Use the ```.pop()``` function to remove the last item from ```myArray ```and assign the popped off value to a new variable,``` removedFromMyArray```.

```js

// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line

```

# Manipulate Arrays With shift()

```pop()``` always removes the last element of an array. What if you want to remove the first?

That's where ``` .shift()``` comes in. It works just like``` .pop()```, except it removes the first element instead of the last.

Example:
```js
const ourArray = ["Stimpson", "J", ["cat"]];
const removedFromOurArray = ourArray.shift();
```
```removedFromOurArray``` would have a value of the string Stimpson, and ourArray would have``` ["J", ["cat"]]```.
# Exercise
Use the ```.shift() ```function to remove the first item from``` myArray ```and assign the ```"shifted off"``` value to a new variable, ```removedFromMyArray```.
```js
// Setup
const myArray = [["John", 23], ["dog", 3]];

// Only change code below this line

```

# Manipulate Arrays With unshift()

Not only can you shift elements off of the beginning of an array, you can also unshift elements to the beginning of an array i.e. add elements in front of the array.

``` .unshift() ```works exactly like ```.push()```, but instead of adding the element at the end of the array,``` unshift() ```adds the element at the beginning of the array.

Example:
```js
const ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```
After the shift, ourArray would have the value``` ["J", "cat"]```. After the unshift, ourArray would have the value ```["Happy", "J", "cat```
# Exercise
Add ```["Paul", 35]``` to the beginning of the ```myArray``` variable using ```unshift()```.


```js

// Setup
const myArray = [["John", 23], ["dog", 3]];
myArray.shift();

// Only change code below this line

```

# Shopping List

# Exercise
Create a shopping list in the variable ``` myList```. The list should be a multi-dimensional array containing several sub-arrays.

The first element in each sub-array should contain a string with the name of the item. The second element should be a number representing the quantity i.e.
```js
["Chocolate Bar", 15]
```
There should be at least 5 sub-arrays in the list.

Start with the code below:
```js

const myList = [];
```