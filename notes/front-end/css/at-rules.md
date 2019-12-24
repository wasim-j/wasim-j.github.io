# @rules
an At-rule is a CSS statement that instructs CSS how to behave  

Not Nested:
- @charset	`@charset "utf-8";` must be placed at the top of, and can only appear in an external style sheet
- @import	`@import url;` or `@import url list-of-media-queries;`. Will only load the resource if the media queries are supported

Nested:
- @media
- [@font-face](./fonts-google.md#font-face)
- [@keyframes](./animate/keyframes.md)

## Media Queries
Change the presentation of content based on different viewport sizes.  

The viewport is a user's visible area of a web page, and is different depending on the device used to access the site.

Media Queries consist of a media type, and if that media type matches the type of device the document is displayed on, the styles are applied.  
You can have as many selectors and styles inside your media query as you want.

### Examples
Here's an example of a media query that returns the content **when the device's width is less than or equal to 100px**:

	@media (max-width: 100px) { /* CSS Rules */ }

and the following media query returns the content **when the device's height is more than or equal to 350px**:

	@media (min-height: 350px) { /* CSS Rules */ }