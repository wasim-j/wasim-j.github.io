[UP](./index.md)

# getter and setter methods

You can define getters (accessor methods) and setters (mutator methods) on any standard built-in object or user-defined object that supports the addition of new properties.  

The syntax for defining getters and setters uses the object literal syntax.

	var obj = {
	  get property() {},
	  set property(value) {}
	};

## get
Binds an object property to a function that will be called when that property is looked up.

## set
Binds an object property to a function to be called when there is an attempt to set that property.