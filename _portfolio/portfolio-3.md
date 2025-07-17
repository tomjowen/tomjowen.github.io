---
title: "Using IFTTT and SpotiPy to bulk sort Spotify’s recommendations"
excerpt: "Alternatively, SpoTinder"
collection: portfolio
---

I find Spotify’s ‘Discover Weekly’ playlists to be pretty hit or miss. It’s 30 songs every week, of which I’ll usually find 20 to be unremarkable, I’ll hate 7 or 8, and I’ll love 2 or 3. This app streamlines the process of finding ‘the diamonds’, while also letting you do it in bulk, rather than every week.

It uses IFTTT to push the discover weekly into a separate playlist every week without requiring any input from you. Then the app lets you play the music, and easily sort some songs into a new playlist with a single keypress, removing all songs heard from the original playlist.

To run the project, first [IFTTT](https://ifttt.com) will need to be setup.
Setup this applet, with your discover weekly, and a new bulk playlist:

![IFTTT](/images/IFTTT.png)
 
Download SpoTinder.py from my Github [here](https://github.com/tomjowen/SpoTinder)

Fill in Spotify user keys and playlist ids to python script  - this will require Spotify for Developers to be setup, and an app made for the project.

With the script running and the window open, start playing the bulk playlist from any Spotify client, and use the left and right arrow keys to sort.
