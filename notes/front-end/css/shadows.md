[UP](./index.md)

# box-shadow property
The box-shadow property applies one or more shadows to an element.

The box-shadow property takes values (in this order)for:
- offset-x (how far to push the shadow horizontally from the element), 
- offset-y (how far to push the shadow vertically from the element), 
- blur-radius (optional), 
- spread-radius (optional)
- color value, in that order. 

## Examples
Example of the CSS to create multiple shadows with some blur, at mostly-transparent black colors:  

### Single Shadow

	box-shadow: 0 10px 20px rgba(0,0,0,0.19);
	/*offset-x|offset-y|blur-radius|color value*/

<div style="width:200px;height:200px;box-shadow: 0 10px 20px rgba(0,0,0,0.19);"></div>

### Two Shadows

	box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
	/*offset-x|offset-y|blur-radius|color value*/

<div style="width:200px;height:200px;box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);"></div> 

- 2nd shadow is darker than the 1st shadow
- 2nd shadow is shorter than the 1st shadow