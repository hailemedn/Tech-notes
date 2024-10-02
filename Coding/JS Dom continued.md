09.28.24
tags: [[frontend]] [[web]] [[js]]

# JS Dom continued

`// returns array of all li elements`
`document.getElementsByTagName('li')`

`document.getElementsByTagName('li')[0].style.color = 'purple'`

`// returns array even if there is one item.`
`document.getElementsByClassName("btn")`

`// returns only one element because id should be unique.`
`document.getElementById('')`
`document.getElementById('title').innerHTML = "GoodBye"`

`// similar to css identifiers`
`// personal favorite way to target an element`
`document.querySelector()`
`document.querySelector(#title)`
`document.querySelector(.btn)`

`// can combine selectors`
`document.querySelector('li a')`
`document.querySelector('li.item')


`<ul id='list'>`
	`<li class = 'item'>`
	`<li class = 'item'>
	`<li class = 'item'>
`</ul>`
`// returns only the 1st item, even tho it matches all 3 children`
`document.querySelector(#list.item);`
`// returns array of all elements with a className item. 
`document.querySelectorAll(#list.item)`
`// to select a specific item`
`document.querySelectorAll(#list.item)[2]`

## Which should we use
- get element or query selector
- can use both
- query selector and query selector all allow for more complex query's and are widely used.
# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Coding/Intermediate JS|Intermediate JS]]
[[Coding/JS Dom Manipulation|JS Dom Manipulation]]
[[Coding/Document Object Model|Document Object Model]]