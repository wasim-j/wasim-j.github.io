[UP](../index.md)

# Function
Creates:
- a new Function object.  
-  functions which execute in the global scope only.

Syntax:

	new Function ([arg1[, arg2[, ...argN]],] functionBody)

The global Function object has **no methods or properties of its own**.  

However, since it is a function itself, it does inherit some methods and properties through the prototype chain from Function.prototype.

## Function prototype object
Every function in JavaScript is a Function object - that is it is an instance of the Function constructor.  

In JavaScript, functions are first-class objects: because they can have properties and methods just like any other object.  

What distinguishes them from other objects is that functions can be called.

- [properties](./inst-props.md)
- [methods](./inst-meth.md)

### Using a function object
#### [parameters](./params.md)
#### [arguments](./args.md)
#### [defining](./def.md)