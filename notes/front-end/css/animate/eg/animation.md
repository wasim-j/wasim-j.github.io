[UP](../index.md)

## Shorthand Example
<style>
#one {
	height: 100px;
	width: 100px;
	background-color: red;
	/* animation-name, animation-duration, animation-timing-function, animation-delay*/
	animation: change 5s ease-in 5s;
}

@keyframes change {
	from {background-color: red;}
	to {background-color: yellow;}
}
</style>
<div id="one"></div>  

HTML:  

	<div id="one"></div>

CSS:
	#one {
		height: 100px;
		width: 100px;
		background-color: red;
		/* animation-name, animation-duration, animation-timing-function, animation-delay*/
		animation: change 5s ease-in 5s;
	}

	@keyframes change {
		from {background-color: red;}
		to {background-color: yellow;}
	}