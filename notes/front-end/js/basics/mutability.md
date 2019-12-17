[UP](./index.md)

# Mutability

## primitive type values
Are immutable and are passed by value

	var myStr = "Bob";
	myStr[0] = "J";

cannot change the value of myStr to "Job", because the contents of myStr cannot be altered.  

Note that this does not mean that myStr cannot be changed, just that the individual characters of a string literal cannot be changed. The only way to change myStr would be to assign it with a new string, like this:

	var myStr = "Bob";
	myStr = "Job";

## object type values
Are mutable and are passed by reference (really a pointer is passed)  

	var ourArray = [50,40,30];
	ourArray[0] = 15; // equals [15,40,30]