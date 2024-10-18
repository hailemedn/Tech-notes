24.10.18  18.45
tags: [[web]] [[backend]] [[security]] [[nodejs]]

# Level two authentication

- here we add encryption to our [[Level one authentication]] password.
- encryption is scrambling our message/text/password with a particular way that only a person with key unscramble and see it.
- some notable mentions
	- Caesar cipher, AES
- with new tech Caesar cipher is easy to crack, while AES algorithm will be touch to crack.
- here we will use mongoose-encryption package to encrypt our password.
- one thing to note here is we have to set `userSchema` with the recommended way

`const userSchema = new mongoose.Schema ({`
	`email: String,`
	`password: String,`
`});`

`// we should keep this in .env file` [[using environment variables]]    
`const secret = 'thisisourlittlesecret'`

`// use encyptedFields to specify values to encypt  `
`// otherwise it will encrypt the entire document.  `
`userSchema.plugin(encrypt, {secret: secret, encryptedFields:['password']});  `
`const User = mongoose.model("User", userSchema);`

- when we register or login, it will automatically encrypt and decrypt our password.

### more on mongoose-encyption
https://www.npmjs.com/package/mongoose-encryption
### mongoose plugins
https://mongoosejs.com/docs/plugins.html



# Reference

[[The Complete 2023 Web Development Bootcamp]]
[[Authentication & Security]] 