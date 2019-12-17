[UP](./index.md)

# Basics
In CSS Grid:
- parent element is referred to as the **container**
- children are referred to as **items**

## Container Properties

### grid-template-columns
To add some columns to the grid, use the grid-template-columns property on a grid container as demonstrated below:

	.container {
	  display: grid;
	  grid-template-columns: 50px 50px;
	}

This will give your grid two columns that are 50px wide each.

- number of parameters given to the grid-template-columns property indicates the number of columns in the grid
- the value of each parameter indicates the width of each column.

### grid-template-rows
Same idea as grid-template-columns

### grid gaps

#### grid-column-gap
Sometimes you want a gap in between the columns. To add a gap between the columns, use the grid-column-gap property like this:

	grid-column-gap: 10px;

This creates 10px of empty space between all of our columns.

#### grid-column-row
Same idea as grid-column-gap

#### grid-gap
shorthand property for grid-row-gap and grid-column-gap

##### one value
If grid-gap has one value, it will create a gap between all rows and columns.

##### two values
If there are two values:
- first one to set the gap between the rows
- second value for the columns.



## CSS Grid units
You can use absolute and relative units like px and em in CSS Grid to define the size of rows and columns. You can use these as well:
- **fr**: sets the column or row to a fraction of the available space,
- **auto**: sets the column or row to the width or height of its content automatically,
- **%**: adjusts the column or row to the percent width of its container.

### Example

	grid-template-columns: auto 50px 10% 2fr 1fr;

<style>
  .e1{background:LightSkyBlue;}
  .e2{background:LightSalmon;}
  .e3{background:PaleTurquoise;}
  .e4{background:LightPink;}
  .e5{background:PaleGreen;}
  
  .container2 {
    font-size: 40px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: auto 50px 10% 2fr 1fr;
    grid-template-rows: 50px 50px;
  }
</style>

<div class="container2">
  <div class="e1">1</div>
  <div class="e2">2</div>
  <div class="e3">3</div>
  <div class="e4">4</div>
  <div class="e5">5</div>
</div>

This snippet creates five columns. 
- 1st column is as wide as its content
- 2nd column is 50px, 
- 3rd column is 10% of its container, 
- 4th and 5th columns; the remaining space is divided into three sections: two are allocated for the fourth column, and one for the fifth.

## Functions
### repeat()
When you used grid-template-columns and grid-template-rows to define the structure of a grid, you entered a value for each row or column you created.  

Lets say you want a grid with 100 rows of the same height. It isn't very practical to insert 100 values individually. Fortunately, there's a better way - by using the repeat function to specify the number of times you want your column or row to be repeated, followed by a comma and the value you want to repeat.

Here's an example that would create the 100 row grid, each row at 50px tall.

	grid-template-rows: repeat(100, 50px);

You can also repeat multiple values with the repeat function, and insert the function amongst other values when defining a grid structure. Here's what I mean:

	grid-template-columns: repeat(2, 1fr 50px) 20px;

This translates to:

	grid-template-columns: 1fr 50px 1fr 50px 20px;

Note: 1fr 50px is repeated twice followed by 20px.

#### auto-fill
The repeat function comes with an option called auto-fill. This allows you to automatically insert as many rows or columns of your desired size as possible depending on the size of the container. 

You can create flexible layouts when combining auto-fill with minmax.

	grid-template-columns: repeat(auto-fill, minmax(60px, 1fr));

When the container changes size, this setup keeps inserting 60px columns and stretching them until it can insert another one.

Note
If your container can't fit all your items on one row, it will move them down to a new one.

#### auto-fit
auto-fit works almost identically to auto-fill. 

The only difference is that when the container's size exceeds the size of all the items combined:
- auto-fill keeps inserting empty rows or columns and pushes your items to the side, 
- auto-fit collapses those empty rows or columns and stretches your items to fit the size of the container.

Note
If your container can't fit all your items on one row, it will move them down to a new one.

