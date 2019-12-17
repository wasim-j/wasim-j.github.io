[UP](./index.md)

# @keyframes
is how to specify exactly what happens within the animation over the duration. 

This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%. 
- If you compare this to a movie, the CSS properties for 0% is how the element displays in the opening scene. 
- The CSS properties for 100% is how the element appears at the end, right before the credits roll. 

Note: Keywords
- for 0% the keyword `from` can be used instead
- for 100% the keyword `to` can be used instead 

Then CSS applies the magic to transition the element over the given duration to act out the scene. Here's an example to illustrate the usage of @keyframes and the animation properties:

## Example

	#anim {
	  animation-name: colorful;
	  animation-duration: 3s;
	}
	@keyframes colorful {
	  0% {
		background-color: blue;
	  }
	  100% {
		background-color: yellow;
	  }
	}

Explanation:
- For the element with the anim id, the code snippet above sets the animation-name to colorful and sets the animation-duration to 3 
seconds. 
- Then the @keyframes rule links to the animation properties with the name colorful. 
- It sets the color to blue at the beginning of the animation (0%) which will transition to yellow by the end of the animation (100%). 
- You aren't limited to only beginning-end transitions, you can set properties for the element for any percentage between 0% and 100%.