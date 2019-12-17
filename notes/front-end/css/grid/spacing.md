[UP](./index.md)

# Grid Item Manipulation
- **grid-column** property -control the amount of columns an item will consume
- **grid-row** property -control the amount of rows an item will consume

![control-spacing](./control-spacing.png)

	.item4{
		background:LightPink;
		grid-row: 2/4; /* starts at vertical line 1 ends at vertical line 4 */
	}
	.item5 {
		background: PaleGreen;
		grid-column: 2/4; /* starts at horizontal line 1 ends at horizontal line 4 */
	}

<style>
  .item1{background:LightSkyBlue;}
  .item2{background:LightSalmon;}
  .item3{background:PaleTurquoise;}
  .item4{
	background:LightPink;
	grid-row: 2/4;
  }
  .item5 {
    background: PaleGreen;
	grid-column: 2/4;
  }
  
  .container1 {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
</style>
  
<div class="container1">
  <div class="item1">1</div>
  <div class="item2">2</div>
  <div class="item3">3</div>
  <div class="item4">4</div>
  <div class="item5">5</div>
</div>

