[UP](./index.md)

# transform property
the transform property has access to scale(), skewX() and skewY

## scale()
To change the scale of an element, CSS has the transform property, along with its scale() function. The following code example doubles the size of all the paragraph elements on the page:  

	div {transform:scale(2);}

<div style="display:flex;padding:50px">
<div style="width:100px;height:100px;background-color:red;margin-right:100px;">1</div>
<div style="width:100px;height:100px;background-color:yellow;transform:scale(2);margin-right:100px;">2</div>
<div style="width:100px;height:100px;background-color:green;transform:scale(0.5);">0.5</div>
</div>

### using scaling for interactivity
The transform property has a variety of functions that lets you scale, move, rotate, skew, etc., your elements. When used with pseudo-classes such as :hover that specify a certain state of an element, the transform property can easily add interactivity to your elements.

Here's an example to scale the paragraph elements to 2.1 times their original size when a user hovers over them:

	#grow:hover {transform: scale(2.1);}

<style>#grow:hover {transform: scale(2.1);}</style>
<div style="display:flex;padding:50px">
<div id="grow" style="width:100px;height:100px;background-color:blue;">#grow</div>
</div>

## translate()
repositions an element in the horizontal and/or vertical directions  

![alt](./translate.svg)

## skewX() and skewY()
skews the selected element along its X (horizontal) axis by a given degree.

	div {transform: skewX(-32deg);}

<div style="display:flex;padding:80px">
<div style="width:160px;height:160px;background-color:pink;transform: skewX(-32deg);">skewX(-32deg)</div>
</div>


## skewY()
skews the selected element along its Y (vertical) axis by a given degree.

	div {transform: skewY(-32deg);}

<div style="display:flex;padding:80px">
<div style="width:160px;height:160px;background-color:pink;transform: skewY(-32deg);">skewY(-32deg)</div>
</div>
