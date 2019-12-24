[UP](../index.md)

# Making text slide across the browser window
Note that animations like this can cause the page to become wider than the browser window.  

To avoid this problem put the element to be animated in a container, and set `overflow:hidden` on the container.  

<style>
#alice {
  animation-duration: 3s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%; 
  }
  to {
    margin-left: 0%;
    width: 100%;
  }
}
</style>

<div style="overflow:hidden;">
<p id="alice">The Caterpillar and Alice looked at each other for some time in silence:
at last the Caterpillar took the hookah out of its mouth, and addressed
her in a languid, sleepy voice.</p>
</div>  

	#alice {
	  animation-duration: 3s;
	  animation-name: slidein;
	}

	@keyframes slidein {
	  from {
		margin-left: 100%;
		width: 300%; 
	  }
	  to {
		margin-left: 0%;
		width: 100%;
	  }
	}

	<div style="overflow:hidden;">
	<p id="alice">The Caterpillar and Alice looked at each other for some time in silence:
	at last the Caterpillar took the hookah out of its mouth, and addressed
	her in a languid, sleepy voice.</p>
	</div>