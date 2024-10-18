24.10.18  22.32
tags: [[web]] [[backend]] [[security]]

# Level three authentication
- with [[Level two authentication]] it's easy to decipher a password if you get the key/secret variable in level two authentication
- with hashing it removes the key from the process.
- a hash function produces a cipher key that's almost impossible to reverse to the plain text, even if it was possible it would take a very long time, not worth any hackers time.
- one example is md5,
- code `password: md5(req.body.password)`

- but hashing also has it's own cons.



# Reference
[[The Complete 2023 Web Development Bootcamp]]
[[Authentication & Security]]
