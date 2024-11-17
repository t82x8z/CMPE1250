java c
CMPE1250 – LAB #1: SCI Tx and Rx, RTI based events. 
The purpose of this LAB is to be able to configure different time settings based on the RTI.
Those settings could be changed through button presses as well as through input received from the terminal. We will also send feedback to the terminalso the user can interact with the firmware running on the board.
PART A 
Create an RTI non-blocking event to toggle the RED LED every 50[ms]. Given the fact that the RTI provides you with an accurate 1[ms] tick, this should be a simple task to accomplish. Verify this functionality using an oscilloscope or AD2.
PART B 
We will now allow this toggle event to be adjusted to settings between 10[ms] and 100[ms], inclusive. Add functionality such that when the UP switch is pressed, the RED LED toggle
event will increase the time in multiples of 10[ms] up to a maximum of 100[ms]. Pressing   the DOWN switch will decrease the RED LED toggle event in multiples of 10[ms] down to a minimum of 10[ms]. Verify this functionality using an oscilloscope or AD2.
PART C 
Up to this point you have been sending ascii characters to the terminal as well as receiving them from it. Including the stdio.h library will allow you to, for instance, send a number formatted as text using sprintf. The other capability is to receive text from the terminal and parse it to a number, if possible, using sscanf. The sscanf function will return 1 if the text was able to be parsed into a number using the format specifier (%d, %f, etc.), otherwise it will return 0. This could help you handle the wrong input.
We wo代 写CMPE1250 – LAB #1: SCI Tx and Rx, RTI based events
代做程序编程语言uld now like to set the toggle event time to any number between 10 and 100 inclusive, having a resolution of 1[ms] this time, as opposed to the 10[ms] in Part B. This will be accomplished adding the following functionality: 
-     Accept input from the terminal and process it once the user presses the ENTER key (CR).
-     If the input cannot be parsed into a number of the format specifierselected, send the following message to the sci: “Input in the wrong format”. 
-     If the input can be parsed into a number, but it is less than 10, or greater than 100, send the following message to the sci: "Wrong setting, number must be between 10 and 100 inclusive”. 
-     If the number meets the requirements for a proper toggle event as defined, adjust the RED LED toggle time in [ms] to be set to the value entered. At this point, send the following message to the sci: “RTI event set to xx[ms]”, where xx is the number of milliseconds the time event was updated to. Verify this functionality using an oscilloscope or AD2. Make sure to add “\r\n” at the end of each message sent to the sci so they can be display in a single line.
Remarks 
•    Please note that if you send a number from the sci to set the time to anon-multiple of
10, the button presses should still work after with increments and decrements by 10, but the time should never exceed 100[ms] or be less than 10[ms].
•    Once you have completed Part C, you could add the feedback message: “ RTI event set to xx[ms]” to also be sent to the sci when the UP or DOWN switches are pressed.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
