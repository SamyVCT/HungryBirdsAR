This project aims to recreate some simple functionalities of the game Angry Birds in augmented reality.

I used Unity 2021.3.19.f1. The project is based on AR Foundation 4.2, in which I have created some assets and added some code.

It was tested on a OnePlus 8T with Android 13. After multiple tests on different devices, it seems that ARCore (which is a Google Play service used for augmented reality) is not supported everywhere: "requires a minimum SDK version of 24" (Android 7.0 Nougat). And some brands (Fairphone) don't support it at all, regardless of the Android version.

---------- What I added --------------------
I merged 2 projects: Simple Occlusion in the scene Depth and Feathered Plane in the scene Plane Detection (just added the Plane Detection scene's components to the Depth scene's camera).
I used 2 scripts, "AR Anchor Manager" and "AR Place Hologram", to make a prefab appear and be bound to the physical object detected (a plane in our case). Here is the Github repository to make it: https://github.com/andijakl/AR-Foundation-Demo
I added a script, "destroyOnCollision", to play a sound when a burger is hit and make it disappear.
Finally, I coded a very simple user interface with 3 buttons (description below).

---------- How to modify the game ----------
The game is in the 'Simple Occlusion' scene.
Make your modifications, then go to File -> Build Settings -> drag and drop the scene -> select your platform -> build.

---------- How to play the game ------------
When you launch the APK on your device:
- Face a horizontal plane (table, ground) at about 1.5 meters. When the plane is detected, it is displayed in dots.
- Click on the button "Ajouter structures" and click on the detected plane.
- A structure should appear. You can move around.
- Click on "Lancer oiseaux". Tap anywhere on the screen to launch birds.
- The "reset" button deletes everything in the scene.
