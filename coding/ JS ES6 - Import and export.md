
24.12.14  21.44  
tags:[[react]] [[web]] [[frontend]] [[js]]


#  JS ES6 - Import and export
- enable us to separate our code and use them, making our code more readable.

## how to use
math.js
```js
const pi = 3.16
export default pi;
```
if pi was a function we don't put pi().

```js
function pi() {
	return 3.16
}

export default pi;

```


app.js
```js
import PI from "./math"
```
we don't have to add the extension.

### to export more than one variable or function.
math.js
```js
const pi = 3.16

function doublePi() {
	return pi * 2
}

function triplePi() {
	return pi * 3
}

export default pi;
export { doublePi, triplePi }; 
```

app.js
```js
import PI from './math';
import { doublePi, triplePi } from './math'
```

the name doesn't matter for the default export, but it does for the rest. 

the order in which you export them don't matter, just get the names right.

we can also write the above code as
```js
import PI, { triplePi, doublePi } from "./math.js";

```

## wild card
using the above math.js

app.js

```js
import * as PI from "./math.js"

// usage
console.log(PI.default) 
console.log(PI.doublePi())
console.log(PI.triplePi())
```

# Reference
[[The Complete 2023 Web Development Bootcamp]]
