# Week Five: Background Process of Music and Customization

Songs typically have an ABA mode
  * Section A: measures 1-4.
  * Section B: measures 5-8. 
  * Section A (repeated): measures 9-12.
```python
# python code
#
# script_name: A-B-A Form
#
# author: Jennifer (modified from earsketch tutorial)
#
# description: A song with A and B sections
#
#
#

#Setup
from earsketch import *
init()
setTempo(120)

#Music

# Create an A section

fitMedia(HOUSE_ACOUSTIC_PIANO_003, 1, 1, 5) # main
fitMedia(RD_WORLD_PERCUSSION_DRUMPART_24, 2, 1, 5) # drums
for measure in range(1, 5):
	fitMedia(HOUSE_ACOUSTIC_PIANO_003, 3, measure, measure + 1)
	
	# bassline, repeatedly fitting first measure of clip
for measure in range(1, 6, 2):
	fitMedia(HOUSE_ACOUSTIC_PIANO_003, 4, measure, measure + 1) # backing

setEffect(4, DELAY, DELAY_TIME, 500) # delay on track 4

# Create a 4 measure B section between measures 5 and 9

fitMedia(RD_WORLD_PERCUSSION_DRUMPART_3, 1, 5, 9) # sparse drums
fitMedia(RD_ROCK_POPELECTRICLEAD_3, 3, 5, 9) # rattling
fitMedia(RD_CINEMATIC_SCORE_MAINDRUM_1,5,5,9)
fitMedia(RD_EDM_DRUMROLL_BREAK_3,6,5,9)
# Then back to section A at measure 9

fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_1, 1, 9, 13) # main
fitMedia(RD_WORLD_PERCUSSION_DRUMPART_24, 2, 9, 13) # drums
for measure in range(9, 13):
	fitMedia(HOUSE_ACOUSTIC_PIANO_003, 3, measure, measure + 1) # bassline, repeatedly fitting first measure of clip
for measure in range(9, 13, 2):
	fitMedia(HOUSE_ACOUSTIC_PIANO_003, 4, measure, measure + 1) # backing

setEffect(4, DELAY, DELAY_TIME, 500) # delay on track 4

#Finish
finish()
myFunction(). It has two parameters, meaning it takes two arguments when called. These parameters (startMeasure and endMeasure) are the variables that hold the arguments being passed to the function, so these variables can be used inside the function body. A custom function can have as many parameters as necessary.

def sectionA(startMeasure, endMeasure):
  # create an A section, placing music from startMeasure (inclusive) to endMeasure (exclusive)
  fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_1, 1, startMeasure, endMeasure) # main
  fitMedia(RD_WORLD_PERCUSSION_DRUMPART_24, 2, startMeasure, endMeasure) # drums
  for measure in range(startMeasure, endMeasure):
	  fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_7, 3, measure, measure + 1) # repeated bassline
  for measure in range(startMeasure, endMeasure, 2): # every other measure
	  fitMedia(RD_WORLD_PERCUSSION_KALIMBA_PIANO_3, 4, measure, measure + 1) # backing
  setEffect(4, DELAY, DELAY_TIME, 500) # delay on track 4
```
#### How does the passing of data work?
I learned that all the data that is used to run a program, is not located in one place. There are two places where data lives that have to go in different cycles in order to arrive at their destined location aka the CPU. These new terms might sound confusing… So here is a quick vocabulary cheat sheet.
##### Vocabulary 
A process is a program
Processes are carried out by the computer’s CPU, or Central Processing Unit (control center)
computer’s memory holds data and processing instructions for the CPU to use (Primary Storage, RAM)
	Memory only stores data temporarily, till the process is currently running.
Hard Drive, Secondary Storage, holds high levels of data even as the pc shuts down. Does not interact directly with the CPU.
 Data goes from secondary storage to Memory so the CPU Can receive it.

  * Secondary storage -> Memory -> CPU

Inputs is data that is received by the computer.
Outputs are the data sent from the computer

#### How about in Earsketch?
We record data using the input device, which in this case would be the microphone.
After this, the CPU brings the data that carries the audio into the memory.
Once this task is completed, and you want to hear the music, you press play. This is when the CPU accesses the data in the Memory and sends an output to your earphones.

#### Reflection
1. I believe that if you find a certain thing interesting in your topic, that even though it is not in your tutorial, you should research it. It does not always have to do with how to code something . For instance, I liked the concept of the music structure and sought out to look for what are my other options. The task would be simple hence the fact that I already knew how to code it.

2. Ideas and creativity are important. When starting your project your mindset should not be "what do I need to meet requirements?" but "what do I want my work to show off?".

