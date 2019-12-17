[UP](../index.md)

## Delay Example
<style>
#one {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: change;
	animation-duration: 3s;
	animation-delay: 3s;
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
		animation-name: change;
		animation-duration: 3s;
		animation-delay: 3s;
	}

	@keyframes change {
		from {background-color: red;}
		to {background-color: yellow;}
	}