---
layout: post
title: Creative Title
---
Today brings a new class to our project, the Animation class. The class currently takes in a sprite sheet image and define the amount of rows and columns within the image. This allows the Animation class to read though the correct amount “images” that is within the image. Within the update function it increments the frames by one until it hits the max frames and restarts back at the first frame showing an animated effect.

The music box has been updated once again this time to support PSM loading of song files as it works fine for the PSM and now has the correct #if checks to make sure the correct code is being ran.

The collision class has #if checks added for debug mode to print console lines only in debug mode.