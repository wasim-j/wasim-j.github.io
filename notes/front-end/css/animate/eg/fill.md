[UP](../index.md)

## fill-mode Example
<style>
#one {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-fill-mode: none;
}

#two {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-fill-mode: forwards;
}

#three {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-fill-mode: backwards;
}

#four {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-fill-mode: both;
}

@keyframes change {
	from {background-color: red;}
	to {background-color: yellow;}
}
</style>
<div style="display:flex">
Value = none
<div id="one"></div>  

Value = forwards
<div id="two"></div>  

Value = backwards
<div id="three"></div>  

Value = both
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