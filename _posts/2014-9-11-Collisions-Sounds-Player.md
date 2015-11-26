---
layout: post
title: Collisions, Sounds and Player
---

A collision manager has been made that requires a player, grunt and boss to check the collision against each other and decide what action is needed to take place. This implementation brought in place a check of player vs grunt, player vs boss and what to do when a sword attack from the player in commenced.

If a player walks onto the ground where the boss or grunt is, it will take damage according to what type it is as bosses would hit higher than a grunt. For sword attacks, the manager will check to see if the sword and the enemy is intersecting and if it is to damage the enemy by the sword’s damage.

Music box has been updated to allow the loading of sound effects, the playing of the sound effect and the ability to now stop music that is playing. However the path name still remains a problem and does not currently work.

Players now have an added ability to attack. Although this is still just the skeleton of the attack and does not call any functions when the attack button is pressed.