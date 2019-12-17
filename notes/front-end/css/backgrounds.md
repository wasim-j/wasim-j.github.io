[UP](./index.md)

# background property
The following functions work on the css `background` property'

## linear-gradient()
CSS provides the ability to use color transitions, otherwise known as gradients, on elements.  
This is accessed through the **background property's linear-gradient() function**.  

Here is the general syntax:

	background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);

- first argument specifies the direction from which color transition starts - it can be stated as a degree, where 90deg makes a vertical gradient and 45deg is angled like a backslash. 
- The following arguments specify the order of colors used in the gradient.  

Example:

	background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));

<div style="height:200px;width:200px;background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255))"></div>

## repeating-linear-gradient()
The repeating-linear-gradient() function is very similar to linear-gradient() with the **major difference that it repeats the specified gradient pattern**.  

repeating-linear-gradient() accepts a variety of values, but for simplicity, you'll work with an angle value and color stop values in this challenge.  

For this example, it helps to think about the color stops as pairs where every two colors blend together.  

	0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px

If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.  

	background: repeating-linear-gradient(
		  90deg,
		  yellow 0px,
		  blue 40px,
		  green 40px,
		  red 80px
		);
		

<div style="height:200px;width:200px;background: repeating-linear-gradient(90deg,yellow 0px,blue 40px,green 40px,red 80px);"></div>
  
  
yellow and black stripes:

	background: repeating-linear-gradient(
		  45deg,
		  yellow 0px,
		  yellow 40px,
		  black 40px,
		  black 80px
		);

<div style="height:200px;width:200px;background: repeating-linear-gradient(90deg,yellow 0px,yellow 40px,black 40px,black 80px);"></div>

## url() - Subtle Pattern as a Background Image
One way to add texture and interest to a background and have it stand out more is to add a subtle pattern. The key is balance, as you don't want the background to stand out too much, and take away from the foreground. The background property supports the url() function in order to link to an image of the chosen texture or pattern. The link address is wrapped in quotes inside the parentheses.

The angle value is the direction of the gradient. Color stops are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.

	background: url( https://i.imgur.com/MJAkxbh.png)

<div style="height:200px;width:200px;background: url(./bg-url.png);"></div>