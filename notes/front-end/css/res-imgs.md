[UP](./index.md)

# Responsive Images
Making images responsive with CSS is actually very simple. Instead of applying an absolute width to an element:

	img { width: 720px; }

You can use:

	img {
	  max-width: 100%;
	  display: block;
	  height: auto;
	}
	
- The max-width property of 100% scales the image to fit the width of its container, but the image won't stretch wider than its original width. 
- Setting the display property to block changes the image from an inline element (its default), to a block element on its own line.
- The height property of auto keeps the original aspect ratio of the image.

## Use a Retina Image for Higher Resolution Displays
The simplest way to make your images appear "retina" (and optimize them for retina displays) is to define their width and height values as only half of what the original file is.

Here is an example of an image that is only using half of the original height and width:

	<style>
	  img { height: 250px; width: 250px; }
	</style>
	<img src="coolPic500x500" alt="A most excellent picture">