### Week Six: Earsketch
  * This week I learned the more creative and imagenitive aspect of Earsketch and how I could manipulate filed or create my own files to aquire the exact beats needed to create my own song.
#### New Functions
makeBeat() takes four arguments:
1. Clip Name
2. Track Number
3. Measure Number
   * makeBeat() only requires a starting measure
4. Beatstring
##### How it is structured / Applied
```ruby
def createBeat(startMeasure, soundClip, beatString):
  endMeasure = startMeasure + 3
  for measure in range(startMeasure, endMeasure):
    makeBeat(soundClip, 1, measure, beatString)
    return endMeasure
```
  #### What did I learn/ How is it useful?
  Learned to return ending measure so we can use it outside function. It cuts back time, only if a person plans on repeating the same beat in different parts of the song. At first I thought It would be useful just in minimizing code, but I later learned that it also allows for more control in the creative song process.
  

#### String Concatenation
  * In languages like ruby , we were taught that you can combine several phrases to make a coherent sentences.
  * We were accustomed to seeing it as "hello" + ' ' + "world"
The end result would give us `hello world`.
In Earsketch concatenation is used to bring different rhythms.
  * It is used like `beatString1 = "0++00-0+"`
##### Reflection
1. Today I learned that sometimes to get you vision properly projected, you might have to create your own methods, and experiment with what the Earsketch API provides you. For instance the sound files might not be what you envision, which is okay, the person just has to go the extra mile to figure out how to create the beat they want.
2. Perserverance. Do not settle for code that works. If it is not what you wish it looked like, sounded or any other aspect look for a solution. When I was learning string concatenation I was a bit confused. I thought that the first example would demonstrate how it would change the song. Yet every time I hit run nothing happened. At first I thought it was a browser error. Once I had tried several and nothing was working, I was about to skip the chapter. Instead, I did a more detailed google search (string concatenation in earsketch) and came to the search 'Going Further With Earsketch'. After reading this, I realized that the problem, was that it was literally concatenating strings, which would not provide a sound. The next example wouild manipulate the song.





