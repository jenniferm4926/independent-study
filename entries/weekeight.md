## Blog #8 : Implementation
---
   * This week has been all about refreshing the unit and tinkering with different methods in Earsketch to create a good main beat.
   * I learned from Week #, that I needed to slow down and stop trying to jump straight in with all the instruments at once. I decided I wanted the main part of my project to be based on the melody of the piano.
   * Once I had picked out the beat, I realized that my memory on the order of the parameters was faulty. This helped me realize I had to have open the Earsketch review sheet, that explained a quick summary for the job of each method.
---
#### Most Recent Code
``` python
#		python code
#		script_name: Run.py
#
#		author: Jennifer Mizhquiri0
#		description: Independent Study Project
#

from earsketch import *

init()
setTempo(105)
beatstring = "0-0+-00++00+-00+0"
beatString2 = '0++-0+1--+000+++0+++'
#section A fitMedia(Sound,Intefer,Float,Float)
fitMedia(YG_NEW_HIP_HOP_GUITAR_2,1,7.5,9.5)
fitMedia(YG_POP_PIANO_7,1,1,7)
makeBeatSlice(HOUSE_BREAKBEAT_003,2, 4, beatString2, [1, 1.5, 2.125, 2.1875])
setEffect(2, VOLUME, GAIN, -60 , 2, 1, 10) # Makes an effect ramp between measures 4 and 8, moving from -60dB to 0dB
makeBeat(YG_POP_PIANO_6,2,7,beatstring)
fitMedia(YG_POP_GUITAR_1,3,2,4.5)

#section B
#setEffect(1, BANDPASS, MIX, 0.3)
#insertMedia(fileName,TrackNumber,Trackstartlocation) #plays the whole clip from where you say it should start
#makeBeatSlice(fileName,track,measure,string,beatnumber) #beatnumber A list/array of start locations within audio file (e.g. [1.0, 2.5]

finish()
```
##### Next Steps
  * I still want my code to follow the ABA music format. My next steps would be creating Section B, using totally different methods and then repeating a lower volume for the closing Section A.
  * I need to add in more instruments towards the middle of the song once I deciede to expand the time.
  * I also want to make it a bit more formulaic so the code is not so long, and remains efficient.
#### Problems/Solution/Advice
  * One of my main problems this week was figuring what method was the best to get the code to do a certain task. At first I wanted to try to use insertMedia instead of makebeat. It was not working as I had hoped. I returned back to the lesson and realized that insertMedia allowed for little manipulation. It's ain task was to play the whole audio file till beginning to end. makeBeat allowed for me to be creative, it worked to cut up a beat by creating spaces, prolonging a beat or making it quicken. Thus, my advice stays being, you need to give yourself time to make changes. Practice commenting lines of code and then switching the method and see if it mends better with the code you created.