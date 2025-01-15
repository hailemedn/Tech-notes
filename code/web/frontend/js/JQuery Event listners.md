24.10.08  20.12
tags: [[web]] [[frontend]] [[js]]

# JQuery Event listners

`$("h1").click(function() {
	`$("h1").css("color", "purple")`
`})`

`$("button").keypress( function(e) {
	`console.log(e.key)`
`} )`

`$("h1").on("mouseover", function() {
	`$("h1").css("color", "yellow")`;
`})`

`// adds element before h1 element`
`$("h1").before("<button> new </button>");`

`.after()`

`// adds before content inside the element`
`.prepend()`

`// adds after content inside the element`
`.append()`

`// removes all`
`.remove()`


`$("h1").hide()  // remove from flow`
`.show()`
`.toggle()    // hide/show`
`.fadeOut()`
`.fadeIn()`
`.fadeToggle()`
`.slideUp()`
`.slideDown()`
`.slideToggle()`

`// stick to numeric values like margin and padding.`
`// eg. color: red; won't work`
`$("h1").animate({ opacity: 0.5; })  // "20%" also allowed`

## Chaining
`$("h1").slideUp().slideDown().animate({ opacity: 0.5; })`


# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[JS Dom Manipulation]]
[[JS Dom continued]]
[[JS Dom continued 2]]
[[JQuery, JS Library]]
