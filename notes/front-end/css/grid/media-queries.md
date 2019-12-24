[UP](./index.md)

# Using Media Queries
CSS Grid can be an easy way to make your site more responsive by using media queries to rearrange grid areas, change dimensions of a grid, and rearrange the placement of items.

## Example

	<div class="container">
	  <div class="item1">header</div>
	  <div class="item2">advert</div>
	  <div class="item3">content</div>
	  <div class="item4">footer</div>
	</div>

[Example Link](./eg-mq.html)

<style>
  .item1 {
    background: LightSkyBlue;
    grid-area: header;
  }
  
  .item2 {
    background: LightSalmon;
    grid-area: advert;
  }
  
  .item3 {
    background: PaleTurquoise;
    grid-area: content;
  }
  
  .item4 {
    background: lightpink;
    grid-area: footer;
  }
  
  .container {
    font-size: 1.5em;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 50px auto 1fr auto;
    grid-gap: 10px;
    grid-template-areas:
      "header"
      "advert"
      "content"
      "footer";
  }
  
  @media (min-width: 750px){
    .container{
      grid-template-columns: auto 1fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
  }
  
  @media (min-width: 1000px){
    .container{ 
      grid-template-areas:
        "header header"
        "advert content"
        "footer footer";
    }
  }

</style>
  
<div class="container">
  <div class="item1">header</div>
  <div class="item2">advert</div>
  <div class="item3">content</div>
  <div class="item4">footer</div>
</div>

	.item1 {
		background: LightSkyBlue;
		grid-area: header;
	}

	.item2 {
		background: LightSalmon;
		grid-area: advert;
	}

	.item3 {
		background: PaleTurquoise;
		grid-area: content;
	}

	.item4 {
		background: lightpink;
		grid-area: footer;
	}

	.container {
		font-size: 1.5em;
		min-height: 300px;
		width: 100%;
		background: LightGray;
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 50px auto 1fr auto;
		grid-gap: 10px;
		grid-template-areas:
		  "header"
		  "advert"
		  "content"
		  "footer";
	}

When the viewport width is 750px or more, the number of columns changes from 1 to 2. The advertisement area then occupies the left column completely

	@media (min-width: 750px){
		.container{
		  grid-template-columns: auto 1fr;
		  grid-template-rows: auto 1fr auto;
		  grid-template-areas:
			"advert header"
			"advert content"
			"advert footer";
		}
	}

When the viewport width is 1000px or more, make the header area occupy the top row completely and the footer area occupy the bottom row completely.

	@media (min-width: 1000px){
		.container{ 
		  grid-template-areas:
			"header header"
			"advert content"
			"footer footer";
		}
	}