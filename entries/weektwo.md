# Intro to Music Week Two 
---
### Important terms to understand
  * Rythym 
    * arrangement of sounds as music flows
  * Tempo
    * speed of a song
    * measured in beats per minute (bpm)
  * Meter
  * Measure
    * Grouped Beats
  ##### Types of beats
  * Beat
    * Beat are grouped per measure. 
  * Sub-beat
    * Divisions of a beat
 

![measure](barStructure-cropped.png "different measures")
  ###### Why are they useful?
  * It helps you use the DAW more efficently by helping you to organize the elements of your music in time.
---
### Functions()
  * I learned that the order matters when putting in arguments and can cause disruptions in code.
---
### Numbers
#### Types of Numbers
1. Integers (Pos/Neg Whole Numbers)
2.  Float (Pos/Neg Fraction Numbers)
 
----
#### Assignment Operators
  * Equal Sign(=) is like a"hold." 
  * The variable name goes on the left of the assignment operator.
  * Value it holds goes on the right.
----
#### Constants
* A constant stores values that never change.
* Constant's have to be  capitalized and do not use  spaces, but instead rely on underscores.
    * Examples: audio files
---
#### Common Run-in Errors (I ran into)
1. Mispelling
2. Parenthesis Placement
##### Other Possible Errors?
3. CaSe SeNSitIvty
4. Initializing 
---
### What I learned
#### Wrong Code
```python
# python code
# script_name: Find The Error 1
# author: The EarSketch Team
# description: Find and fix the error in this script

from earsketch import *

init()
setTempo(88)

fitMedia(electroString, 1, 1, 9)
electroString = Y13_STRING_1

fitMedia(drums, 2, 5, 9)
drums = HIPHOP_DUSTYGROOVE_017

finish()
```
### My solution
```python
# python code
# script_name: Find The Error 1 (How I fixed)
# author: The EarSketch Team
# description: Find and fix the error in this script

from earsketch import *

init()
setTempo(88)
electroString = Y13_STRING_1
fitMedia(electroString, 1, 1, 9)

drums = HIPHOP_DUSTYGROOVE_017
fitMedia(drums, 2, 5, 9)

finish()
```
  * After I fixed the bug, I compared answers and learned that EarSketch recommends you declare variables in clusters on top. 
# Recomendations
  * Always comment code. Try commenting things out when it runs and does not go the way you want it to. Also comment what the code is supposed to do so you remember the next session or someone else can learn from it.
  * Learn to write your code the most efficent way possible. It makes it look neater and easier to see the different parts to the project. It makes it easier to comment blocks of code that do not work to fix bugs and evades confusion. I did not have proper indentations and syntax and the only thing that fixed the code was commenting line by line to add the missing ')'
  