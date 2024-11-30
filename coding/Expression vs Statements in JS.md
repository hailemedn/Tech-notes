24.11.30  02.59  
tags:[[js]] [[react]]


# Expression vs Statements in JS
## Expression
a code that resolves to or becomes a value
```js
var x = 5;
var y = getAnswer();
```

- so in the above code, the entire variable declaration process is a statement, because it's an instruction.
- but x and y are expressions because they resolve to a value.

## Statements
these are instructions or codes that perform an action
- conditional statements
- loops


### in react inside curly braces we can only insert expressions.
```js
var fName = "haile";
var lName = "ramos";
const luckyNum = 7;

ReactDOM.render(
  <div>
    <h1>
      Hello {fName} {lName}
    </h1>
    <ul>
      <li>rice</li>
      <li>potatos</li>
      <li>eggs</li>
    </ul>
  </div>,
  document.getElementById("root")
```

# Reference
- [[The Complete 2023 Web Development Bootcamp]]
- https://www.youtube.com/watch?v=WVyCrI1cHi8&list=PL-xu4i_QDSxcoDNeh8rx5-pHCCTOg0XsI
- [[React Intro]]

