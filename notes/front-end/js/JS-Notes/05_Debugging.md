Debugging is the process of finding exactly what isn't working and fixing it.

After spending time creating a brilliant block of code, it is tough realizing it may have errors. 
These issues generally come in three forms: 

__Syntax Errors__ that prevent a program from running,

Example of a syntax error - often detected by the code editor:
```javascript
funtion willNotWork( {console.log("Yuck");}	
// "function" keyword is misspelled and there's a missing parenthesis
```
__Runtime Errors__ when code fails to execute or has unexpected behavior, and

Here's an example of a runtime error - often detected while the program executes:
```javascript
function loopy() {while(true) {console.log("Hello, world!");}}	
// Calling loopy starts an infinite loop, which may crash your browser
```
__Semantic (or Logical) Errors__ when code doesn't do what it's meant to.
Example of a semantic error - often detected after testing code output:
```javascript
function calcAreaOfRect(w, h) {return w + h; // This should be w * h}
let myRectArea = calcAreaOfRect(2, 3);	
// Correct syntax and the program executes, but this gives the wrong answer
```

Modern code editors (and experience) can help identify syntax errors. 

Semantic and runtime errors are harder to find. They may cause your program to crash, make it run forever, or give incorrect output.

Think of debugging as trying to understand why your code is behaving the way it is.

# By Elimination
Debugging is frustrating, but it helps to develop (and follow) a step-by-step approach to review your code. 
This means checking the intermediate values and types of variables to see if they are what they should be. 
You can start with a simple process of elimination.

For example, if function A works and returns what it's supposed to, then function B may have the issue. 
Or start checking values in a block of code from the middle to try to cut the search space in half. 
A problem in one spot indicates a bug in the first half of the code. If not, it's likely in the second.

# Browser Console
Both Chrome and Firefox have excellent JavaScript consoles, also known as DevTools, for debugging your JavaScript.

You can find Developer tools in your Chrome's menu or Web Console in FireFox's menu. 
If you're using a different browser, or a mobile phone, we strongly recommend switching to desktop Firefox or Chrome.

The console.log() method, which "prints" the output of what's within its parentheses to the console, will likely be the most helpful debugging tool. 
Placing it at strategic points in your code can show you the intermediate values of variables. 
It's good practice to have an idea of what the output should be before looking at what it is. 
Having check points to see the status of your calculations throughout your code will help narrow down where the problem is.

# typeof Operator
You can use typeof to check the data structure, or type, of a variable. This is useful in debugging when working with multiple data types. 
If you think you're adding two numbers, but one is actually a string, the results can be unexpected. Type errors can lurk in calculations or function calls. 
Especially take care when you're accessing and working with external data in the form of a JavaScript object (JSON).Here are some examples using typeof:
```javascript    
console.log(typeof ""); // outputs "string"
console.log(typeof 0); // outputs "number"
console.log(typeof []); // outputs "object"
console.log(typeof {}); // outputs "object"
```
JavaScript recognizes six primitive (immutable) data types: Boolean, Null, Undefined, Number, String, and Symbol (new with ES6) and one type for mutable items: Object. 
Note that in JavaScript, arrays are technically a type of object.

# Common Mistakes
* Misspelled Variable and Function Names
* Unclosed Parentheses, Brackets, Braces and Quotes
* Mixed Usage of Single and Double Quotes
* Use of = Operator Instead of === Operator
* Missing Open and Closing Parenthesis After a Function Call
* Arguments Passed in the Wrong Order When Calling a Function
* Off By One Errors When Using Indexing

# Beware of Loops
## Use Caution When Reinitializing Variables Inside a Loop
Sometimes it's necessary to save information, increment counters, or re-set variables within a loop. 
A potential issue is when variables either should be reinitialized, and aren't, or vice versa. 
This is particularly dangerous if you accidentally reset the variable being used for the terminal condition, causing an infinite loop. Printing variable values with each cycle of your loop by using console.log() can uncover buggy behavior related to resetting, or failing to reset a variable.

## Prevent Infinite Loops with a Valid Terminal Condition
Loops are great tools when you need your program to run a code block a certain number of times or until a condition is met, but they need a terminal condition that ends the looping. 
Infinite loops are likely to freeze or crash the browser, and cause general program execution mayhem, which no one wants.

There was an example of an infinite loop in the introduction to this section - it had no terminal condition to break out of the while loop inside loopy(). 
```javascript
//Do NOT call this function!
function loopy() {
      while(true) {
        	console.log("Hello, world!");
      }
}
```
It's the programmer's job to ensure that the terminal condition, which tells the program when to break out of the loop code, is eventually reached. 

One error is incrementing or decrementing a counter variable in the wrong direction from the terminal condition. 
Another one is accidentally resetting a counter or index variable within the loop code, instead of incrementing or decrementing it.
