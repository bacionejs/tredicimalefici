[![Play](README.JPG)](https://bacionejs.github.io/tredicimalefici)

## Description
*Tredici Malefici* **(13 evils)** is a missile defense &#128640; javascript game where aliens &#128125; have discovered your phobia of the number 13. To exploit your fear, they drop **13 bombs** adorned with **13 spikes**. Turn the tables and use this fear to your advantage.

- Controls: Click/Tap
- Tested on: Android phone/tablet (Chrome/Firefox) in portrait mode, but it will probably work on anything.
- Download: The game is one monolithic index.html file with no external dependencies, so it is easy to download and run offline from your file manager in your browser.
- [Live](https://bacionejs.github.io/tredicimalefici)
- [YouTube](http://www.youtube.com/@bacionejs)
- [Code](https://github.com/bacionejs/tredicimalefici)
- [Post-mortem](https://github.com/bacionejs/tredicimalefici#post-mortem)

---

## Purpose
- Competition: [js13kgames](https://js13kgames.com)
- Theme: The 2024 theme is Triskaidekaphobia (fear of the number 13)
- Goal: Win the t-shirt prize 🏆🎉

---

## Post-mortem

- Day 1: Finished the core game: bombs, rockets and explosions 💥
- Day 2: Added a [lowpass filter and ramp](https://bacionejs.github.io/explosion) *explosion sound* 🔊
- Day 3: Added *health and ammo bars* 🚥
- Day 4: Added a [logarithmic curve-fitting algorithm](https://bacionejs.github.io/difficultyalgorithm) for *level difficulty* 📈
- Day 5: Added *text-to-speech* (TTS) 🗣️
- Day 6: Added random 😈
- Day 7: Chose a name for the game, made a *youtube video*
- Day 8: Added intro

and... 🎬

Making this game was 🥳
I learned how to use *sin, cos, PI, hypot, atan2, pow, lowpass, ramp, tts and curve-fitting* 📚
Graphics and sound were *procedurally generated*. For more examples, see [Bacione JavaScript Editor](https://github.com/bacionejs/editor) 🫦

The game is small, mainly because my Bacione editor on mobile isn’t designed for large projects, but also because I like simplicity.[^1]

I was at first lost about what to code for the 2024 theme *Triskaidekaphobia* (fear of the number 13). While the 2023 theme *13th Century* seemed easier to have ideas about, what can you do with a phobia? I researched Triskaidekaphobia and dozens of phobias and still nothing came to mind…

Previous games I made didn’t use standard game algorithms, so I wanted to try learning them. I've never used `hypot`, `sin`, `cos`, `atan`, etc. Those functions just all sounded so CPU intensive, and I’m a minimalist, right? For Marslander I simply did `y > mountain[floor(x)]` and for Ski `x - skier < tree && tree < x + skier`.[^1]

I started out with JavaScript Classes, but eventually refactored to use function closures… because they are more beautiful. It is pleasantly weird how the closure remembers the variables in the scope it was returned from. I pushed hard to keep my global variables to a minimum, generalize functions, and add some to my library.

If you read my code you might be alarmed at the formatting. Since I program on mobile, screen real estate is at a premium. White-space is for `&&`, `||`, and multi-line blocks, either vertical (outside) or horizontal (inside), but not both. Horizontal white-space is 2 spaces and vertical-whitespace is 1 blank line, except for large blocks which have 9 blank lines. Why are `&&` and `||` the only special characters than I wrap with white-space? Because they are the only ones that blend in with alphanumeric characters, making them hard to spot.

My programs are always one monolithic file with no external dependencies. This is because Bacione is designed to run without a server, offline on Android from your file manager in your Chrome browser. I don't have a computer and at one point my solar panel was too small to charge anything bigger than a mobile device. I struggled for a while with various mobile editors but found Neovim with Apache on Termux to be the best.[^2] But vim-motions are difficult while thumb typing on mobile. Plus I wanted to remove the server. Thus, Bacione was conceived on a remote pacific island with sparse internet, where 90% of people don't have internet or a computer. I had hoped to make Bacione in a few weeks, but months later, by the time it was finished, my daughter had lost interest in programming. Nowadays she draws. So, not wanting it to be a waste, I've tried to spread the news.

Sooo, since I use monolithic files, I only use procedurally generated graphics and sound. It was borne of necessity but I enjoy it. There is just something intrinsically appealing about vector graphics and sound generation.

I don't like being unoriginal but I enjoy making games based on older designs. I've never done a shooting game so that was at the top of my list. But I didn't want complex controls. For example, the Asteroids’ ship is very difficult to control on mobile. So, what about a stationary ship? Well, that is sort of a missile defense game.

I didn't want to spend more than a week on the game, and I'm not very good, so the game is very small. But it is beautiful and fun. Although, it could use some hectic overload to get your heart rate up or cause some rage. But alas, we have a pleasant shooter, with pleasant explosions and delicious neon vector graphics that look like candy. There IS a random boss that is an initial shock but after a couple times you have him figured out. Amidst the fantasia, a voice randomly pipes in about how well you are doing.

I spent many hours creating dozens of victory and philosophical phrases, gleaned from dozens of philosophical works and massaged them to be short and pithy. I had just bought my daughter Meditations by Marcus Aurelius and she hadn't touched it, so I conspired to put philosophy in a game. I'm too clever. Anyway, they sounded ridiculous when spoken by the blasé text-to-speech voice. So alas, there remain but three, philosophy-free. Time wasted.
> "It is not that we have a short time to live, but that we waste a lot of it."  
> — **Seneca**, *On the Shortness of Life*

Surprisingly, I spent a large amount of time on one line of code: the logarithmic curve-fitting formula for level difficulty. Now, this might seem like an obvious formula to you, but it was a breakthrough for me. I assume everybody uses something like it to increase a game's difficulty. I was so enamored by the idea, and it seems so fundamental to gaming, that I dedicated a whole repository to it. [^3]

Also, surprisingly, I spent a lot of time looking for an explosion sound. Part of the problem is that when doing Google searches, the overwhelming number of links are audio files or libraries. Even when searching “procedurally generated,” or some variant of that, I still struggled finding anything. And the libraries that I did find were complex. I just wanted a snippet that was less than 5 lines. So I consulted ChatGPT. We had many long discussions. We were both patient and kind, but we gained little ground. At one point, it did suggest lowpass and ramp but the HTML page it produced didn't sound anything like an explosion. I even had it produce a page with several sliders so I could tweak the parameters live. Still no luck. Part of the problem is that overlapping ideas can hide the solution. And I was too lazy to learn enough about this particular topic to understand what I was doing. I was poking in the dark. So, once again I dedicated an entire repository to it.[^4] I even submitted it in Google Console to ensure the love spreads a little quicker.

In the beginning, I started with a text status which included score, level, health, ammo, and speed. But after most debugging was completed, I really didn't need score and speed. Besides, level is a sufficient gauge of progress. Also, it isn't necessary to see the level value until the level is finished, so I moved that to the inter-level splash screen. Three down, only two left, health and ammo, and well, isn't that the standard anyway? And shouldn't they be graphical? Standard right? I need to stop being so minimalistic. I generalized the function enough to shoehorn into my library. Also, if you look close enough you will see a simple optimization. I hate bothering the CPU.

When I added a glass dome as the starbase, it always seemed like there should be a party going on inside, a rave:
```
souls dancing
lost in good memories
with their brothers in arms
blue light pulsing to the rhythm
extending outward to the glass dome
shimmering with a hint of cosmic rays
```

The music is inline base64 that will make you want to stand up and dance. By adding a fade in/out it doesn't glitch in a loop. The pulsing neon blue of the rave is an alpha adjusted gradient loop on canvas. A more obvious choice is css animation but I do everything on canvas for consistency.

Now, I must say that I am horrified when people don't include a screenshot in their repository. So that was part of wrapping things up. Also, it is helpful to have a YouTube demo. And it is so simple to set up a live link via GitHub Pages, so why wouldn't anybody do that too?

Normally, I do a screen recording on my phone and then copy it to my tablet where I crop it with ffmpeg. But in the future, I plan to use a wrapper page that simulates a phone's dimensions so it can all be done on the tablet.

I’m tempted to do a tutorial like I did for Ski and Marslander.[^5] I wrote a JavaScript app which semi-automatically generates tutorials. And, perhaps I should put the generator in a repository for others to use. I also have a generator for YouTube demos. So the toolbox of utilities seems to keep growing. Isn't that always the case?

[^1]: [Bacione JavaScript Editor](https://github.com/bacionejs/editor)
[^2]: [Neovim with Apache on Termux](https://github.com/bacionejs/termux)
[^3]: [Logarithmic Curve-Fitting for Level Difficulty](https://bacionejs.github.io/difficultyalgorithm)
[^4]: [Explosion Sound Generation](https://bacionejs.github.io/explosion)
[^5]: [Ski/Marslander Tutorial](https://bacionejs.github.io/editor/Games.pdf)
