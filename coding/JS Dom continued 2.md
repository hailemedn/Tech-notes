10.02.24
tags: [[frontend]] [[web]] [[js]]

# JS Dom continued 2.


## JS Dom adding class to add properties
`document.querySelector("button").classList;  //<button class="btn">`

`//button class="btn invisible">
`document.querySelector("button").classList.add("invisible")  

`.remove('invisible')`

`// add or remove depending on if it has the class or not`
`.toggle('invisible')`


`// modifies all text including the html inside the h1 tag.`
`document.querySelector("h1").innerHTML = ""`

`// capture and modify only the text element.`
`document.querySelector('h1').textContent = ""`

## Change attributes value
`// returns all attributes related with a tag.`
`document.querySelector('a').attributes`

`// returns the value assigned to href attribute`
`document.querySelector('a').getAttribute('href')`

`// changes the href attribute.`
`document.querySelector('a').setAttribute('href', 'www.ggoel.com')




# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Intermediate JS|Intermediate JS]]
[[JS Dom Manipulation|JS Dom Manipulation]]
[[Document Object Model|Document Object Model]]
