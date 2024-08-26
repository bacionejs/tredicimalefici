[![Info](README.JPG)](https://bacionejs.github.io/tredicimalefici)

**Tredici Malefici** is a missile defense game where aliens have discovered your phobia of the number 13. To exploit your fear, they drop bombs adorned with 13 spikes. Turn the tables and use this fear to your advantage.

- Purpose: `js13kgames game jam javascript coding competition`
- 2024 theme: Triskaidekaphobia (fear of the number 13)
- Goal: Win the t-shirt prize
- Limitations: Portrait mode only
- Controls: Click/tap
- Tested on: Android phone/tablet (Chrome/Firefox), but it will probably work on anything.

- [Live](https://bacionejs.github.io/tredicimalefici)
- [Download](#How-To-Download)
  - download index.html
  - open your file manager
  - click index.html to run in your browser
  - click/tap to play
- [YouTube](http://www.youtube.com/@bacionejs) - demo


---

### Game Jam Post-mortem

- I always create my games with procedurally generated graphics and sound, a method I enjoy and use primarily because my editor and games are designed as a monolithic file. For more examples of vector graphics (and emoji graphics), check out my editor/games at [github.com/bacione/editor](https://github.com/bacione/editor).

#### Day 1
Finished the core game.

#### Day 2
Added health and ammo bars.  
Added sounds. I already had a rocket sound from my Marslander game, but I needed an explosion sound.  
I searched for an explosion sound algorithm but wasn't satisfied with what I found.  
Finally, I discovered that simply adding a lowpass filter and a ramp to my existing rocket sound did the trick.

#### Day 3
Added a boss-a UFO with a grinning alien that drops fast bombs.  
Testers (my family) didn't like the UFO, especially the grinning alien.  
I wasn't motivated to fix it since I preferred the previous simplicity, so I removed it.

#### Day 4
Testers experimented to determine the appropriate difficulty.  
Besides the minimum value (start) and maximum value (asymptote), I used one extra point and fed it into a logarithmic curve-fitting algorithm.

#### Day 5
The game is only 3k in size. I wanted to add more content to help me reach 13k.
I added 30 victory/philosophical phrases, but the apathetic text-to-speech (TTS) voice made most of them sound ridiculous, so I sadly removed all but two:
- "Great job"
- "You were really good"

#### Day 6
The game crashes on older phones after a while, so I fixed the explosion drawing algorithm.  
Added a random fast level. It seems to break up the monotony but, being only one extra line of code, hasn't helped me reach 13k.  
Experimented with additional sounds and music but decided against it because I don't like much sensory input.  
However, I know others might enjoy a sensory overload, so I might add more content later...

#### Day 7
I gave up on trying to make the game bigger.  
Chose a name for the game, made a youtube video, and called it a wrap.
