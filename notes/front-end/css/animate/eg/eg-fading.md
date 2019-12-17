[UP](../index.md)

# Create Visual Direction by Fading an Element from Left to Right
<style>

  #ball {
    width: 70px;
    height: 70px;
    margin: 50px auto;
    position: fixed;
    left: 30%;
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    animation-name: fade;
    animation-duration: 3s;
  }

  @keyframes fade {
    50% {
      left: 70%;
      opacity: 0.1;
    }
  }

</style>

<div id="ball"></div>

HTML:

	<div id="ball"></div>

CSS:

	  #ball {
		width: 70px;
		height: 70px;
		margin: 50px auto;
		position: fixed;
		left: 30%;
		border-radius: 50%;
		background: linear-gradient(
		  35deg,
		  #ccffff,
		  #ffcccc
		);
		animation-name: fade;
		animation-duration: 3s;
	  }

	  @keyframes fade {
		50% {
		  left: 70%;
		  opacity: 0.1;
		}
	  }