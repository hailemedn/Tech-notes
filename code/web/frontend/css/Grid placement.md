17.09.24
tags: [[css]] [[frontend]] [[web]]

# Grid placement

## terms in CSS Grid
- Grid container
- Grid items
- tracks ->  row, columns
- intersections of tracks -> cells
- lines separating tracks -> grid lines , gap(has got height, width)

`.container {`
	`height:100vh`
	`display:grid;`
	`gap: 3rem;    // track separating lines thickness`
	`grid-template-columns: 1fr 1fr 1fr;   // creating tracks`
	`grid-template-rows: 1fr 1fr;`
`}`

`.item {`
	`grid-column: span 2;   //sets the column span for this item`
	
	grid-column-start: 2;
	grid-column-end: 4;

	//   grid row start / grid column start / grid row end / grid column end
	// the numbers are line numbers , you can see them in dev tools
	grid-area: 2 / 1 / 3 / 3      // short hand for the above

	// pushes the items to the end
	order: 1    // by default all have order 0

	// places it infront of every item in the container
	order: -1;
`}`


### Grid allows overlay over other items by setting grid-area.

`grid-column: 2 / 4     // grid-column-start / grid-column-end`

`// end after three lines, span doesn't work with negative values
`grid-column: 2 / span 3`

### you can use negative values with grid-column/row properties to target the other end.

## side-note
`#E5836580   //RGBalpha(transparency)


# Reference

[[The Complete 2023 Web Development Bootcamp]]
