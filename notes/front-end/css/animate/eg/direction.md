[UP](../index.md)

## Direction Example
<style>
#one {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-direction: normal;
	animation-iteration-count: infinite;
}

#two {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-direction: reverse;
	animation-iteration-count: infinite;
}

#three {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-direction: alternate;
	animation-iteration-count: infinite;
}

#four {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-direction: alternate-reverse;
	animation-iteration-count: infinite;
}

@keyframes change {
	from {background-color: red;}
	to {background-color: yellow;}
}
</style>
<div style="display:flex">
Value = normal
<div id="one"></div>  

Value = reverse
<div id="two"></div>  

Value = alternate
<div id="three"></div>  

Value = alternate-reverse
<div id="four"></div>
</div>
HTML:  

	<div id="one"></div>  
	<div id="two"></div>
	<div id="three"></div>
	<div id="four"></div>

CSS:
	#eg {
		height: 100px;
		width: 100px;
		background-color: red;
		animation-name: change;
		animation-duration: 3s;
		animation-direction: /*normal, reverse, alternate, alternate-reverse*/
	}

	@keyframes change {
		from {background-color: red;}
		to {background-color: yellow;}
	}