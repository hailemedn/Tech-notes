25.01.01  04.42  
tags: [[react]] [[web]] [[frontend]] [[js]]


# Destructuring

```js
const rgb = [12, 165, 79];

const cars = {
	model: "E3",
	color: "black",
}
```

inorder to grab the red, we use `rgb[0]`  
but this can get hard to read and tricky if we got a large lines of code.

we can use destructuring to map each item to a variable.


For the array, the names of the vars, don't matter, you can call it whatever you want.
```js
const [red, green, blue] = [12, 165, 79];
```

When you destructure an object the var names have to match the key.

```js
const { model, color } = cars
```

## nested objects/arrays destructuring.
```js
const cars = [
  {
    model: "Honda Civic",
    //The top colour refers to the first item in the array below:
    //i.e. hondaTopColour = "black"
    coloursByPopularity: ["black", "silver"],
    speedStats: {
      topSpeed: 140,
      zeroToSixty: 8.5,
    },
  },
  {
    model: "Tesla Model 3",
    coloursByPopularity: ["red", "white"],
    speedStats: {
      topSpeed: 150,
      zeroToSixty: 3.2,
    },
  },
];
```

destructure honda and tesla
```js
const [ honda, tesla ] = cars
```

accessing the first from the nested array colorsByPopularity and topSpeed from speedStats.

```js
// hondaTopColor returns "black".
// topSpeed returns 140.
const { colorsByPopularity: [ hondaTopColor ] } = honda;  
const { speedStats : { topSpeed } } = honda;


// combined
const { colorsByPopularity : [ hondaTopColor ], speedStats : { topSpeed } } = honda

```

if we want to change the name that is similar to a key when destructuring objects we can use the code below.

```js
//hondaTopSpeed returns 140, similar to the above
const { speedStats : { topSpeed: hondaTopSpeed }} = honda;
```


## default values.
sometimes when interacting with api's, they might have some missed data. in those cases we can use default values.

```jsx
const animals = [
	{
		name: "garfield",
		sound: "meow"
	},
	{
		sound: "bark"
	}
];

const [cat, dog] = animals;

// if we print name and sound we get airbud, and bark
// bark bc it was already defined, if it wasn't it will use the default value
const { name = "airbud", sound = "woof woof"} = dog; 

```



# Reference
[[The Complete 2023 Web Development Bootcamp]]
