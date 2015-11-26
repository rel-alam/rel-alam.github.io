---
layout: post
title: Enum and Animations
---

The animation class now uses an enum to determine which sprite from a sprite sheet it should play.

public enum animationFrame 
{
Back = 0, Left, Right, Forward, unknown, unknown2, unknown3, unknown4, unknown5, unknown6
};
As an enum states are numbered (the first being 0, second is 1 etc) this also easy specification on which part of the sprite sheet that it should be playing from. This allows easy switching between different animations for different characters.

The player class has been fixed and no longer spams the game with button presses but now takes in only a single press if the key is held down.


keyLast = keyCurrent;
 keyCurrent = Keyboard.GetState();
//...
 keyCurrent.IsKeyDown(Keys.L) && keyLast.IsKeyUp(Keys.L)
The above code uses a two keyboard states and compare each state to see if the key that is being pressed was pressed on the previous state

The collision manager also had its timer for the attack removed as the player can no longer spam the attack key.

Once the animation was placed in the speeds at which it was played at plays too fast and a fix is currently not made yet.