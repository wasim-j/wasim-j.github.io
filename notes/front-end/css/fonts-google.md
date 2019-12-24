# Importing a Google Font
Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL.

To import a Google Font, you can copy the font(s) URL from the Google Fonts library and then paste it in your HTML.  

## method 1: with html
- copy the following code snippet and paste it into the top of your code editor(before the opening style element):


	<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

- Use in your CSS by using Lobster as the FAMILY_NAME as in the following example:  


	font-family: FAMILY_NAME, GENERIC_NAME;.

note:  
- The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.
- Family names are case-sensitive and **need to be wrapped in quotes if there is a space in the name**.

<h2 id="font-face"> method 2: with CSS </h2>
the font can be loaded from either a: 
- remote server: using the url()
- locally-installed font on the user's own computer: using local()  


	@font-face {
	  font-family: MyHelvetica;
	  src: local("Helvetica Neue Bold"),
		   local("HelveticaNeue-Bold"),
		   url(MgOpenModernaBold.ttf);
	  font-weight: bold;
	}