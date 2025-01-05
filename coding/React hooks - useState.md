25.01.01  04.13  
tags: [[react]] [[web]] [[frontend]] [[js]]


# React hooks
## problem
we are trying to increment a number and display it on the UI, when a button is clicked
![[Pasted image 20250101041451.png||200]]

normally how would approach this is using this code.
```jsx
var count = 0;

function increase() {
  count++;
  console.log(count)
}

ReactDOM.render(
  <div className="container">
    <h1>{count}</h1>
    <button onClick={increase}>+</button>
  </div>,
  document.getElementById("root")
);
```

this code will increment our count, but it won't be displayed.  
if we see the logs, it's incrementing by one each time, but on our UI it will still be 0. why bc our react dom is not re-rendering.

to re-render our UI, we can use something repetitive like the below code.

```jsx
var count = 0;

function increase() {
  count++;
  ReactDOM.render(
    <div className="container">
      <h1>{count}</h1>
      <button onClick={increase}>+</button>
    </div>,
    document.getElementById("root")
  );
}

ReactDOM.render(
  <div className="container">
    <h1>{count}</h1>
    <button onClick={increase}>+</button>
  </div>,
  document.getElementById("root")
);
```

using useState hook we can simplify our solution.
- one rule of hooks is they can only be used inside a functional component.

```jsx
function App() {
	const [count, setCount] = useState(0); // 0 is the initial value representing var count = 0 in the above code.

	function increase() {
		setCount(count++);
	}

	return (
		<div className="container">
		    <h1>{count}</h1>
		    <button onClick={increase}>+</button>
		</div>
	)
}
```






# Reference
[[The Complete 2023 Web Development Bootcamp]]
[[Destructuring]]
