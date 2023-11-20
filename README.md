# AudioVisual-Cues_Pack
This package is made for Unity with the sole purpose of providing other Unity developers an easy tool for implementing visual cues for audio that plays, which is a great accessibility feature for deaf players.

What's in It:
The AudioVisual Cues Dynamic Plug-In package allows you to have live-reacting image cues for audio sources inside your Unity project. 
You can generate the sound controller into your scene, assign the main canvas, camera, image cues, and audio sources, and it’ll start working right away.

Creating Sound Controller:
You can generate a sound controller via Unity Editor.
1.	After you import this package into your project you’ll find a new menu item: “GameObject > AudioVisual Cues > Generate Sound Controller” in the editor
2.	When you click “Generate Sound Controller” option, a wizard will popup created by GenerateSoundController.cs script
3.	After you click “Create” button, a new gameobject will be created at the origin with a SoundController component. By default, “SoundController” script will be attached to this gameobject
4.  After you create the sound controller, assign the camera, canvas, and assign the image for the audio source
(should have an audio clip that plays On Awake), hit play and you should be able to see the image drawn on the screen at the location of the audio source.
5.	You can assign multiple mixer groups and as many audio sources as you want. The screen can look something like this using the script to that effect.

Definitions:
Object Name (Optional): The name of the gameobject that will be created. If this option is left empty, by default the gameobject’s name will be set to “SoundController” and will appear as such in the Hierarchy.
Main Camera: What the sound controller will use to determine where the image cues will appear on screen when moving around. (note: you will new multiple SoundController gameobjects if you want to use more than one camera)
Main Canvas: What the sound controller will use to draw images cues on and move them around. (note: you will new multiple SoundController gameobjects if you want to draw on more than one canvas)
Enable Controller: Determines if the script will run. If disabled, images will be cleared from the canvas and will cease running.
Mixer Groups Data: Audio settings that will be associated with a specific mixer group. If an audio source shares the same mixer group as one inside Mixer Groups Data, it will assign those settings to it (unless it’s overridden).
Enable Setting: Determines whether that specific Audio Setting will be represented on the canvas. When disabled, images will be erased from the canvas
Name: The name for the Audio Setting. It doesn’t really affect anything, but is convenient when referencing an Audio Setting inside code. (If left blank, it will use the name of the clip
Audio Source: What all functions will be based from. Sounds that play through the audio source
Mixer Group: Gets assigned automatically from the audio source.
Use Mixer Group Data: Determines whether the audio setting will use values from Mixer Group Data.
Image: The image the sound controller will use to draw on the canvas, representing the audio source.
Offset: Moves the target location to draw image cue from
Min Opacity: The minimum opacity the image will be drawn to. (ranges from 0 to 1)
Max Opacity: The maximum opacity the image will be drawn to. (ranges from 0 to 1)
RMS Multiplier: The sensitivity of the volume detection. Higher the value, the higher the decibel value created.
Max Size: The maximum image size drawn on the canvas.
Min Size: The minimum image size drawn on the canvas.
Calculate Opacity Based On Distance: Changes the opacity to change based on the distance from the audio listener.
Calculate Image Size Based On Volume: Changes the image size to change based on the volume coming from the audio source.
M Overrides: When checked, the value will override the one associated with Mixer Group Data.
