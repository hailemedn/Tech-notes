241006
tags: [[programming-tips]] [[error]] [[github]] [[web]] 

# adding github remote access using the terminal

## error 
when ever i tried to push a code to github, it would ask me to input github username and password. 

## tried
entering a password won't work

## works but not the best solution
instead of the password, if you input a token you generated from github, it will push your code to github. 

the problem is it will ask you for username and password again, when you try to push again.

### where to generate token
you generate a token by heading to settings and developer options and it's straight forward from there. try to limit the permissions.

## what worked
when adding a remote using `git remote add orgin`  add the token infront of url, like this
`git remote add origin https://<token>@github.com/hailemedn/haile-valut.git

now when you try to push the code it won't ask for github username and password.

## resources used
Gemini

# Reference

