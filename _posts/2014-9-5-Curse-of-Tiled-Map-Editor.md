---
layout: post
title: Curse of Tiled Map Editor
---

After two days of deciding on how the map is going to be created within the game, 
it was opted to choose Tiled Map Editor a simple easy to 
use tile based map design tool that works by 
inputting your own image in a tiled set and loading it through the program.

Attempts to implement the functions to correctly load in 
the tmx file format (similar to XML) were hit by hard brick walls stopping the progress. 
The way in which the tmx file was laid out caused a fair bit of issues trying to figure 
out how to load in the file. This lead to almost a success but instead turns out I was 
just loading the texture tile set instead of the correct individual tiles.

Much needed anger and frustration was brought about until further research led me to a 
github post that contained the source code on loading in the tmx file. This had allowed 
me to see that reading in the file was a lot harder than I actually thought.

My next step was to implement the player class and to also create a music box to play 
songs and sound effects.

The player class was created with the basic functions required to get it created and 
moving around on the screen. The player class was created with the ability of having 
health, inventory, velocity, score and a weapon. Movement of the class was made triggering up, 
down, left or right to move the player around in the correct way.

The frustration of the day has not been completed yet when faced with a content cannot be 
found when trying to load in a song, in which the directory the error is showing appears to be fine.
 This turned out to be I was accidentally creating the path wrong even though it seemed right.