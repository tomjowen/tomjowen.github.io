---
title: "Building (and Then Using) a Hardware Password Manager"
excerpt: "A surprisingly good way to manage passwords using a Raspbery Pi Pico and an HID compatible Arduino<br/><br/><img src='/images/500x300.png'>"
collection: portfolio
---

The code for this project can be found on my github here

Software password managers are fine, but as someone who uses a work laptop, a phone, lab computers, a personal laptop at uni, and a desktop pc at home, they’re just a bit inconsistent. Having a physical device was designed to centralise and solve that problem. 

Unsurprisingly, as a password manager, it can generate, store, recall, delete, regenerate and type passwords for a functionally unlimited number of accounts.  Passwords can be found either through search or through a favourites system. 

Components:
*Raspi Pico
*Arduino Pro Micro – The pico is not HID compliant, so a pro micro is needed to type passwords in to a device over USB, they communicate over serial. The pico can be powered from the micro, so only one cable is needed 
*4x4 Matrix Keypad – Needs an input from somewhere, 0-9 act as the keyboard (old Nokia phone style), with the letters being for navigation. This is a major drawback to this system, typing feels slow, clunky and mushy, and gives the device a large footprint. 
*SD Card Reader – Data is stored here, encrypted with a pin that you setup
*I2C Display

Videos of it working can be seen [here](https://www.youtube.com/shorts/KOHCZmaIBUA) or a longer playlist [here](https://www.youtube.com/playlist?list=PLouFc3BkexWFiNbRgFanChZ0leR1_jGs7). This project was originally made for my Computer Science NEA, so these videos are proving functionality through tests.
