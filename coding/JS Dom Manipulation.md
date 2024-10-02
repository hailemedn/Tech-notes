09.28.24
tags: [[frontend]] [[web]] [[js]]

# JS Dom Manipulation

## JavaScript
### Inline
- not modular
- not easy to debug
- not good practice
` <body onload = "alert('Hello');"> </body>`

### Internal
`<body>`
`<script type = "text/javascript"> alert("Hello") </script>`
`</body>`

### External
`<body>`
	`<h1></h1>`
	`<p></p>`
	`<script src = "index.js" charset="utf-8"> </script>`
`</body>`

where we place the script tag matters.
Best practice is to put it at the end inside of the body tag.



# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Intermediate JS|Intermediate JS]]