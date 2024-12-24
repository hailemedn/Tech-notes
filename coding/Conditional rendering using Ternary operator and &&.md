24.12.24  01.20  
tags: [[react]] [[web]] [[frontend]] [[js]]


# Conditional rendering using Ternary operator and &&
## problem
we can't use a statement inside html in jsx to conditionally render stuff. below code throws an error.
```jsx
return (
	<div>
		{
			if (isLoggedIn) {
			    return <h1>Hello</h1>;
			  } else {
			    return <Login />;
			  }
		}
	</div>
)
```

## Ternary operator
we can use a ternary operator to fix this problem

```jsx
condition ? do if true : do if false
```

```jsx
return(
	<div>
		isLoggedIn ? <h1>Hello</h1> : <Login />
	</div>
)
```

## &&
in logic while using && for a condition to resolve to true both expressions have to be true.

in JavaScript if the first expression returns false. it won't calculate the rest.

```jsx
condition && expression // the second won't be resolved.
	false     true/false
```

react leverages this to simplify some code.   

using ternary
```jsx
currentTime > 18 ? <h1>night time baby</h1> : null ;
```

using &&

```jsx
currentTime > 18 && <h1>night time baby</h1>
```

explanation if the first condition returns true, the second part will be executed.

if false, it won't execute.

# Reference

[[The Complete 2023 Web Development Bootcamp]]