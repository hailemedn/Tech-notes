24.12.21  18.56  
tags: [[react]] [[web]] [[frontend]] [[js]]


# Javascript ES6 arrow functions

```js
var numbers = [3, 56, 2, 48, 5];
```

Arrow function cuts down code to make a function;
```js
function add(a, b) {
	return a + b;
}

// arrow function
const add = (a, b) => a + b
```

we don't need a parenthesis is we only have one parameter  
additionally we don't need return or brackets if we only have 1 expression.
```js
	/*numbers.map(function (num) {
		return num * 2
	}) */
	
	numbers.map( num => num * 2 )
```

it's a good practice to add parenthesis to one expression if it has more than one attribute.

```js
{emojipedia.map( emojiTerm => (
          <Entry
            key={emojiTerm.id}
            emoji={emojiTerm.emoji}
            name={emojiTerm.name}
            description={emojiTerm.meaning}
          />
        ))}
```


# Reference
[[The Complete 2023 Web Development Bootcamp]]
