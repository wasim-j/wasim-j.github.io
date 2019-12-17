[UP](./index.md)

# try...catch
marks a block of statements to try, and specifies a response, should an exception be thrown

	try {
	   try_statements
	}
	[catch (exception_var_1 if condition_1) { // non-standard
	   catch_statements_1
	}]
	...
	[catch (exception_var_2) {
	   catch_statements_2
	}]
	[finally {
	   finally_statements
	}]