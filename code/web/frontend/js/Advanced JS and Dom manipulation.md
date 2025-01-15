241007
tags: [[frontend]] [[web]] [[js]]

# Advanced JS and Dom manipulation

`// Event listener`  
`// addEventListner(event, function)`  
`document.querySelector('button').addEventListner('click', handleClick)`  

`function handleClick() {  
	`alert('I got clicked');`  
`}`  

## using methods with parenthesis and without parenthesis.

`// method call`  
`// will run regardless of if the event happens or not`  
`handleClick()`  

`// a function passed to be later called.`  
`// runs only when the event happens`  
`// reason why we used it in the above example`  
`handleClick`  

## Anonymous functions
`document.querySelector('button').addEventListener('click',   
	`function() { alert('I clicked it') }; )`  

### side note
- In the browser console  
`// shows us the steps taken to execute`  
`debugger;`  
`calculator(2, 3, add);`  

## Higher order functions
functions that takes other functions as input.


# Reference

[[The Complete 2023 Web Development Bootcamp]]
