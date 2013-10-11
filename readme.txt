*****************************************************************
W5200 Arduino Ethernet Library
******************************************************************
* Update History.

11/Oct./2013
-. Change the W5100 code under Sam folder(Arduino Due)
-. SPI clock set to 48Mhz and add delay routine
* How to use
-. Copy 2 fils from AVR to ..libraries/Ethernet/arch/Avr/utility/
-. Copy 2 fils from SAM to ..libraries/Ethernet/arch/Sam/utility/


2/Feb./2013
-. Update for supporting Arduino Due (32bit) : you can find the changes by checking #ifdef W5200
-. Changes: Make 2 folder, AVR and SAM.
-. AVR folder id for 8bit AVR and SAM folder is for 32bit
-. Contribution for supporting 32bit code: Fabien Duay (deayfabi at gmail.com)
* How to use
-. Copy 2 fils from AVR to ../avr/libraries/Ethernet/utility/
-. Copy 2 fils from SAM to ../sam/libraries/Ethernet/utility/


*****************************************************************
W5200 Arduino Ethernet Library
******************************************************************
How to use:

1. Install W5200 library
   Overwrite w5100.cpp, w5100.h to the "/libraries/Ethernet/utility" folder in your Arduino IDE. 

2. Using the W5200 library and evaluate existing Ethernet example.
   In the Arduino IDE, go to Files->Examples->Ethernet and open any example, compile and upload the file to Arduino board.

3. Note: libraries/Ethernet/Ethernet.h needs the following at line 10 instead of #define MAX_SOCK_NUM 4, since it doesn't #include "w5100.h" anymore:
   Thanks "Matthew Lange"

#ifdef W5200
#define MAX_SOCK_NUM 8
#else
#define MAX_SOCK_NUM 4
#endif