## Debugging Homework

### 1. What is the purpose of a breakpoint?

A **_breakpoint_** is a marker in the code where the program will stop running. You insert it by clicking in front of the line after the line number. It stops the code from running any further.

This way you can check what is happening at that point in the program. The **_breakpoint_** allows you to examine the objects that you are dealing with and the properties of those objects.


### 2. Does the line of code on a breakpoint run when you start debugging?

**No**. The line on which the marker is will **NOT** be run.

The program runs normally until it reaches the breakpoint. The program highlights the line in blue where the program is paused. The Debugger tool window will open up as soon as the breakpoint is reached.

So if your breakpoint is at line 27, the code will not run line 27. But it will open up the Debugger tool window at that point.

### 3. How do we debug the next line of code?

We debug a line of code by going into the Debugger tool and going to the Variables tab. Here we can see more information about the instances that are created. We can see the properties and values that are relevant to this specific line of code.

We use **_Step Over_** to run the line of code we are on to jump to the next line. If it jumps over it - it means that that line is not run. There is a bug! If the code does run. And every time you click on *Step Over*, every line is being run. **All is well!**


### 4. What does the step into command do?

**_Step into_** allows us to switch to the place where the breakpoint is at. We will be at the very start of the method. You can see which specific variables are part of this particular line/method at this specific point in time.

When you **_Step Into_** it again, and your method refers to, for example, a function in another a class - it will take you to that file in the program. **_Step Into_** basically allows you to delve into your method and takes you through various files (if the method uses functions from several files).


### 5. What is the difference between evaluate expression and evaluate code fragment?

- *Evaluate Expressions*: With evaluate expressions you can evaluate one expression. You can type an expression such as
`hotel.getBookingCount()`. When you click on evaluate, the tool will give the result of the expression. You can evaluate expressions and methods on instances of objects that have been created at this point in time. You don't need to use semicolons.

- *Evaluate Code Fragment*: When you open the evaluate expression window, you can click on the expand button in the line which opens **_Code Fragment_**.
You can run multiple lines of code and even create temporary variables to store information. You can actually run entire methods with multiple expressions.
`Booking booking = bookings.get(0);
hotel.addBooking(booking);
hotel.getBookings();`
Similar to Evaluate Expressions, when you evaluate the **_Code Fragment_** it will return the result. Every time you run it, it will remember the variables and the values in them. For example, if you had a counter with counter++ and it would return the value. Every time you would evaluate the code, the result returned would increment.
