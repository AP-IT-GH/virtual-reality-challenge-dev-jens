# 3D painting challenge - Baeten Jens

oplossing VR challenge 2

# Getting Started
## Open the broken 3D painting prototype Scene:
 - From the Project window, expand, Assets > Challenges 02_3DPainting > Scenes
 - Double-click on the 3DPainting_Prototype_Broken Scene to open it.

# Challenge tasks
### 1.  The Canvas that allows you to change the shape on the pedestal follows the camera.
- de canvas_pedestal stond in screen space mode dit word dan altijd op het scherm getoont door de render mode aan te passen naar world space krijgt de canvas een plek in de wereld
<br><br>
### 2.  The toggled ray and palette canvas are tracking the opposite hands.
- De input refrences van Lefthand en RighRay waren omgedraaid. Door deze de juiste referentie te geven is het probleem opgelost.
<br><br>
### 3.  The paint brush activation is backwards, starting when the trigger is released and stopping when it’s pressed.
- Bij het grab interactble paintbrush object zijn de events van "On Activate" en "On Deactivate" omgedraaid. Bij het "On Activate" event stond er CreateTrail.EndTrail terwijl dit .StartTrail moest zijn en dit visa versa bij de "On Deactivate".
<br><br>
### 4.  The medium brush size button turns invisible when pressed and makes the trail gigantic.
- Onder XR Rig > LeftHand > Canvas_Pallette > Button_Size heb ik de Button_medium de zelfe pressed color gegven als de andere 2 knoppen omdat als je voor deze verndering op de knop duwde verdween hij. Ook heb ik bij het On Click event de width van de trail verlaagd van 0.25 naar 0.03 zodat dit mooi in het midden ligt van de 2 andere knoppen
<br><br>
### 5.  The paint brush sound effect stays the same, regardless of how far it is from you.
- Door de de audio source te verlagen van een minimale afstand van 0.1 en een maximale afstand 1