[UP](../index.md)

# Creating Motion
When elements have a specified position, such as fixed or relative, the CSS offset properties right, left, top, and bottom can be used in animation rules to create movement.

As shown in the example below, you can push the item downwards then upwards by setting the top property of the 50% keyframe to 50px, but having it set to 0px for the first (0%) and the last (100%) keyframe.

<style>
.box {
    height: 40px;
    width: 70%;
    background: black;
    margin: 50px auto;
    border-radius: 5px;
    position: relative;
  }

#rect {
  animation-name: rainbow;
  animation-duration: 4s;
}

@keyframes rainbow {
  0% {
    background-color: blue;
    top: 0px;
    
  }
  50% {
    background-color: green;
    top: 50px;
    
  }
  100% {
    background-color: yellow;
    top: 0px;
    
  }
}
</style>

<div id="rect" class="box"></div>

HTML:

	<div id="rect" class="box"></div>

CSS:

	.box {
		height: 40px;
		width: 70%;
		background: black;
		margin: 50px auto;
		border-radius: 5px;
		position: relative;
	  }

	#rect {
	  animation-name: rainbow;
	  animation-duration: 4s;
	}

	@keyframes rainbow {
	  0% {
		background-color: blue;
		top: 0px;
		
	  }
	  50% {
		background-color: green;
		top: 50px;
		
	  }
	  100% {
		background-color: yellow;
		top: 0px;
		
	  }
	}