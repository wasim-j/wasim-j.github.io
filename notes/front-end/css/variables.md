[UP](./index.md)

# CSS Variables
A powerful way to change many CSS style properties at once by changing only one value.

## creation
To create a CSS Variable, you just need to give it a name with two dashes in front of it and assign it a value like this:

	--penguin-skin: gray;

This will create a variable named `--penguin-skin` and assign it the value of `gray`.  

Now you can use that variable elsewhere in your CSS to change the value of other elements to gray.

## assignment
After you create your variable, you can assign its value to other CSS properties by referencing the name you gave it.  

	background: var(--penguin-skin);

This will change the background of whatever element you are targeting to gray because that is the value of the `--penguin-skin` variable.

### fallback value

	background: var(--penguin-skin, black);

This will set background to black if your variable wasn't set.

## browser fallbacks for compatability
Internet Explorer will ignore the background color because it does not support CSS variables.In that case:  
- the browser will use whatever value it has for that property
- if it can't find any other value set for that property, it will revert to the default value, which is typically not ideal.

### Solution
This means that if you do want to provide a browser fallback, it's as easy as providing another more widely supported value immediately before your declaration. That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.

	<style>
	  :root {
		--red-color: red;
	  }
	  .red-box {
		background: red; /* fallback is provided here */
		background: var(--red-color); /* if browser can't recognise the variable, at least red has already been set */
		height: 200px;
		width:200px;
	  }
	</style>
	<div class="red-box"></div>

## Cascading CSS variables
When you create a variable, it becomes available for you to use inside the element in which you create it. It also becomes available within any elements nested within it. This effect is known as cascading.

### :root element
The `:root` selector matches the document's root element.  

In HTML, the root element is always the html element.  
Because of cascading, CSS variables are often defined in the :root element.  

By creating your variables in :root, they will be available throughout the whole web page.

## media query to change a variable
CSS Variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.