[UP](../index.md)

# Error
The Error constructor creates an error object.  

Instances of Error objects are thrown when runtime errors occur.  

The Error object can also be used as a base object for user-defined exceptions. See below for standard built-in error types.

Syntax  

	new Error([message[, fileName[, lineNumber]]])

[Standard Built-In Error types](./type.md)

## properties

### Error.prototype
Allows the addition of properties to Error instances.

## methods
The global Error object contains no methods of its own, however, it does inherit some methods from the prototype chain.

# Error instances
All Error instances and instances of non-generic errors inherit from Error.prototype.  

As with all constructor functions, you can use the prototype of the constructor to add properties or methods to all instances created with that constructor.

## properties

### Error.prototype.constructor
Specifies the function that created an instance's prototype.

### Error.prototype.message
Error message.

### Error.prototype.name
Error name.

## methods

### Error.prototype.toSource()
Returns a string containing the source of the specified Error object; you can use this value to create a new object. Overrides the Object.prototype.toSource() method.

### Error.prototype.toString()
Returns a string representing the specified object. Overrides the Object.prototype.toString() method.

# Error Handling
- Throwing a generic error
- Handling a specific error
- Custom Error Types