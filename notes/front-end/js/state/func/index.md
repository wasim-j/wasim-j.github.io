[UP](../index.md)

[Function Reference](../../global/fund/func/index.md)

# Function Statements

## function
defines a function with the specified parameters  

	function name([param[, param,[..., param]]]) {
	   [statements]
	}

## return
ends function execution and specifies a value to be returned to the function caller.

	return [[expression]]; 

## function*
defines a generator function, which returns a Generator object.

	function* name([param[, param[, ... param]]]) {
	   statements
	}

## async function
defines an asynchronous function, which returns an AsyncFunction object

	async function name([param[, param[, ... param]]]) {
	   statements
	}