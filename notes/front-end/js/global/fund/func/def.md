[UP](./index.md)

# Defining a function

## declaration

	function name([param[, param[, ... param]]]) {
	   statements
	}

## named function expression

	let x = function y ([param[, param[, ... param]]]) {
	   statements
	}

## anonymous function expression

	let x = function ([param[, param[, ... param]]]) {
	   statements
	}

## arrow function

	([param[, param]]) => {
	   statements
	}

	param => expression

## Function constructor

	let x = new Function (arg1, arg2, ... argN, functionBody)

### difference between Function constructor and function declaration
Functions created with the Function constructor **do not create closures** to their creation contexts; **they always are created in the global scope**.  

When running them, they will only be able to access their own local variables and global ones, not the ones from the scope in which the Function constructor was created.