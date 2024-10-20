24.10.19  21.34  
tags:[[web]] [[backend]] [[security]]

# Level four authentication - salting and hashing passwords with bcrypt

## salting
- refers to adding extra random generated characters to an already hashed password and hashing it again.
- this will make the password more complex and almost impossible to create a hash table  [[Hacking 101]] .

## Salting rounds
- amount of time the salting process happens
- in each round salting is done with the same random characters generated in the first round.
- for example if the salting round is 10. the salting is done 10 times which will make the password complex and hard to create hash tables.
password: qwerty  
salt: 1234jljd  
password that goes into hash function: qwerty1234jljd  
hash generated: generatedhash

2nd round salting: generatedhash1234jljd

## usage
const bcrypt = require("bcrypt")

const saltRounds = 10;


### to hash a password
`app.post("/register", async (req, res) => {`  
	
	`// generate the hash`  
	`const hash = await bcrypt.hash(req.body.password, saltRounds);  `
	`const newUser = new User({  `
		`email: req.body.username,  `
		`password: hash,  `
	`});`  
	`await newUser.save();`  
	`res.render("secrets")  `
`});  `


### to check a password
`app.post("/login", async (req, res) => {   `
	`const username = req.body.username; `
	`const password = req.body.password; `  
	`const foundUser = await User.findOne({ email: username });  `
	`if (foundUser) {  `

		`// compare the password`  
		`const match = bcrypt.compare(password, foundUser.password)`  
		`if(match) {  `
		`res.render("secrets")  `
		`} else {`
		`res.send("wrong password")  `
		`}`
	`} else {  `
		`res.send("Can't find the user.")  `
		`console.log();  `
	`}  `
`})`  



# Reference
[[The Complete 2023 Web Development Bootcamp]]  
[[Authentication & Security]]  
