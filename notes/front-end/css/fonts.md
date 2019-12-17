[UP](./index.md)

# Typography

## Fonts
There are several default fonts that are available in all browsers.  
These generic font families include: 
- monospace, 
- serif
- sans-serif

Generic font family names are not case-sensitive. Also, they **do not need quotes because they are CSS keywords**.

### Importing a Google Font
Google Fonts is a free library of web fonts that you can use in your CSS by referencing the font's URL.

To import a Google Font, you can copy the font(s) URL from the Google Fonts library and then paste it in your HTML.  

#### method 1: with html
- copy the following code snippet and paste it into the top of your code editor(before the opening style element):


	<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

- Use in your CSS by using Lobster as the FAMILY_NAME as in the following example:  


	font-family: FAMILY_NAME, GENERIC_NAME;.

note:  
- The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available.
- Family names are case-sensitive and **need to be wrapped in quotes if there is a space in the name**.

<h3 id="font-face"> method 2: with CSS </h3>
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

## Properties

### text-align
- text-align: justify; causes all lines of text except the last line to meet the left and right edges of the line box.
- text-align: center; centers the text
- text-align: right; right-aligns the text
- text-align: left; (the default) left-aligns the text.

### text-transform
The text-transform property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.

The following table shows how the different text-transformvalues change the example text "Transform me".

Value	Result
- lowercase	"transform me"
- uppercase	"TRANSFORM ME"
- capitalize	"Transform Me"
- initial	Use the default value
- inherit	Use the text-transform value from the parent element
- none	Default: Use the original text

### font-weight
The font-weight property sets how thick or thin characters are in a section of text.

### line-height
CSS offers the line-height property to change the height of each line in a block of text. As the name suggests, it changes the amount of vertical space that each line of text gets.

## Elements

### bold text - &lt;strong&gt;
To make text bold, you can use the strong tag. This is often used to draw attention to text and symbolize that it is important.

the browser applies the CSS of font-weight: bold; to the element.

### underline - &lt;u&gt;
To underline text, you can use the u tag. This is often used to signify that a section of text is important, or something to remember. With the u tag, the browser applies the CSS of text-decoration: underline; to the element.

### emphasize - &lt;em&gt;
To emphasize text, you can use the em tag. This displays text as italicized, as the browser applies the CSS of font-style: italic; to the element.

### strikethrough - &lt;s&gt;
To strikethrough text, which is when a horizontal line cuts across the characters, you can use the s tag. It shows that a section of text is no longer valid. With the s tag, the browser applies the CSS of text-decoration: line-through; to the element.