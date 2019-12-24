[UP](./index.md)

# Alignment
In CSS Grid, the content of each item is located in a box which is referred to as a cell. You can align the content's position within its cell 

## Horizontal

### Individual (justify-self)
align the content's position within its cell 

horizontally using the justify-self property on a grid item. By default, this property has a value of stretch, which will make the content fill the whole width of the cell. 

This CSS Grid property accepts other values as well:

- **start**: aligns the content at the left of the cell,
- **center**: aligns the content in the center of the cell,
- **end**: aligns the content at the right of the cell.


	.item1{
		background:LightSkyBlue;
	}
	.item2{
		background:LightSalmon;
		justify-self: start;
	}
	.item3{
		background:PaleTurquoise;
		justify-self: end;
	}
	.item4{
		background:LightPink;
		justify-self: stretch;
	}

<style>
  .item1{
    background:LightSkyBlue;
	justify-self: center;
  }
  .item2{
    background:LightSalmon;
    justify-self: start;
  }
  .item3{
    background:PaleTurquoise;
    justify-self: end;
  }
  .item4{
    background:LightPink;
    justify-self: stretch
  }
  
  .container {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 10px;
  }
</style>
  
<div class="container">
  <div class="item1">1</div>
  <div class="item2">2</div>
  <div class="item3">3</div>
  <div class="item4">4</div>
</div>

### Collective (justify-items)
Sometimes you want all the items in your CSS Grid to share the same alignment. You can use the previously learned properties and align them individually, or you can align them all at once horizontally by using justify-items on your grid container. This property can accept all the same values you learned about in the previous two challenges, the difference being that it will move all the items in our grid to the desired alignment.

	.containerB {
			...
			justify-items: end;
			...
		}


<style>
  .item5{background:LightSkyBlue;}
  .item6{background:LightSalmon;}
  .item7{background:PaleTurquoise;}
  .item8{background:LightPink;}
  
  .containerB {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 10px;
	justify-items: end;
  }
</style>
  
<div class="containerB">
  <div class="item5">5</div>
  <div class="item6">6</div>
  <div class="item7">7</div>
  <div class="item8">8</div>
</div>

## Vertical

### Individual (align-self)
Just as you can align an item horizontally (using justify-self), there's a way to align an item vertically as well. To do this, you use the align-self property on an item. This property accepts all of the same values as justify-self.

	.item1b{
		background:LightSkyBlue;
		align-self: center;
	}
	.item2b{
		background:LightSalmon;
		align-self: start;
	}
	.item3b{
		background:PaleTurquoise;
		align-self: end;
	}
	.item4b{
		background:LightPink;
		align-self: stretch;
	}

<style>
  .item1b{
    background:LightSkyBlue;
	align-self: center;
  }
  .item2b{
    background:LightSalmon;
    align-self: start;
  }
  .item3b{
    background:PaleTurquoise;
    align-self: end;
  }
  .item4b{
    background:LightPink;
    align-self: stretch
  }
  
  .container2 {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 10px;
  }
</style>
  
<div class="container2">
  <div class="item1b">1</div>
  <div class="item2b">2</div>
  <div class="item3b">3</div>
  <div class="item4b">4</div>
</div>

### Collective (align-items)
Using the align-items property on a grid container will set the vertical alignment for all the items in our grid. Similar to justify-items

	.container2b {
		...
		align-items: end;
		...
	}

<style>
  .item5b{background:LightSkyBlue;}
  .item6b{background:LightSalmon;}
  .item7b{background:PaleTurquoise;}
  .item8b{background:LightPink;}
  
  .container2b {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 10px;
	align-items: end;
  }
</style>
  
<div class="container2b">
  <div class="item5b">5</div>
  <div class="item6b">6</div>
  <div class="item7b">7</div>
  <div class="item8b">8</div>
</div>

## Examples

### Center All

	.container3 {
		...
		justify-items: center;
		align-items: center;
		...
	}

<style>
  .item3v{background:LightSkyBlue;}
  .item3x{background:LightSalmon;}
  .item3y{background:PaleTurquoise;}
  .item3z{background:LightPink;}
  
  .container3 {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    grid-gap: 10px;
	justify-items: center;
	align-items: center;
  }
</style>
  
<div class="container3">
  <div class="item3v">A</div>
  <div class="item3x">B</div>
  <div class="item3y">C</div>
  <div class="item3z">D</div>
</div>
