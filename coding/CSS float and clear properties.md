15.09.24
tags: [[css]] [[frontend]] [[web]] 

# CSS float and clear properties

## float
other properties wrap around 
`img {float: left;}` 

### best use case for float
![[Pasted image 20240915194931.png|300]]

## clear
if you don't want other element wrapping around the element with the property float,
set the property clear to it.
`img {float: left}`
`footer {clear: left}`
### it works but not recommended, use Grid or Flexbox instead
![[Pasted image 20240915202635.png|300]]

to clear both sides use `clear: both`


# Reference

[[The Complete 2023 Web Development Bootcamp]]
