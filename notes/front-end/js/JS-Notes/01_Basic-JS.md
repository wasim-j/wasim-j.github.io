
**Basic Javascript**

- [Commenting ](#Commenting)
- [Variables ](#Variables)
	- [Assignment ](#Assignment)
	- [Initialising ](#Initialising)
		- [Uninitialized Variables ](#Uninitialized_Variables)
	- [Case-Sensitivity ](#Case-Sensitivity)
- [Numbers ](#)
	- [Increment/Decrement Operators ](#Increment_Decrement)
	- [Decimals ](#Decimals)
	- [Remainders ](#Remainders)
	- [Compound Assignment (+=, -=, *=, /=) ](#Compound_Assignment)
	- [Generating Random Numbers ](#Generating_Random_Numbers)
		- [Random Fractions ](#Random_Fractions)
		- [Random Whole Numbers ](#Random_Whole_Numbers)
			- [Within a Range ](#Within_a_Range)
	- [String to Integer ](#String_to_Integer)
		- [Radix ](#Radix)
- [Strings ](#)
	- [Escaping Literal Quotes ](#Escaping_Literal_Quotes)
		- [Single Quotes (Without Escaping) ](#Single_Quotes)
	- [Other Escape Sequences ](#Other_Escape_Sequences)
	- [Concatenating Strings (using + and +=) ](#Concatenating_Strings)
	- [String Length ](#String_Length)
	- [Find String Character (Using Bracket Notation) ](#Find_String_Character)
		- [Last Character in a String ](#Last_Character_in_a_String)
	- [String Immutability ](#String_Immutability)

# Commenting <a name="Commenting"></a>
As you write code, you should regularly add comments to clarify the function of parts of your code. 
Good commenting can help communicate the intent of your code—both for others and for your future self.

```javascript
// This is an in-line comment.

/* This is a 
   	multi-line comment */
```

# Variables <a name="Variables"></a>
In computer science, data is anything that is meaningful to the computer.

JavaScript provides seven different data types which are undefined, null, boolean, string, symbol, number, and object.

For example, computers distinguish between numbers, such as the number 12, and strings, such as "12", "dog", or "123 cats", which are collections of characters. This is important: computers can perform mathematical operations on a number, but not on a string.


Variables allow computers to store and manipulate data in a dynamic fashion. They do this by using a "label" to point to the data rather than using the data itself.

Variables are similar to the x and y variables you use in mathematics, which means they're a simple name to represent the data we want to refer to. Computer variables differ from mathematical variables in that they can store different values at different times.

We tell JavaScript to create or declare a variable by putting the keyword var in front of it, like so:
```javascript
var ourName;
```

Variable names can be made up of numbers, letters, and $ or _, but may not contain spaces or start with a number.

## Assignment <a name="Assignment"></a>
In JavaScript, you can store a value in a variable with the assignment operator.

```javascript
myVariable = 5; //Assigns the Number value 5 to myVariable.
```
Assignment always goes from right to left.

Everything to the right of the = operator is resolved before the value is assigned to the variable to the left of the operator.

## Initialising <a name="Initialising"></a>
It is common to initialize a variable to an initial value in the same line as it is declared:
```javascript
var myVar = 0;
```
### Uninitialized Variables <a name="Uninitialized_Variables"></a>
When JavaScript variables are declared, they have an initial value of undefined.


If you do a mathematical operation on an undefined variable your result will be NaN which means "Not a Number". 

If you concatenate a string with an undefined variable, you will get a literal string of "undefined".


## Case-Sensitivity <a name="Case-Sensitivity"></a>
In JavaScript all variables and function names are case sensitive. This means that capitalization matters. MYVAR is not the same as MyVar nor myvar. 

It is possible to have multiple distinct variables with the same name but different casing. It is strongly recommended that for the sake of clarity, you do not use this language feature.

# Numbers <a name="Numbers"></a>
## Increment/Decrement Operators <a name="Increment_Decrement"></a>
Increment or add one to a variable with the ++ operator. i++; is the equivalent of i = i + 1;

Decrement or decrease a variable by one with the -- operator. i--; is the equivalent of i = i - 1;

## Decimals <a name="Decimals"></a>
Decimal numbers are sometimes referred to as floating point numbers or floats.

Not all real numbers can accurately be represented in floating point. This can lead to rounding errors.

## Remainders <a name="Remainders"></a>
The remainder operator % gives the remainder of the division of two numbers.

In mathematics, a number can be checked to be even or odd by checking the remainder of the division of the number by 2. 

17 % 2 = 1 (17 is Odd) 

48 % 2 = 0 (48 is Even)

Note: The remainder operator is sometimes incorrectly referred to as the "modulus" operator. It is very similar to modulus, but does not work properly with negative numbers.

## Compound Assignment (+=, -=, *=, /=) <a name="Compound_Assignment"></a>
In programming, it is common to use assignments to modify the contents of a variable. 
Remember that everything to the right of the equals sign is evaluated first, so we can say: 

myVar = myVar + 5; to add 5 to myVar. 

Since this is such a common pattern, there are operators which do both a mathematical operation and assignment in one step.

## Generating Random Numbers <a name="Generating_Random_Numbers"></a>
### Random Fractions <a name="Random_Fractions"></a>
JavaScript has a Math.random() function that generates a random decimal number between 0 (inclusive) and not quite up to 1 (exclusive). 

Thus Math.random() can return a 0 but never quite return a 1

### Random Whole Numbers <a name="Random_Whole_Numbers"></a>
Use Math.random() to generate a random decimal.

Multiply that random decimal by 20.

Use another function, Math.floor() to round the number down to its nearest whole number.

Putting everything together, this is what our code looks like: 

Math.floor(Math.random() * 20); // whole number between 0 and 19
         
#### Within a Range <a name="Within_a_Range"></a>
To do this, we'll define a minimum number min and a maximum number max.Here's the formula we'll use. Take a moment to read it and try to understand what this code is doing: 

Math.floor(Math.random() * (max - min + 1)) + min

## String to Integer <a name="String_to_Integer"></a>
The parseInt() function parses a string and returns an integer. Here's an example: 
```javascript
var a = parseInt("007");
```	
The above function converts the string "007" to an integer 7. If the first character in the string can't be converted into a number, then it returns NaN.

### Radix <a name="Radix"></a>
It takes a second argument for the radix, which specifies the base of the number in the string. The radix can be an integer between 2 and 36.The function call looks like: 

parseInt(string, radix);
		
And here's an example: 
```javascript
var a = parseInt("11", 2);
```		
The radix variable says that "11" is in the binary system, or base 2. This example converts the string "11" to an integer 3.

# Strings <a name="Strings"></a>
```javascript
var myName = "your name";
```
"your name" is called a string literal. It is a string because it is a series of zero or more characters enclosed in single or double quotes.

## Escaping Literal Quotes <a name="Escaping_Literal_Quotes"></a>
When you are defining a string you must start and end with a single or double quote. What happens when you need a literal quote: " or ' inside of your string?

In JavaScript, you can escape a quote from considering it as an end of string quote by placing a backslash (\) in front of the quote.
```javascript
var sampleStr = "Alan said, \"Peter is learning JavaScript\".";
```

This signals to JavaScript that the following quote is not the end of the string, but should instead appear inside the string. 
So if you were to print this to the console, you would get: 

Alan said, "Peter is learning JavaScript".

### Single Quotes (Without Escaping) <a name="Single_Quotes"></a>
String values in JavaScript may be written with single or double quotes, so long as you start and end with the same type of quote. 
Unlike some languages, single and double quotes are functionally identical in JavaScript.

"This string has \"double quotes\" in it"

The value in using one or the other has to do with the need to escape quotes of the same type. 
Unless they are escaped, you cannot have more than one pair of whichever quote type begins a string.

## Other Escape Sequences <a name="Other_Escape_Sequences"></a>
Quotes are not the only characters that can be escaped inside a string. There are two reasons to use escaping characters: 

First is to allow you to use characters you might not otherwise be able to type out, such as a backspace. 

Second is to allow you to represent multiple quotes in a string without JavaScript misinterpreting what you mean.
```javascript
myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
```

## Concatenating Strings (using + and +=) <a name="Concatenating_Strings"></a>
In JavaScript, when the + operator is used with a String value, it is called the concatenation operator. 
You can build a new string out of other strings by concatenating them together. 

eg. 'My name is Alan,' + ' I concatenate.'

Note: Watch out for spaces. Concatenation does not add spaces between concatenated strings, so you'll need to add them yourself.

We can also use the += operator to concatenate a string onto the end of an existing string variable. 
This can be very helpful to break a long string over several lines.

## String Length <a name="String Length"></a>
You can find the length of a String value by writing .length after the string variable or string literal. 

eg. "Alan Peter".length; // 10

## Find String Character (Using Bracket Notation) <a name="Find_String_Character"></a>
Bracket notation is a way to get a character at a specific index within a string.
Most modern programming languages, like JavaScript, don't start counting at 1 like humans do. They start at 0. This is referred to as Zero-based indexing.

For example, the character at index 0 in the word "Charles" is "C". 

So if var firstName = "Charles", you can get the value of the first letter of the string by using firstName[0].

### Last Character in a String <a name="Last_Character_in_a_String"></a>
In order to get the last letter of a string, you can subtract one from the string's length.

For example, if var firstName = "Charles", you can get the value of the last letter of the string by using firstName[firstName.length - 1].

## String Immutability <a name="String_Immutability"></a>
In JavaScript, String values are immutable, which means that they cannot be altered once created.

For example, the following code: 
```javascript
var myStr = "Bob";
myStr[0] = "J"; //cannot change the value of myStr to "Job", because the contents of myStr cannot be altered. 
```
Note that this does not mean that myStr cannot be changed, just that the individual characters of a string literal cannot be changed. 
The only way to change myStr would be to assign it with a new string, like this: 
```javascript
var myStr = "Bob"; //myStr = "Job";
```
