24.12.14  20.27  
tags:[[react]] [[web]] [[frontend]] [[js]]


# React components
- A long page of code can be hard to read and understand.
- components allows us to split a large web structure into smaller parts, when displayed on a page is easier to read and understand.
- another use is we can reuse these components.
- it also enables us to spot problems easily if there are any.
- naming convention for components is Pascal case (first letter of a word is capitalized.) for both component file name and the function.

Header.jsx
```js
function Header() {
	return <h1>Header text</h1>
}
```

app.js
```js
function App() {
	return (
		<Header />
	)
}
```

# Reference
[[The Complete 2023 Web Development Bootcamp]]
