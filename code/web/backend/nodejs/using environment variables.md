24.10.18  20.05
tags: [[web]] [[backend]] [[nodejs]]

# using environment variables
- when setting up any project and before you push code to remote like github it's important to setup .env file and gitignore.
## why
- bc we don't want to push our little piece of secret information into a public repository like github which will become visible and searchable.
### prime example
- https://www.theregister.com/2015/01/06/dev_blunder_shows_github_crawling_with_keyslurping_bots/
- https://vertis.io/2013/12/16/unauthorised-litecoin-mining/

## how to use
- install package
- create .env file
- add secrets/keys in there
	- `SECRETS=thisismysecret`
	- the var is in capital and snake case
		- `MY_SECRET=thesecret`
- use the keys in your JS
	- `process.env.SECRETS`
- create .gitignore file and include names of files that shouldn't be pushed to remote like node modules and .env file
- recommended files names to include in .gitignore
	- https://github.com/github/gitignore/blob/main/Node.gitignore
- you're done, next time you push your code to remote files like .env and node_modules won't be uploaded and your secret will be kept safe

## deployment
- when deploying the website platforms will enable you to input environment variable so that the website works properly while keeping your keys hidden.

## cloning without node_modules 
- when you later clone projects from repository inorder to use your dependencies just run the command `npm install` and all the project dependencies will be installed.



# Reference
[[The Complete 2023 Web Development Bootcamp]]
[[Level two authentication]]
