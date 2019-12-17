[UP](../index.md)

[Cheat Sheet](./flexcc.md)

# Flex Container

## display: flex
Adding `display: flex` to an element turns it into a flex container. This makes it possible to align any children of that element into rows or columns

By **default value for the flex box will display elements in a row**.

## flex-direction
You do this by adding the `flex-direction` property to the parent item and setting it to `row` or `column`.  

Creating a:
- **row** will align the children horizontally
- **column** will align the children vertically.

## [Collective Alignment](./coll-align.md)

## flex-wrap
CSS flexbox has a feature to split a flex item into multiple rows (or columns). By default, a flex container will fit all flex items together. For example, a row will all be on one line.  

However, using the `flex-wrap` property, it tells CSS to wrap items. This means extra items move into a new row or column. The break point of where the wrapping happens depends on the size of the items and the size of the container.  

CSS also has options for the direction of the wrap:
- **nowrap**: this is the default setting, and does not wrap items.
- **wrap**: wraps items from left-to-right if they are in a row, or top-to-bottom if they are in a column.
- **wrap-reverse**: wraps items from bottom-to-top if they are in a row, or right-to-left if they are in a column.

# Flex items
There are several useful properties for the flex items.

## flex-shrink
When it's used, it **allows an item to shrink if the flex container is too small**.  

Items shrink when the width of the parent container is smaller than the combined widths of all the flex items within it.  

The `flex-shrink` property **takes numbers as values**. The **higher the number, the more it will shrink compared to the other items** in the container. For example: 

- if one item has a flex-shrink value of 1 and the other has a flex-shrink value of 3, 
- the one with the value of 3 will shrink three times as much as the other.

## flex-grow
The **opposite of flex-shrink**.  
Recall that `flex-shrink` controls the size of the items when the container shrinks.  

The `flex-grow` property **controls the size of items when the parent container expands**

## flex-basis
**specifies the initial size of the item before CSS makes adjustments** with flex-shrink or flex-grow.  

The units used by the flex-basis property are the same as other size properties (px, em, %, etc.). The value auto sizes items based on the content.

### flex 
**shorthand for flex-grow, flex-shrink, and flex-basis.**

For example:  

	flex: 1 0 10px; 

Will set the item to flex-grow: 1;, flex-shrink: 0;, and flex-basis: 10px;.  

The default property settings are `flex: 0 1 auto;`.

## order
Used to tell CSS **the order of how flex items appear in the flex container**.  

**By default, items will appear in the same order they come in the source HTML**. The property takes numbers as values, and negative numbers can be used.

## [Individual Alignment](./ind-align.md)
