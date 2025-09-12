Project: clock-display
Authors: David Barnes and Michael Kölling

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling

It is discussed in chapter 3.

To use this project, create an instance of class ClockDisplay. Then inspect this 
instance and leave the object inspector window open. With the inspector window open, 
call the object's methods, such as timeTick and setTime. Watch the 
"displayString" in the inspector.

The displayString field simulates the actual clock display device. Were this 
program running in a real clock, it would change the real, physical display 
hardware instead of this string. The timeTick method would be triggered once 
every minute by some timer hardware.

Everything else could be pretty much the same.


Note: This project does not implement adequate handling of errors.

Part II: clock-display project

21. Open the clock-display project and create a ClockDisplay object by selecting the following constructor:
new ClockDisplay()
Call its getTime method to find out the initial time the clock has been set to.
Can you work out why it starts at that particular time?

it starts at this particulas time because the private int limit i 24 because of their being 24 hours in a day so it goes up by 1 minute.******

22. Open an inspector for this object. With the inspector open, call the object’s methods. Watch the
displayString field in the inspector. Read the project comment (by double-clicking the text icon in the
class diagram) for more information.



