# VictoryPlugin
UE4
# VictoryPlugin
Rama's Victory Blueprint Library

100+ Extra Blueprint Nodes For you!

UE4 Forum Link ~ Victory BP Library Thread ~ https://forums.unrealengine.com/showthread.php?3851-(39)-Rama-s-Extra-Blueprint-Nodes-for-You-as-a-Plugin-No-C-Required!


注释：

Get Controller ID ~ takes in player controller and gives the ULocalPlayer's ControllerID

Get Player State PlayerID ~ returns the replicated unique PlayerID for the supplied Player Controller!

Get Current Operating System Time ~ Retrieve your local current time, milliseconds, seconds, minutes, hours, day, month, year!

Get Time Since Previous Recorded Time ~ Retrieve the difference in time since your chosen previous time! You can record down to the sub-millisecond level, and up to hours!

Get Difference Between Any Two Times ~ With this node you can compare any two times that you've recorded using my node above!

You can store as many moments in time as you want using my above node, the time is recorded as string that I can parse back into actual DateTime struct data!

Get Supported Screen Resolutions for End User's Current Display Adapter
https://forums.unrealengine.com/show...ll=1#post26535

Get Current OS Platform (Win,Mac,Linux,PS4,XboxOne,Android,iOs,HTML5, etc)
https://forums.unrealengine.com/show...ll=1#post59742

Video of my BP Rag Doll System With Follow Camera

Included in these BP nodes is a set of nodes to enable you to activate/deactivate ragdoll any time you want, WITH a built-in follow camera during ragdoll!

Here is a video of exactly what I am providing in these nodes, I used these nodes to make the video.
https://www.youtube.com/watch?v=e-3irWhYzMU


Pictures

Here are some pics of a few of the nodes I am giving you below!

Get Recently Rendered / Not Rendered Actors
https://forums.unrealengine.com/filedata/fetch?id=1134322&d=1504063719

Get Character Bone Current Locations
https://forums.unrealengine.com/filedata/fetch?id=1134318&d=1504063727
Trace for Closest Socket
https://forums.unrealengine.com/filedata/fetch?id=1134319&d=1504063724

Victory Ragdoll System, Including Follow Camera
https://forums.unrealengine.com/filedata/fetch?id=1134320&d=1504063713
Trace Data With Skeletal Mesh
https://forums.unrealengine.com/filedata/fetch?id=1134321&d=1504063721

5 More Pictures, Enjoy!
https://forums.unrealengine.com/show...ll=1#post26153


Current List of Functions (48 Nodes Total)



~~~ Recently Added ~~~


~~~ Frame Rate / Graphics Options ~~~

Set Max Frame Rate

Set Frame Rate To Be Unbound!


4 New Nodes

Max of Float Array

Max of Int Array

Min of Float Array

Min of Int Array

https://forums.unrealengine.com/show...ll=1#post77775

~~~

Get Current Operating System Time
https://forums.unrealengine.com/show...ll=1#post65910

Get Time Since Previous Record Timed
https://forums.unrealengine.com/show...ll=1#post65910

Get Difference Between Any Two Recorded OS Times
https://forums.unrealengine.com/show...ll=1#post65920


Get Supported Screen Resolutions for End User's Current Display Adapter
https://forums.unrealengine.com/show...ll=1#post26535

Combine Strings ~ Combine two strings with optional separator and labels
https://forums.unrealengine.com/show...ll=1#post26535

Clone Static Mesh Actor (during game time)
https://forums.unrealengine.com/show...ll=1#post26262

Teleport Actor to Actor
https://forums.unrealengine.com/show...ll=1#post25769


~~~ File IO ~~~

~ SaveStringTextToFile - Save human-readable text to a file of your choosing.



~~~ ViewPort & Mouse Cursor ~~~

The Set/Get Mouse Position nodes work directly with the player's viewport, and do not require access to the HUD canvas.

~ Set Mouse Position - SET the mouse position to any values of your choosing!
~ Get Mouse Position - Get the current mouse position, will be consistent with results of SET Mouse Position

~ Get Center Of Viewport - Obtain the coordinates of the center of the viewport! Works in PIE as well as standalone game instances

~~~

~~~ Traces ~~~

TraceData - Calculates the Start and End for a new Trace for use with any trace node of your choosing!

~ TraceData Get Trace Data From Character Socket - You pick the rotation, and only need to supply the actor (really a character, but casted internally for your convenience), and a socket name, and a trace length. Optionally you can draw the trace data as a thick 3D line so you can visualize what the actual trace will do

~ TraceData Get TraceData From Skeletal Mesh Socket - You pick the rotation, and only need to supply the Skeletal Mesh Component, a socket name, and a trace length. Optionally you can draw the trace data as a thick 3D line so you can visualize what the actual trace will do


