[UP](./index.md)


# Scope
In JS, scope refers to the visibility of variables.  

##  global scope
Variables which are defined outside of a function block have Global scope.  

This means, they can be seen everywhere in your JavaScript code.

### var keyword
Variables which are used without the var keyword are automatically created in the global scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with var.

## local scope
Variables which are declared within a function, as well as the function parameters have local scope.  

That means, they are only visible within that function.


## local and global example
It is possible to have both local and global variables with the same name. When you do this, the local variable takes precedence over the global variable.

	var someVar = "Hat";
	function myFun() {
	  var someVar = "Head"; //will return "Head" because the local version of the variable is present
	  return someVar;
	}
