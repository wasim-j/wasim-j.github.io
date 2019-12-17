[UP](../index.md)

# Array
Used in the construction of arrays; which are high-level, list-like objects.  

## Syntax  

	[element0, element1, ..., elementN]
	new Array(element0, element1[, ...[, elementN]])
	new Array(arrayLength)

## Access
JavaScript arrays are zero-indexed: 
- 1st element of an array is at index 0	`arr[0]`
- last element is at the index equal to the value of the array's length property minus 1	`arr[arr.length - 1]`
- using an invalid index number returns `undefined`

## Properties

### Array.length
The Array constructor's length property whose value is 1.

### get Array[@@species]
The constructor function that is used to create derived objects.

### Array.prototype
Allows the addition of properties to all array objects.

## Methods

### Array.from()
Creates a new Array instance from an array-like or iterable object.

### Array.isArray()
Returns true if a variable is an array, if not false.

### Array.of()
Creates a new Array instance with a variable number of arguments, regardless of number or type of the arguments.

## Array Instances

### Properties

#### Array.prototype.constructor
Specifies the function that creates an object's prototype.

#### Array.prototype.length
Reflects the number of elements in an array.

#### Array.prototype[@@unscopables]
A symbol containing property names to exclude from a with binding scope.

### [Methods](./inst-meths.md)