##### auto-fill vs auto-fit example
<style>
  .item1a{background:LightSkyBlue;}
  .item2a{background:LightSalmon;}
  .item3a{background:PaleTurquoise;}
  .item4a{background:LightPink;}
  .item5a{background:PaleGreen;}
  
  .container1 {
    font-size: 40px;
    min-height: 100px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: repeat( auto-fill, minmax(60px, 1fr));
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
  
  .container2 {
    font-size: 40px;
    min-height: 100px;
    width: 100%;
    background: Silver;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
</style>
auto-fill

	grid-template-columns: repeat( auto-fill, minmax(60px, 1fr));

<div class="container1">
  <div class="item1a">1</div>
  <div class="item2a">2</div>
  <div class="item3a">3</div>
  <div class="item4a">4</div>
  <div class="item5a">5</div>
</div>
auto-fit

	grid-template-columns: repeat( auto-fit, minmax(60px, 1fr));

<div class="container2">
  <div class="item1a">1</div>
  <div class="item2a">2</div>
  <div class="item3a">3</div>
  <div class="item4a">4</div>
  <div class="item5a">5</div>
</div>

### minmax()
It's used to limit the size of items when the grid container changes size. To do this you need to specify the acceptable size range for your item. Here is an example:

	grid-template-columns: 100px minmax(50px, 200px);
	
In the code above grid-template-columns is set to create two columns:
- 1st is 100px wide
- second has the minimum width of 50px and the maximum width of 200px.

#### minmax() example

<style>
  .itemU{background:LightSkyBlue;}
  .itemV{background:LightSalmon;}
  .itemX{background:PaleTurquoise;}
  .itemY{background:LightPink;}
  .itemZ{background:PaleGreen;}
  
  .containerA {
    font-size: 40px;
    min-height: 300px;
    width: 240px;
    background: LightGray;
    display: grid;
    grid-template-columns: repeat(3, minmax(90px, 1fr));
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
  
  .containerB {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: repeat(3, minmax(90px, 1fr));
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
  }
</style>

	.containerA {
		...
		width: 240px;
		grid-template-columns: repeat(3, minmax(90px, 1fr));
		...
	}
  
<div class="containerA">
  <div class="itemU">1</div>
  <div class="itemV">2</div>
  <div class="itemX">3</div>
  <div class="itemY">4</div>
  <div class="itemZ">5</div>
</div>

	.containerB {
			...
			width: 100%;
			grid-template-columns: repeat(3, minmax(90px, 1fr));
			...
		}

<div class="containerB">
  <div class="itemU">1</div>
  <div class="itemV">2</div>
  <div class="itemX">3</div>
  <div class="itemY">4</div>
  <div class="itemZ">5</div>
</div>

## Demo

	.d1{background:LightSkyBlue;}
	.d2{background:LightSalmon;}
	.d3{background:PaleTurquoise;}
	.d4{background:LightPink;}
	.d5{background:PaleGreen;}

<style>
  .d1{background:LightSkyBlue;}
  .d2{background:LightSalmon;}
  .d3{background:PaleTurquoise;}
  .d4{background:LightPink;}
  .d5{background:PaleGreen;}
  
  .container {
    font-size: 40px;
    width: 100%;
    background: LightGray;
    display: grid;
	grid-template-columns: 100px 100px 100px; /* 3 columns each with a width of 100px */
	grid-template-rows: 50px 50px; /* 2 rows each with a height of 50px */
	grid-gap: 10px 20px; /* 1st val - gap between rows, 2nd val gap between columns */
  }
</style>

<div class="container">
  <div class="d1">1</div>
  <div class="d2">2</div>
  <div class="d3">3</div>
  <div class="d4">4</div>
  <div class="d5">5</div>
</div>

	.container {
		font-size: 40px;
		width: 100%;
		background: LightGray;
		display: grid;
		grid-template-columns: 100px 100px 100px; /* 3 columns each with a width of 100px */
		grid-template-rows: 50px 50px; /* 2 rows each with a height of 50px */
		grid-gap: 10px 20px; /* 1st val - gap between rows, 2nd val gap between columns */
	}