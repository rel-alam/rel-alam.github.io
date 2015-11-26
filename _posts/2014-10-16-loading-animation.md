---
---
Loading from the main menu has finally been completed on having a small of issue of trying to access the player to assign it loaded values before the game started. This caused the null bug to occur as since the player has not yet been created. To fix this, a new game play state is pushed on and then the loading is called. This ensures that the player now exists and we can safely load in the player variables.

The movement code of the player has been changed from and if statement to an else if statement. This allowed movement in only one direction to occur which made the game feel better overall.

Animation class has been updated to include the correct naming for the enum states and to pass in the total amount of frames to correctly state the amount of frames to run.

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
//old code
 
public Animation(Texture2D texture, int a_iRows, int a_iColumns)
{
Texture = texture;
m_iRows = a_iRows;
m_iColumns = a_iColumns;
m_iCurrentFrame = 0;
Animated = animationFrame.Left;
m_iTotalFrames = m_iRows * m_iColumns ;
 
//...
}
 
//new code
 
public Animation(Texture2D texture, int a_iRows, int a_iColumns, int totalFrames)
{
Texture = texture;
m_iRows = a_iRows;
m_iColumns = a_iColumns;
m_iCurrentFrame = 0;
Animated = animationFrame.Left;
m_iTotalFrames = totalFrames;
 
//...
 
}
The old code times the amount of rows by the columns to determine the total amount of frames and its duration of how long it should play for. This resulted in animations for walking and attacking playing for 30 frames where it should of only played for 3 frames. The added argument allows to you to choose to determine how long it will play for.