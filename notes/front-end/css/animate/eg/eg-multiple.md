[UP](../index.md)

# Setting multiple animation property values

<style>
#one {
	height: 100px;
	width: 100px;
	background-color: red;
	animation-name: fadeInOut, moveLeft300px, bounce;
	animation-duration: 6s, 5s, 1s;
	animation-iteration-count: 2, 1, 5;
}

@keyframes fadeInOut {
	from {opacity: 1;}
	50% {opacity: 0.5}
	to {opacity: 1;}
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
		animation-name: fadeInOut, moveLeft300px, bounce;
		animation-duration: 2.5s, 5s, 1s;
		animation-iteration-count: 2, 1, 5;
	}

	@keyframes change {
		from {background-color: red;}
		to {background-color: yellow;}
	}