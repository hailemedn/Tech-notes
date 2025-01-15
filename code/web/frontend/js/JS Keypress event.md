241008
tags: [[web]] [[frontend]] [[js]] 

# JS Keypress event

`// function(event) {}`
`// callback function -> waits until an event happens to trigger.`
`document.addEventListener('keypress', function(event) { makeSound(event.key)})`

eg. 1
`// whenever a key is pressed, e captures information about the keypress`
`// the type, the key etc.`
`document.addEventListener('keypress', function(e){ console.log(e)} )`

## side note
instead of keypress, we should use keydown.



# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Advanced JS and Dom manipulation]] 