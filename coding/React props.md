24.12.17  05.02  
tags: [[react]] [[web]] [[frontend]] [[js]]


# React props
allows us to send data to a component

## usage

app.jsx
```jsx
<>
	<Card name="ramos" age="26"/>
</>
```

Card.jsx
```jsx
function Card(props) {
	console.log(props); // returns an object
	console.log(props.name); // ramos
	console.log(props.age); // 26

	// inside jsx
	return <h1>{props.name}</h1>
}
```



# Reference
[[The Complete 2023 Web Development Bootcamp]]
