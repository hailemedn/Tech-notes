15.09.24
tags: [[css]] [[frontend]] [[web]]

# CSS Flexbox

`.container {`

	//makes it a block element
	//removes the display property of containers children
	display: flex;

	//takes as much space as it needs and allows inline elements to take          //spot in the line
	display: inline-flex  
`}`

## flex-direction
default is set to row.
### `flex-direction: row;`
- main axis = x-axis
- cross axis = y-axis

### `flex-direction: column;`
- the reverse of above

## flex-basis
Changes the height and width of children based on the main axis
`flex-basis: 100px`

## flexible layout

### order
`//applied to children`
`.children {`
	`order: 0        //default for all children elements`
	`order: 1       //if applied to one of the children, that element will be                       pushed to the end`
`}`

### flex-wrap
`applied to parent/container`
`.container {
	//default value - if there's no space, elements are pushed off screen
	flex-wrap: no-wrap;
	
	//if there's no space, elements wrap to the next line.
	flex-wrap: wrap	
	
	//wraps from bottom to the upper line
	flex-wrap: wrap-reverse
}`

### justify-content
`applied to parent/container`
`justifies contents along the main axis`
`.container {
	`justify-content: flex-start         //to the left
	`justify-content: flex-end        //to the right
	`justify-content: center         //center
	`justify-content: space-between         //distribute gaps on elements
	`justify-content: space-around         //
	`justify-content: space-evenly         //
	
}`


### align-items
works only when `flex-wrap: wrap;` is set.
sets distribution along the cross axis.

`.container {
	`flex-wrap: wrap`
	`align-items:           // values similar to justify-content`
}

`.child {
	`align-self:           // values similar, separate it from the group and                            set it's own distribution`
	`align-content         //`
}`

## flex sizing

content width/height < width/height < flex-basis < max/min-width/height 

### grow & shrink
`flex-grow: 1         // grow to the max-width`
`flex-shrink: 1       // shrink to the min-width`

`.child {
		
	`flex-basis: 0  // keeps everything equal, width/height
	`flex-grow: 1`
	`flex-shrink: 1`

	 `flex: 1 1 0   //grow, shrink and basis respectively`
	 `flex: 1       //commonly used`
}`



# Reference

[[The Complete 2023 Web Development Bootcamp]] 