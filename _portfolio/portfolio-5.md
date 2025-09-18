---
title: "The PopBox"
excerpt: "Make a modern pop song in minutes"
collection: portfolio
---

I’m sure everyone has seen [that](https://www.youtube.com/watch?v=oOlDewpCfZQ) Axis of Awesome video, about how all modern pop is built around the same 4 chords: I, IV, VI, vi.
This device takes that idea further, making it easier than ever to from concept to having the basis of a pop song blocked out. 
Using the knob, you can select a key, and a depth for all chords. Then, each red key will play a different chord, and each grey key will modulate its corresponding chord, either up or down, which can be changed by clicking the knob.

It is programmed entirely in circuitpython, and the code can be found [here](https://github.com/tomjowen/PopBox).

Parts list:
* Raspberry Pi Pico
* KY-040 encoder
* I2C screen
* 8x Keyswitches
  
I then 3D Printed the backplate, keycaps and encoder knob (.stl files available in the repository), and chiselled out a large block of wood as the housing.  
