
Mon 8.5.2024 

Tags: [[mobile-dev]] [[android-dev]] [[programming]] 

# Hello world

## choosing company domain when setting up project

- we want to choose a domain that we own, so that it is unique, because it helps to identify the application from countless others on the Playstore and on the phone.
- Then the package name is set automatically by reversing the domain

## Choosing minimum SDK (Android version)

- there is a tradeoff here, 
	- we want to make sure most devices support our application.
	- But we also need to make sure that the android version supports the feature we are looking to implement.
- There is a help me choose button at the bottom to see more about the amount of active users each API version distribution/ android platform has and additional information.

## After finishing configuring

- after all the loading is done, I couldn't find the layout folder and file, so i had to create it, in the previous versions, it will let you name and setup the layout folder and file but no longer.
- So inside android/app/res/   path create  layout/activity_main.xml
- in full android/app/res/layout/activity_main.xml
- it also let's you choose Activity name: (MainActivity in this case), which i might have to create later I'm not sure we will get back to it when we have the answer.

# References

https://learn.udacity.com/nanodegrees/nd940-gc-251/parts/bf8d0df3-0dca-4bf7-a317-d4e066fa069a/lessons/ls2257/concepts/53e09954-aed6-4db2-9eb4-b1d1b1cb1bff