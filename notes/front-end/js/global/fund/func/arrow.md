[UP](./index.md)

# arrow function
does not have its own this, arguments, super, or new.target.  

These function expressions are best suited for non-method functions, and they cannot be used as constructors.

## Syntax

### basic

	(param1, param2, …, paramN) => { statements } 
	(param1, param2, …, paramN) => expression
	// equivalent to: => { return expression; } 

	// Parentheses are optional when there's only one parameter name:
	(singleParam) => { statements }
	singleParam => { statements }

	// The parameter list for a function with no parameters should be written with a pair of parentheses.
	() => { statements }

### advanced

	// Parenthesize the body of function to return an object literal expression:
	params => ({foo: bar}) 

	// Rest parameters and default parameters are supported
	(param1, param2, ...rest) => { statements } 
	(param1 = defaultValue1, param2, …, paramN = defaultValueN) => { 
	statements } 

	// Destructuring within the parameter list is also supported
	var f = ([a, b] = [1, 2], {x: c} = {x: a + b}) => a + b + c;
	f(); // 6