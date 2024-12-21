24.12.20  19.37  
tags: [[react]] [[web]] [[frontend]] [[js]]


# Javascript ES6 Map,Filter,Reduce

```js
var numbers = [3, 56, 2, 48, 5];
```

## map
returns new array by doing something to each item in an array
```js
// newMappedNumbers outputs [6, 112, 4, 96, 10]
const newMappedNumbers = numbers.map(function(item) {
	return item * 2;
})
```

## filter
returns new array of items which returns to true;
```js
// returns [56, 48]
const newFilteredNumbers = numbers.filter(function (item) {
  return item > 10;
});
```

## reduce
accumulate a value by doing something to each item in an array.
```js
// returns 114.
const newReducedNumbers = numbers.reduce(function (accumulator, item) {
  return accumulator + item;
});
```

## find
finds the first number that matches from an array.
```js
//returns 56
const newFoundNumber = numbers.find(function (item) {
  return item > 10;
});
```

## findIndex
returns the index of the first number that matches from an array.
```js
const newFoundNumberIndex = numbers.findIndex(function (item) {
  return item >  10;
});
```
# Reference
[[The Complete 2023 Web Development Bootcamp]]
