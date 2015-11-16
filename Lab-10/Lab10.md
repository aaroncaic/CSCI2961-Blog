## Lab 10 Blog

#### Group Members: 
  * Aaron Cheng
  * Haoxin Luo

---------------------------------------

##### Part 1 (Setup)
* We "synced" our Arduino/Genuino Mega 2560 board with Arduino IDE.
* After that we compiled and uploaded `Blink` without a problem.
* The LED blinked every second, but we also played around with the speed.

---------------------------------------

##### Part 2 (LCD Setup/Printing)
* We copied and pasted the custom LCD library (provided to us) into the Arduino IDE.
* Compiling the code gave us errors because it could not recognize a lot of the characters in the code due to copy and pasting.
* Thus we typed the code manually instead. That solved the issue.
* After compiling and uploading the code, the LCD printed "Hello World" as it should.
* Screenshot:
 ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab10_1.jpg)

---------------------------------------

##### Part 3 (Printing Over Serial)
* With the help of code examples from the Arduino IDE Examples library, we managed to get serial printing to work relatively quickly.
* After compiling and uploading the our code, we opened up the Serial monitor and typed in "Lab Part 3". Here is the result:
 ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab10_2.jpg)

---------------------------------------

##### Part 3 (Continued...: Handling Newlines)
* Making our code handle newlines, `\n`, took a lot longer than expected.
* A lot of trial and error was involved due to our lack of knowledge on the Arduino library.
* In the end we finally got it to work properly. We typed in "hello \nworld" and here is the result:
 ![](https://raw.githubusercontent.com/aaroncaic/CSCI2961-Blog/master/Lab%20Screenshots/Lab10_3.jpg)
