---
layout: post
title: Barriers, Collisions and Sounds
---
It seems kind of strange that the collision manager already has reference to the barrier class before its shell was even being started. Anyways the barrier is a simple class to create walls in the game that the player cannot pass. It only needed the position to be set within the constructor with the rest done in its inherited class.

The collision manager has been updated to ultlise the new barrier class introducing collisions of the player against barriers. This was a quick and poor way of getting the job done, by timesing the velocity by -1 it worked by stopping the player but quickly introduced loads of new bugs especially with two walls next to each other causing reversal of controls and ability to pass through the wall.

Another check was made into the collision manager which fixed the issue caused by the two barriers next to each other.

Collision manager was updated to now use a list for the enemies and barriers allowing easy checks.

The player class had a small update in which redundant code of setting texture was removed as this is done in the base entity class. The weapons position is now modified with the player’s movement allowing the weapon to appear to the sides, above or below it depending on the last movement.

Another attempt at fixing the music box’s path name issue was conducted but still couldn’t determine what was actually wrong with it. However after a fair bit of time, it turns out I was creating the path completely wrong and now the music box is able to play sound effects as the window’s version of monogame did not like songs being loaded in.