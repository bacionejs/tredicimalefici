[![Play](README.JPG)](https://bacionejs.github.io/tredicimalefici)

*Tredici Malefici* **(13 evils)** is a missile defense javascript game where aliens have discovered your phobia of the number 13. To exploit your fear, they drop **13 bombs** adorned with **13 spikes**. Turn the tables and use this fear to your advantage.

- [Live](https://bacionejs.github.io/tredicimalefici)
- [YouTube](http://www.youtube.com/@bacionejs)

- **Purpose: javascript coding competition for [js13kgames](https://js13kgames.com)**
- Theme: The 2024 theme is Triskaidekaphobia (fear of the number 13)
- Goal: Win the t-shirt prize
- Limitations: Portrait mode only
- Controls: Click/tap
- Tested on: Android phone/tablet (Chrome/Firefox), but it will probably work on anything.

- Download  
  - download index.html
  - open your file manager
  - click index.html to run in your browser
  - click/tap to play

---

### Competition Diary

#### Day 1
- Finished the core game: bombs, rockets and explosions

#### Day 2
- Added *linger and fade* to explosions
- Added *sounds*. I already had a rocket sound from my Marslander game, but I needed an *explosion* sound. I searched for an explosion sound algorithm but wasn't satisfied with what I found. Finally, I discovered that simply adding a *lowpass filter and ramp* to my existing rocket sound did the trick.

#### Day 3
- Added a boss -- a UFO with a grinning alien that drops fast bombs. Testers (my family) didn't like the UFO, especially the grinning alien. I wasn't motivated to fix it since I preferred the previous simplicity, so I removed it.

#### Day 4
- Added health and ammo *graphical bars*
- Added a [logarithmic curve-fitting algorithm](https://bacionejs.github.io/difficultyalgorithm)
for level difficulty.

#### Day 5
- Added *text-to-speech* (TTS) phrases.

#### Day 6
- Added a random *fast level* to break up the monotony.

#### Day 7
- Chose a name for the game, made a *youtube video*, and called it a wrap.

## Summary
It was fun making this game.

I learned how to use *sin, cos, PI, hypot, atan2, pow, lowpass, ramp and tts*.

Graphics and sound were *procedurally generated*. For more examples, see [Bacione JavaScript Editor](https://github.com/bacionejs/editor)

