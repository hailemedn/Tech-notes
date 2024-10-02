04.09.24
tags: [[programming]] [[android-dev]] [[kotlin]]


dividing an int with int gives you an int
1/2 = 0  
1.0/2.0 = 0.5

you can call objects on numbers.
var fish = 2
fish.times(2)   //fish = 4


just like python i don't have to put semi colon at the end of every line.
val and var are used to declare variables 
val: you can't reassign a value - unchangeable
you can reassign with var. - changeable

datatype in inferred. that means you don't have to put a datatype when declaring a variable.
var number = 1;

you can't reassign a variable with another datatype once it's inferred. 

Number types won't implicitly convert to other types, so you can't assign a short value to a long variable or a byte to an int.

val b: Byte = 1
val i: Int = b   //throws an error.

  
but you can always assign them by casting
val i: Int = b.toInt()

When you declare a variables type explicitly, By default it's value can't be null
var rocks : Int = null //error

use ? to indicate that a variable can be null
var rocks: Int? = null

you can allow for a list to be null
var lotsOfFish : List \<String?>  = listOf(null, null)
var everMoreFish : List \<String>? = null
var definitelyFish : List \<String>? = null

if the list is not null, the elements can't be null


### Reference

https://learn.udacity.com/nanodegrees/nd940-gc-251/parts/634581f8-3a85-423b-9945-e5729bf0dc28/lessons/fc002016-7ebe-4980-a4cb-419f8e7cb979/concepts/82da4dff-ca6f-4823-a83a-264ce042be4c?lesson_tab=lesson