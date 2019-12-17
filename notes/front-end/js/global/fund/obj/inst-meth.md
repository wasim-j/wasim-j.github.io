[UP](./index.md)

# Object Instance Methods

## Object.prototype.__defineGetter__()
Associates a function with a property that, when accessed, executes that function and returns its return value.

## Object.prototype.__defineSetter__()
Associates a function with a property that, when set, executes that function which modifies the property.

## Object.prototype.__lookupGetter__()
Returns the function associated with the specified property by the __defineGetter__() method.

## Object.prototype.__lookupSetter__()
Returns the function associated with the specified property by the __defineSetter__() method.

## Object.prototype.hasOwnProperty()
Returns a boolean indicating whether an object contains the specified property as a direct property of that object and not inherited through the prototype chain.

## Object.prototype.isPrototypeOf()
Returns a boolean indicating whether the object this method is called upon is in the prototype chain of the specified object.

## Object.prototype.propertyIsEnumerable()
Returns a boolean indicating if the internal ECMAScript [[Enumerable]] attribute is set.

## Object.prototype.toSource()
Returns string containing the source of an object literal representing the object that this method is called upon; you can use this value to create a new object.

## Object.prototype.toLocaleString()
Calls toString().

## Object.prototype.toString()
Returns a string representation of the object.

## Object.prototype.unwatch()
Removes a watchpoint from a property of the object.

## Object.prototype.valueOf()
Returns the primitive value of the specified object.

## Object.prototype.watch()
Adds a watchpoint to a property of the object.