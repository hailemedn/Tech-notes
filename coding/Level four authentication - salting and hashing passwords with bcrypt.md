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



# Reference
[[The Complete 2023 Web Development Bootcamp]]  
[[Authentication & Security]]  
