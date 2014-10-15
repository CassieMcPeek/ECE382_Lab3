ECE382_Lab3
===========

SPI - "I/O"

# Purpose
The purpose of this lab was to use serial peripheral interface in order to communicate between the MSP430 and the Nokia1202 display. 

# Prelab
The prelab was turned in as a hardcopy to Capt Trimble. 


# Logic Analyzer

  The very first step in the logic analyzer section of this lab was to copy over the code Lab3.asm and make sure it was working correctly. The code was intended to draw a vertical line on the Nokia1202 display every time the button SW3 was pressed. The table below was then completed by finding the four writeNokiaByte calls throughout the code in order to generate the vertical bar by determining what parameters were being passed in.
  
  
![alt text] (https://raw.github.com/CassieMcPeek/ECE382_Lab3/master/Table1.JPG "Logic Analyzer")

After the table above was filled out and understood, I captured the generated waveform on the logic analyzer. The captured waveform is shown below:

![alt text] (https://raw.github.com/CassieMcPeek/ECE382_Lab3/master/Lab3_logic_analyzer.png "Logic Analyzer")

I then used the table above as well as the generated waveform in order to fill out the table below:

![alt text] (https://raw.github.com/CassieMcPeek/ECE382_Lab3/master/Table2.JPG "Logic Analyzer")

When the button is pressed, ther is a gap between the current line and the previous one because the commands in lines 276 and 294 are increased by 1. The data passed in through line 66 is never altered and the command executed in line 288 is never changed. 

Next, I configured the logic analyzer to produce a waveform to show reset on the falling edge:

![alt text] (https://raw.github.com/CassieMcPeek/ECE382_Lab3/master/Lab3_Reset_Analyzer.png "Logic Analyzer")

# Functionality

The required functionality of this lab was to create a block on the LCD that is 8x8 pixels with the location of the block passed in through the subroutine via r12 and r13. 

The updated code can be seen in the Lab3.asm file. 

I demonstrated required functionality to Capt Trimble on 15 OCT. 

Documentation: C2C Ian Goodbody assisted me with the required functionaility by assisting me in debugging my code and checking my syntax. Also C2C Dustin Weisner helped me format the logic analyzer to produe the desired waveforms. 