~ Trace For Character Mesh, Closest Bone Pass in just 3 simple variables, Trace Start, Trace End, and the Trace Owner. Get Back: Hit Location, Hit Normal, Name of Closest Bone to the impact, the location of that Bone, and the Actor/Character that was hit.

~ Trace For Character Mesh, Closest Socket: Pass in just 3 simple variables, Trace Start, Trace End, and the Trace Owner. Get Back: Hit Location, Hit Normal, Name of Closest Socket to the impact, the location of that Socket, and the Actor/Character that was hit.


~ Get Character's Mesh Component Retrieve the Mesh component of a character, IsValid let's you know whether the return value is valid or not, so do a branch to check

~ Get Bone Locations Returns an array of all the bone locations on the Character. The Character's Mesh component must be valid for this to work. Returns false if the operation could not occur.


~~~ Closest Point to Source Point Calculation ~~~

~ Closest Point to Source Point : Takes in an array of points and finds which one was closest to the source point. Returns: what the minimum distance was, as well as the vector that was closest to Source.


~~~ Rendering ~~~


~ Freeze Game Render

~ UnFreeze Game Render

~ Game Window is the Foreground window in the OS: - works in PIE and Standalone game instances

You can combine the above to freeze the game render whenever the game window is not the foreground in the OS !

~ Get Array of Currently Rendered Actors - Retrieve array for use with foreach loop, iterating over all currently rendered actors. You can choose what time interval is recent enough, I default to 0.01 seconds.

~ Get Array of Currently NOT Rendered Actors Detailed Info and Pics[/URL]) - Retrieve array for use with foreach loop, iterating over all currently NOT rendered actors. You can choose what time interval is recent enough, I default to 0.01 seconds.


~~~ Aim Offsets ~~~


~ Aim Offsets, For Use With Blend Spaces in probable range of -90,90 to 90,90

~ GetAimOffsets - Original Inspiration for this BP Library, This is a Blueprint version of the same core c++ code as Shootergame uses. With this function you can create a blendspace using 9 animations for the nine directions to create an equivalent of the UE3 Aim Node. You plug the results of this function straight into your Aim Blendspace. See Shootergame example for exact details.

~ GetAimOffsetsFromRotation - Instead of assuming you want to get the character's aim based on the controller, you can use this version to supply the rotation in world space that you want the character to aim to.


~~~ 3D Drawing ~~~


~ Drawing 3D Lines of Chosen Thickness


~ Thick3DLineBetweenActors - Draw a 3D line of your chosen thickness and duration between two Actors! You can use the BP color pick to pick line color!

~ Thick3DLineFromCharacterSocket - Draw a 3D line of your chosen thickness and duration from a specified Character Mesh Socket to your chosen destination. You can use the BP color pick to pick line color!

~ Thick3DLineFromSocket - Same as above, but you can use any mesh of your choosing.


~~~ Misc ~~

~ Get Object/Actor Name As String - Get the name of any actor, component, or anything at all, as a String.

Identify whether game logic is running in Editor,PIE,or Game World!

[B]~ Set Scene Component Mobility

Convenience
~ GetControllerRotation - Get the Character's controller's rotation, fast way to get PlayerController or AIController rotation!

Conversions

~ RotatorToVector
~ VectorToRotator


~~~ Misc 2: Colors and Math ~~~


~ Change Hue

~ Change Saturation

~ Get Float As String With Precision - Get a float as a string with your chosen precision, the re-precisioned float is rounded appropriately. Enjoy!

~ GetSocketLocalTransform - Accessor to this c++ function for your convenience, enjoy


~~~ My Fully Toggle-able Ragdoll Physics System ~~~


Below is the entire graph using my nodes to toggle ragdoll physics mode with the press of a button, while also causing the camera to stay up to date with the position of the ragdoll as it flies around!

See video above!

~ Initialize Victory Rag Doll - you need to have two variables in your blueprint to store the output of this node. Note that you only call this node ONCE. If you call while character is in ragdoll it will not work correctly So I call this at game start with EventReceiveBeginPlay. The output is in relative Character space, not world space so once it is obtained once it is always correct.

~ Is In Rag Doll - Very useful for creating a Rag doll toggle system

~ Enter Rag Doll - The supplied actor is converted to a Character for your convenience, returns false if operation could not occur. Checks whether the character has a physics asset for you.

~ Leave Rag Doll - Here is where you use the output from Initialize Victory Rag Doll to restore the character to proper orientation. This part took me a while to figure out!

~ Update Character Camera - My gift to you, causes the camera to stay up to date with the ragdoll as it moves around, but does so SMOOTHLY. Took me a while to get this just right. You can adjust the interpolation speed / how fast the camera keeps up with the ragdoll. The offset determines how high above the ragdoll the camera tries to stay. 
