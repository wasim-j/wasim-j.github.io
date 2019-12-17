[UP](../index.md)

# Date Object
- [properties](./const-props.md)
- [methods](./const-meth.md)  

Creates a JavaScript Date instance that represents a single moment in time.  
Date objects are based on a time value that is **the number of milliseconds since 1 January 1970 UTC**.

Syntax:

	new Date();
	new Date(value);
	new Date(dateString);
	new Date(year, monthIndex [, day [, hours [, minutes [, seconds [, milliseconds]]]]]);

## Note 
JS Date objects can only be instantiated by calling JavaScript Date as a constructor:  
- calling it as a regular function (i.e. without the new operator) will return a string rather than a Date object; unlike other JavaScript object types, **JavaScript Date objects have no literal syntax**.

## Date Instances
All Date instances inherit from Date.prototype.  

The prototype object of the Date constructor can be modified to affect all Date instances.  

- [properties](./inst-props.md)
- [methods](./inst-meth.md)