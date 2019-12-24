## Inheritance

	<style>
	  body {
		background-color: black;
		color: green;
		font-family: monospace;
	  }
	</style>
	<h1>Hello World</h1>  

The h1 element will inherit the color and font-family from the body element.

## What wins

	<style>
	  body {
		background-color: black;
		font-family: monospace;
		color: green;
	  }
	  #orange-text {
		color: orange;
	  }
	  .pink-text {
		color: pink;
	  }
	  .blue-text {
		color: blue;
	  }
	</style>
	<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>

**green < pink < blue < orange < white**  
**(type sel < class sel < id sel < inline style)**

### !important
There's one last way to override CSS. This is the most powerful method of all. But before we do it, let's talk about why you would ever want to override CSS.

In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important

	.pink-text {
		color: pink !important;
	}

Now pink wins.