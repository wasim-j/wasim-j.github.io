[UP](./index.md)

# parameters

## default parameters
allow named parameters to be initialized with default values if no value or undefined is passed.

	function [name]([param1[ = defaultValue1 ][, ..., paramN[ = defaultValueN ]]]) {
	   statements
	}

## rest parameters
allows us to represent an indefinite number of arguments as an array

	function f(a, b, ...theArgs) {
	  // ...
	}