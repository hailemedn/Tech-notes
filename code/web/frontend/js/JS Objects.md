241007
tags: [[web]] [[frontend]] [[js]]

# JS Objects

eg. 1
`var keeper1 = {
	`name: 'molita',
	`gender: 'female' }`
	
`var keeper2 = {
	`name: 'Solina',
	`gender: 'male' }`

Instead create constructor function (factory for keepers).
`// Keepers is capitalized`
`function Keepers (name, gender) {
	`this.name = name;`
	`this.gender = gender;`
	`this.moveSuitCase = function () { alert("I'm picking up ur suitcase.");`
`}`

once we create a constructor we don't need to implement eg. 1.
Instead we use
`var keeper1 = new Keepers("molita", "female");`
`var keeper2 = new Keepers("Solina", "male");`

`keeper1.name   // molita`

## Methods
functions associated with an object.
to execute use paranthesis.
`keeper1.moveSuitCase()`





# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Advanced JS and Dom manipulation]]