24.10.08  18.56
tags: [[web]] [[frontend]] [[js]]

# JQuery, JS Library
eg. 1. vanilla js vs JQuery.
`document.querySelector('h1')`
`$('h1')`

cdn should be placed above the local JS Script in the body of the html.

`// allows us to put the js cdn in the head section of html`
`$(document).ready(function() {} )`

### side note
minify -> getting rid of the spaces and comments to make JS or CSS smaller size and load faster.

eg. 2
`document.querySelector('h1')`
`$('h1')

`document.querySelectorAll('button')`
`$('button')`

`// returns the value`
`$('h1').css("font-size")`

`// sets the value.`
`$('h1').css('font-size', '16')`

## Behaviour
`$('h1').addClass('big-title');`
		`.removeClass('big-title);`

`// add multiple classes`
`.addClass('big-title margin50)`

`// returns true or false`
`$('h1').hasClass('margin50')`

`// change text`
`// applied to all buttons`
`$('button').text('bye')`

`// instead of innerHtml`
`$('button').html('<em> Hey </em>);

# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[JS Dom continued]]
[[JS Dom continued 2]]

