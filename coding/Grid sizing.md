17.09.24
tags: [[css]] [[frontend]] [[web]]

# Grid sizing

assume all codes are inside `.container {}`

	diplay: grid;
	
	// fixed, unresponsive
	grid-template-rows: 100px 200px;
	grid-template-columns: 400px 800px;
	
	// combined shorthand of the above
	grid-template: 100px 200px / 400px 800px

	// auto takes the remaining available space as width
	grid-template-column: 100px auto; // 100%

	// auto will fit the height to the content
	grid-template-rows: 100px auto; // fit content


## fractional unit (fr)
Defines the ratio for rows/columns size

## min-max

	// in small spaces | 100 |  200   |
	// in larger spaces | 100 |    400     |
	grid-template-columns: 100px minmax(200px,400px)


## repeat
`grid-template-columns: repeat(2, 200px)    //same us :200px 200px`  


### what happens if we don't set enough rows and column?
Keeps the width size provided in grid-template-column and it fits the height of the content, if you add a fifth element like in the eg. below

`grid-template-columns: repeat(2, 200px);`
`grid-teplate-rows: repeat(2, 200px);`

`// any items outside of the provided row will be set to this size.`
`grid-auto-rows: 300px `


![[Pasted image 20240917213614.png|200]]


## placement
from left to right and from top to bottom
### 2x4
`display:grid;
`grid-template-rows: repeat(2, 200px);
`grid-template-column: repeat(4, 200px);`

![[Pasted image 20240917215915.png|300]]



# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[CSS Grid|CSS Grid]] 