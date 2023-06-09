# PURE-test
 research project for hololens 2. Supervised by Kürşat Çağıltay for an undergraduate research project in Sabanci University.
 
 The current iteration of the project is a replication study of the following paper: [Impact of Task on Attentional Tunneling in Handheld Augmented Reality](https://dl.acm.org/doi/abs/10.1145/3411764.3445580) by Brandon V. Syiem, Ryan M. Kelly, Jorge Goncalves, Eduardo Velloso, Tilman Dingler 

## Setup
 The unity project must have MRTK set up. The installation wizard can be found [here](https://learn.microsoft.com/en-us/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool).

 Under MRFT packages, download the following:
* mixed reality toolkit -> mixed reality toolkit foundations
* platform support -> mixed reality OpenXR plugin

 Build platform must be set to UWP. ARM64 architecture must be chosen.
 
 This project utilizes URP in order to render the bloom effects on the hololens. Please make sure your project is set up with URP
 
 
 ## How to use the program
This part assumes that you were able to successfully export and run the program on your HoloLens.

When the program starts, there should be an interactable sphere rougly 1 meter in front of you. This sphere can be *dragged* and *rotated* but it cannot be scaled. Move this sphere to the desired surface (for our purposes, we attached it to a wall).

Along with this interactable sphere, there should be 4 more visible gray spheres around the object, roughly 0.5 meters above and below it, and roughly 1 meter to the sides (to the corners of these dimentions, if you visualize a rectangle with these dimentions). When the interactable sphere is moved, these spheres should also move along with it. Rotate the interactable sphere as desired so that these spheres are in their intended positions.

When the scene is set, go back to where you were at the start of the program, there should be a floating button labeled "lock in" to your right. By pressing this button, the interactable sphere will disappear and the LED's will start blinking randomly. The following is the logic controlling the LED's:

* A random LED is chosen
* The program ranomly determines to either light a physical light or a virtual light
* the random LED lights up for 1 second
* when the LED turns off, the program waits for 3-5 seconds, and then starts over again.

under `User Files\LocalAppData[APP name]\LocalState\[file name]`, the program will create a log of all actions taken so far.
under `User Folders\Music\MRTK_ET_Demo\tester\[timestamped file]_test\test`, the program will create a log of eye-tracking data collected so far.

When the scene is locked in, eye-tracking data will start being collected. To save the data to a file, you must press the button again.

# Contact Infromation
* Supervisor: [Kürşat Çağıltay](github.com/cagiltay) (kursat.cagiltay@sabanciuniv.edu)
* Kutluhan Aygüzel (kutluhan@sabanciuniv.edu)
* İlayda Efsane Algın (aefsane@sabanciuniv.edu)
* [Bilgehan Çağıltay](github.com/DivinorWieldor) (bcagiltay@sabanciuniv.edu)
* Bilge Kaan Yıldırım (bilge.yildirim@sabanciuniv.edu)
