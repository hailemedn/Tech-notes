04.09.24
tags: [[kotlin]] [[android-dev]] [[programming]] 

variables declared with val can't be reassigned, but we can manipulate the elements of the variable

val elem = ["one", "two", "three"]
elem = ["four", "five", "six"]  //error;
elem.remove("four")  //👍



### Reference

https://learn.udacity.com/nanodegrees/nd940-gc-251/parts/634581f8-3a85-423b-9945-e5729bf0dc28/lessons/fc002016-7ebe-4980-a4cb-419f8e7cb979/concepts/9c8de356-5e68-4e96-b8e6-a11ce2bca67f?_gl=1*1l7wrfv*_gcl_au*Mjk0ODAyMDYyLjE3MjUwMzU5OTA.*_ga*MTI0NjgwNjk2NC4xNzA0NzUyODA5*_ga_CF22GKVCFK*MTcyNTQxMTAxNC41LjAuMTcyNTQxMTAxNC42MC4wLjA.&lesson_tab=lesson