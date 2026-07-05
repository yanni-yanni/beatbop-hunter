# BeatBop Hunter

**Watch Beatbop find the beat in music in real time!**

BeatBop Hunter is a little interactive demo that listens to audio on the fly 
and performs beat extraction. It finds where each beat lands, and how fast the
music is going. It only ever hears the music *up to the current moment*. 
So you're watching it figure out the beat the same way you would in real time,
with no idea what's coming next! :)

## What it can do

- **Find beats as the music plays.** Every time it hears a beat, a dot appears
  and makes a click sound.
- **Estimate the tempo.** It shows a live guess of the speed in BPM (beats per
  minute), it's not "accurate" per se because it offers the instantaneous est. 
  Still, it should indirectly offer some information about the performance. 
- **Show its confidence.** A number tells you how sure it currently is.
- **Track through changes.** Try the tempo-change or accelerando examples!
- **Run on your own music.** Drop in any audio file and it does the same thing.

It works great on some audio, while some other is harder (i.e. many tracks and 
multiple instrument simultaneously). Try it out yourself and find its limit!

## How to open it

Just double-click **`demo.html`**. It opens in your web browser and runs on its
own. 

If it ever looks stuck or out of date, do a hard refresh: **Cmd+Shift+R** (Mac)
or **Ctrl+Shift+R** (Windows).

## How to use it: 

**Choose a stimulus (the button grid).** These are built-in test rhythms. Each 
button has a short note about what it tests:

- *Fixed 120 bpm* / *Fixed 90 bpm*: steady, metronomic beats.
- *Tempo change 100→150*: the speed jumps halfway.
- *With rests*: some beats are missing.
- *Syncopated*: accents land off the beat.
- *Accelerando*: the tempo speeds up continuously.

The button you're playing will be highlighted. 

**Stop.** Stops playback.

**Beat clicks (checkbox).** Turns the click sound on or off. With it on, you
hear a tick every time a beat is detected. Turn it off to hear the music 
alone with visual dots only.

**The counters (top right).** Live readouts while it plays:
- *tempo*: its current guess of the speed, in BPM.
- *conf*: how confident it is right now (higher is surer).
- *onsets*: how many beats it has detected so far.

**Drop an audio file / browse.** Drag any audio file onto the dashed box, or
click *browse* to pick one. It starts playing right away and gets its own
button so you can replay it. You can keep dropping in new files anytime, 
no need to reload the page. (WAV and MP3 work most reliably.)

**Two visualization timelines.**
- *Top: Onset-strength envelope:* a live trace of the audio.
- *Bottom: Detected rhythmic events:* each detected beat as a dot. 
   The dashed line is the playhead (the current moment). Dots should only 
   ever appear at or behind it and never ahead because the tracker can't see the future.

## More about "Listening forward only"

Detection at any moment uses only what's been heard so far. (The audio file itself is 
loaded so your browser can play it, but the beat-finding part never gets to look ahead.)

## Citation

**If you use BeatBop Hunter in your work, a class, or a write-up**, please
credit it as:

> BeatBop Hunter: an interactive demo of online (real-time) beat tracking.
> [Your name / project], 2026.

*(Replace with your own name and a link once you publish it.)*

The beat-tracking ideas here build on standard approaches in music information retrieval 
and rhythm cognition, in particular:

- Large, E. W., & Jones, M. R. (1999). The dynamics of attending: How people
  track time-varying events. *Psychological Review, 106*(1), 119–159. — the
  entrainment / dynamic-attending model behind the oscillator tracker.
- Bello, J. P., Daudet, L., Abdallah, S., Duxbury, C., Davies, M., & Sandler,
  M. B. (2005). A tutorial on onset detection in music signals. *IEEE
  Transactions on Speech and Audio Processing, 13*(5), 1035–1047. — the onset
  detection methods.


