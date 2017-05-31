#		python code
#		script_name:Independent Project
#
#		author: Jennifer Mizhquiri  
#		description: Instrumental
#

from earsketch import *

init()
setTempo(110)

melody =YG_ALT_POP_MELODY_4
main=YG_ALT_POP_PIANO_5
loop =RD_EDM_DRUMBEATPART_2
violin =Y09_VIOLIN_1#
clap =OS_CLAP04
sadpiano =YG_POP_PIANO_7
harp = RD_CINEMATIC_SCORE_HARP_3
wobble = YG_ALT_POP_SNARE_2
beat1 = "0--0--000--00-0-"
#line 1
fitMedia(main,1,1,26)
setEffect(1, VOLUME, GAIN, 0, 23, -60, 25)
#repears low thump
for measure in range(4,11,2):
  fitMedia(loop,2,measure,measure + 1.5)
  makeBeat(wobble, 3, measure + 3 , beat1)
  
for measure in range (4,11):
  if (measure % 2 == 1):
    setEffect(2,PAN,LEFT_RIGHT,-90,measure,-90,measure+.5)
  else:
    setEffect(2, PAN, LEFT_RIGHT,100,measure,100, measure +.5)
#line 4

fitMedia(harp,6,12,15)
fitMedia(harp,6,21,25)
setEffect(6, VOLUME, GAIN, 0, 9, -60, 25)
fitMedia(clap,4,17,23)

#line 5

fitMedia(violin,5,12,24)
setEffect(5, VOLUME, GAIN, -10, 10, -60, 23) #Lower Vol for violin, to make piano dominate

#end

finish()

