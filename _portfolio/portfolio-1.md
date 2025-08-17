---
title: "Using NFC Cards to Play Music From A Network Shared Folder"
excerpt: "On an Android Phone, a Raspberry Pi controlled headless device, and a Raspberry Pi controlled arcade cabinet.<br/><br/><img src='/images/NFC.png'>"
collection: portfolio
---

For better or for worse, I have convinced myself that I can tell the difference between lossy and lossless compression, even through my poorly amplified DT 990s. As such, I have built up a fairly sizeable music library. That’s great on my desktop PC, where the files are stored locally and there are a hundred pieces of excellent software to catalogue and play my music. It’s less good when I want to listen to my music on my phone, or in the kitchen.

The solution, inspired by this video (https://www.youtube.com/watch?v=-jGWjFR936o), was to network share my media library, get a pack of 50 RFID cards and write the name of the album (as the folder appears in my media library) to the contents of the card.

From there, each device required slightly different approaches:

The headless device was the simplest. It required mounting the network share drive to the pi with one of a hundred different methods, connecting an RC522 reader to it, and running (on startup) a very short script. All the script needs to do is listen for cards, ‘os.join’ the contents of the card to the directory of the mounted network drive, and play the files through mpv using an MPRIS command. I also included a couple of cards with commands like skip (also using MPRIS), and shutdown (using os.exec()).

The arcade player (more information about it here), was almost identical, except it required a graphical player, I ended up using Tauon (found here), mostly for synced lyric support. From there, I had to connect the arcade buttons, using qjoypad (or equivalent) to map the buttons to keys. I used the joystick for vol+/vol- and skip/prev, and then mapped various buttons to play/pause, mute, clear queue, and change view.  Then, one final script run at startup to move the mouse to the bottom right corner (because using raspi-config to hide the mouse makes making any changes a painful experience)

Find a video of the arcade machine working here

The android phone was, unfortunately, a bit of a cop out. Tasker was the obvious choice for this project, and it works brilliantly except for the fact that I could find no way to mount the network share in a way that Tasker could access. This meant that I had to store music locally on the phone. I used FolderSync to regularly clone the network share to my phone, so at least new music will always be accessible, but my storage is running out fast!

*PUT TASKER CODE SCREENSHOTS HERE*

The list of the 50 albums that I ended up including can be found here. 

