---
layout: post
title: Missing Title
---
Collisions have been greatly modified today to use  a single entity manager instead of four different objects. The new entity manager allows the collision to now reference towards that object where it stores the different entities giving an easy approach for the collision manager. The jittering bug when colliding with a wall has been fixed. It is accomplished by taking the player’s movement forward and minus it by the same amount when it hits a wall effectively not allowing it to move.

The player class has been updated to save and load using the p and o key respectively as well as controlling the updating and drawing of the weapon to the screen.