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

the initial time returned by getTime() is "00:00", and it starts there because the constructor initializes both hour and minute values to 0 by default.

22. Open an inspector for this object. With the inspector open, call the object’s methods. Watch the
displayString field in the inspector. Read the project comment (by double-clicking the text icon in the
class diagram) for more information.

the displayString matches the getTime() and the timeTick() goes up a minute until 59 the it goes up a hour and continues until 24hours then goes back to 00:00.

23. How many times would you need to call the timeTick method on a newly created ClockDisplay object to
make its time reach 01:00? How else could you make it display that time?

you would need to click it 60 times until you can get 01:00 on the displayclock.
a different way of doing it is to increment is and make it so that evbery time you clik the voidtimeTick() it goes straigt to 01:00 instead of going to 00:01 every click.

24. Write down the definition of a variable of type NumberDisplay called digit. Write an assignment
statement that creates a NumberDisplay object with a rollover limit of 10 and assigns the object to the
variable.

NumberDisplay digit;                 // variable definition
digit = new NumberDisplay(10);       // assignment
// (or) NumberDisplay digit = new NumberDisplay(10);

25. Write Java statements that define a variable named window of type Rectangle, and then create a
rectangle object and assign it to that variable. The rectangle constructor has two int parameters for the
lengths of its sides.

Rectangle window;            // define the variable
window = new Rectangle(40, 60);  // create and assign
// (or) Rectangle window = new Rectangle(40, 60);

26. Look at the second constructor in ClockDisplay’s source code. Explain what it does and how it does it.

it builds 2 couters and delegates to setTime(hour, minute), which validates, assigns, and calls updateDisplay().

27. Identify the similarities and differences between the two constructors. Why is there no call to
updateDisplay in the second constructor, for instance?

both create hours = new NumberDisplay(24) and minutes = new NumberDisplay(60).
the differences are that no-argument constructor initializes the clock to 00:00 and directly invokes updateDisplay().
In contrast, the constructor accepting hour and minute parameters sets the time using setTime(), which inherently includes a call to updateDisplay().
Consequently, the parameterized constructor does not explicitly call updateDisplay(), as this action is already performed by setTime().

28. Given a variable
Printer p1;
which currently holds a reference to a printer object, and two methods inside the Printer class with the
headers
public void print(String filename, boolean doubleSided)
public int getStatus(int delay)
write two possible calls to each of these methods.

"p1.getStatus"(0); and ""(100);

29. Open the house project from chapter 1 and review the Picture class. What types of object are created by
the constructor of Picture?

circles squares and triagles.

30. List all the external method calls that are made in the draw method of Picture on the Triangle object
called roof.

here are the method calls: new Triangle(), roof.changeSize(height, width), roof.moveHorizontal(...), roof.moveVertical(...), roof.changeColor(...), roof.makeVisible().

31. Does the Picture class contain any internal method calls?

draw() setColor().

32. What is the result of the expression (8 % 3)? In other words, what value remains when 8 is divided by 3?

2 remains.

33. Try out the expression (8 % 3) in the Code Pad. Try other numbers. What happens when you use the
modulo operator with negative numbers?

every time you insert a negative number it will always give you 0.

34. What are all possible results of the expression (n % 5), where n is an integer variable?

n can be or greater than 0 or smaller than 0 it depends on the sign of n.

35. What are all possible results of the expression (n % m), where n and m are integer variables?

for anything that is not zero m, all possible results are integers whose absolute value is less than |m|, and whose sign matches n (or zero).

36. Challenge exercise Change the clock from a 24-hour clock to a 12-hour clock. Be careful: This is not as
easy as it might at first seem. In a 12-hour clock, the hours after midnight and after noon are not shown
as 00:30, but as 12:30. Thus, the minute display shows values from 0 to 59, while the hour display shows
values from 1 to 12!



37. There are (at least) two ways in which you can make a 12-hour clock. One possibility is to just store hour
values from 1 to 12. On the other hand, you can simply leave the clock to work internally as a 24-hour
clock but change the display string of the clock display to show 4:23 or 4.23pm when the internal value
is 16:23. Implement both versions. Which option is easier? Which is better? Why?


