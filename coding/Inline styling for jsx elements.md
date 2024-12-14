24.12.14  17.05  
tags:[[react]] [[web]] [[frontend]] [[js]]


# Inline styling for jsx elements
- when ever we want to inject a JavaScript code into an html element in jsx, we have to use a set of curly braces.
```jsx
<h1 style={ }>Hello world</h1>
```

## Inline styling
- the style prop takes a JavaScript object so the code might look weird
```jsx
<h1 style={{color: red}}>Hello world</h1>
```

similar to below code.
```jsx
const customStyle = {
	color: "red",
	fontSize: "14",
	border: "1px solid black"
}
<h1 style={customStyle}></h1>
```

notice the number value for fontSize is in quotes. all values in the object needs to be inside quotes.

## why would we want to use inline styling?
- it enables us to change the styling, based on conditions or other circumstances.
- using the above code we can change the color.
```js
customStyle.color = "blue"
```

# Reference
[[The Complete 2023 Web Development Bootcamp]]
