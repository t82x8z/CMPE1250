java c
CMPE1250 - ICA #8, Serial Communication Interface (SCI) 
Built a new library (compilation unit), according to the header “sci.h” provided. You are required to provide an implementation of the basic functions described in the header file.
This assignment verifies the functions in the library and introduces you to SCI operation and interfacing with a terminal.
Part 1 
Locate and run a Terminal. To begin with, use the 19200 baud communication rate and default settings for the rest (8 data bits, no parity, 1 stop bit, no flow control). Write a program that that repeatedly receives a character from the terminal (i.e. the computer keyboard) and echoes it back to the terminal (i.e. the computer monitor). This will involve the use of sci0_rxByte() (non-blocking) and sci0_txByte(). If you are using Tera Term, goto setup->Terminal and make sure the Local echo function is enabled. Can    you run your code and explain what is happening and why? 
Try this other baud rates as an exercise: 38400, 115200. Can they all work at 8[MHz] bus speed? Explain  why yes or why not. If one of them cannot run at 8[MHz], make sure you set your bus speed to 20[代 写CMPE1250 – ICA #8, Serial Communication Interface (SCI)R
代做程序编程语言Mhz].
Part 2 
For this part, keep the baud rate at 19,200. Add code that will perform. the following:
-      Pressing the LEFT switch will turn the RED LED ON and send the message:  "LEFT pressed\r\n" to the sci0. Releasing the LEFT switch will turn the RED LED OFF and send the message: "LEFT released\r\n" to the sci0.
-      Pressing the CENTER switch will turn the YELLOW LED ON and send the message:  "CENTER pressed\r\n" to the sci0. Releasing the CENTER switch will turn the YELLOW LED OFF and send the message: "CENTER released\r\n" to the sci0. 
-      Pressing the RIGHT switch will turn the GREEN LED ON and send the message:  "RIGHT pressed\r\n" to the sci0. Releasing the CENTER switch will turn the GREEN LED OFF and send the message: " RIGHT released\r\n" to the sci0.
Please note hat for this part to work properly you need to track the “state” of the switch, so it performs the operation only once per press and once per release.
Why do we add “\r\n” at the end of the message? what happens if we do not add those or if we add only one of them? Experiment and explain your conclusions.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
