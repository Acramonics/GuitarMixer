Things to try to make this work
===============================

1. Try using DC coupling on the 'scope

2. Try a larger PSU voltage

3. Try more PSU smoothing

4. Try the mixer stage alone on music

5. Try the buffer stage alone on music


Filtering
---------

4. Do we have just an HF effect or also ringing (impedance problems)?

5. Add 1K/10nF R-C low pass filter - before or after the opamp

6. Add 22pF cap U2 Pin3 to ground for high frequencies

Decoupling
----------

7. Add 470nF or 1uF cap between R5/R7 and U2 Pin2

8. Or add 100nF before R5 and R7

9. Try 100R and 10uF (+ to output) after opamp



Gain / feedback
---------------

10. Try R11 at 10k or 1k or shorted to reduce gain of inverter

11. Try R10 at 10K or 1k to reduce gain

12. Try R10 at 220k to increase gain

13. Add 4.7pF cap in parallel with R10

Bias
----

14. Remove R9 (9v positive bias)

15. Remove R8 (no positive bias)

16. Remove R8 and short R9 (non-inv input straight to earth)

17. Try R8 and R9 at 10K to increase current

18. Try C8 = 1uF or 47uF

19. Try C8 = 2.2uF and C7 = 22uF


Impedance matching
------------------

20. Try R5/R7 at 1K to reduce output impedance (and noise) from buffers


Major changes
-------------

21. Try separating signal ground from -ve power

22. Try a non-inverting amplifier for the mixer part (see below)

--------------------------------------------------------------------


Square wave testing
-------------------

https://sound-au.com/articles/squarewave.htm

High-frequency boost leads to peak at the start

1K + 10nF low pass filter (~16kHz) might help

Might prefer to use a higher-order 24dB/octave filter tuned to (say)
22kHz.

A descending flat top of a square wave indicates bass attentuation
An ascending flat top of a square wave indicates bass boost


Non-inverting amp
-----------------
https://share.google/images/nToTiObG5TNGJYSms
https://www.allaboutcircuits.com/video-tutorials/basic-amplifier-configurations-non-inverting-amplifier/

```
           | \
Vin -------|+ \
           |   \___________ Vout
           |   /        |
       ----|- /         |
       |   | /          |
       |                |
       +------|R2|------|
       |
       |
      ---
       R1
      ---
       |
       |
      GND

Vout = Gcl (closed-loop gain) = 1 + (R2/R1)
```

Other web pages:
----------------
https://www.reddit.com/r/diypedals/s/R89ESHo1lh
Transistor based mixer: http://www.seekic.com/circuit_diagram/Audio_Circuit/Mixer/
Other mixer circuits: http://www.seekic.com/circuit_diagram/Audio_Circuit/Mixer/
JFET mixer: https://www.diy-electronic-projects.com/p30-FET-Audio-Mixer
Inverting OpAmp mixer: https://es.pinterest.com/pin/714031715956747662/
Hybrid mixer: https://www.electroniq.net/audio/hybrid-2-channel-audio-mixer-circuit.html#google_vignette
Dual rail mixer: https://modwiggler.com/forum/viewtopic.php?t=258014
GGG Mixer: https://generalguitargadgets.com/pdf/ggg_mixer_sc.pdf
Vero Mixer: https://tagboardeffects.blogspot.com/2013/01/2-channel-mixer.html
