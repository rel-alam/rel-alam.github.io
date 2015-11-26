---
layout: post
title: Saving and Loading
---
The player class now has four new textures added to it for the front, back and side images which changes to the correct image depending the last way the player moved. Attack has also been given a counter to stop spam hitting and slowing it down to a more reasonable speed. A new check for the player’s alive state has been added to set to false when the health reaches 0 or less.

Collision manager has now been modified to directly push lists into it instead of having to create a constructor that does it. This allows the manager to be used anywhere it needs as the list of the objects can be pushed in from a different class.

A file manager(saving/loading) has been added but currently breaks as an attempt to use serialisation led to failure. Serialisation is not possible as the player class needs to be serialise which results in the class it inherits also needs to be serialised as well. However the base entity inherits GameComponment a class built into XNA which cannot be serialised. This inheriting to save a few lines of code to update the objects has led to a bigger difficulty that is not easily recoverable. This means I need to save out the individual properties within the player class to get a correctly saved class.