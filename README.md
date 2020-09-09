# light-and-sound-cornhole-game
When a bag goes into the cornhole LED's and Sounds are activated.
Tuesday Sept 8th 2020 added Adafruit Circuit Playground Code to Repository.  Victory!  Brand new to Github.
CircuitPython Audio Out
lady ada
Though the following example uses the Circuit Playground Express to demonstrate, the code works exactly the same way with the Circuit Playground Bluefruit. Simply copy the code and follow along with your Circuit Playground Bluefruit!
The Circuit Playground Express has some nice built in audio output capabilities.

There are two ways to get audio output, one is via the small built in speaker. The other is by using alligator clips to connect a headphone or powered speaker to the A0/AUDIO pin.

circuit_playground_spkr.jpg
The speaker is over here, its small but can make some loud sounds! You can ENABLE or disable the speaker. If you disable the speaker, audio will only come out the A0/AUDIO pin. If you enable the speaker, audio will come out from both!

If you want to connect a speaker or headphones, use two alligator clips and connect GND to the sleeve of the headphone, and A0/AUDIO to the tip.

The A0/AUDIO pin cannot drive a speaker directly, please only connect headphones, or powered speakers!


Basic Tones
We can start by making simple tones. We will play sine waves. We first generate a single period of a sine wave in python, with the math.sin function, and stick it into sine_wave.

Then we enable the speaker by setting the SPEAKER_ENABLE pin to be an output and True.

We can create the audio object with this line that sets the output pin and the sine wave sample object and give it the sample array

audio = AudioOut(board.SPEAKER)
sine_wave_sample = RawSample(sine_wave)

Finally you can run audio.play() - if you only want to play the sample once, call as is. If you want it to loop the sample, which we definitely do so its one long tone, pass in loop=True

You can then do whatever you like, the tone will play in the background until you call audio.stop()

https://learn.adafruit.com/adafruit-circuit-playground-express/circuitpython-audio-out

Playing Audio Files
Tones are lovely but lets play some music! You can drag-and-drop audio files onto the CIRCUITPY drive and then play them with a Python command

Here's the two files we're going to play:

Click the green buttons to download the wave files, and save them onto your CIRCUITPY drive, alongside your code.py and lib files

