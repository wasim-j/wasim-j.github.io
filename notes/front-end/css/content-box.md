# content-box
This is the initial and **default value** as specified by the CSS standard.  

The width and height properties **include the content, but does not include the padding, border, or margin**.  

For example, 

	.box {width: 350px; border: 10px solid black;} // renders a box that is 370px wide.

Here, the dimensions of the element are calculated as: 
- width = width of the content,
- height = height of the content.  

(Borders and padding are not included in the calculation.)