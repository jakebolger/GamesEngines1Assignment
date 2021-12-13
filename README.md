# GamesEngines1Assignment

Name: Jake Bolger

Student Number: C18395341

Class Group: TU857

# Description of the Project
The goal for this project was to create a procedurally generated system in Unity. This System comprises of three different Scenes, a start Menu, a procedurally generated nature environemt and a mini game with a procedurally generated terrain as its background. The menu has three options to chose from, Explore, Mini Game, and Quit. The procedurally generated terains are red forest for both the exlpore option and the Mini Game. The Explore scene also has a beach with a procedurally generated Sea.

# Instructions for use
To use this project you must run the Start Menu scene in the Unity Editor, from there you can select and option from the Menu. When you select the Explore button, the game will bring you to the explore scene where you will be brought through a tour of the enviornment getting a look at the forrest and the beach.
Next, to access the Mini Game you will need to select the Mini Game button from the Main Menu. The game will bring you to the mini game where you can use the controls 'W', 'A', 'S', 'D', to move the marble player on the rotating panel. The aim of the game is to try and stay on the panel without gettin knocked off by the Enemy player or touching any of the red obstacles on the panel. If you fall off or touch the obstacles, the player will respawn where you started.

# How it Works
In this section the game mechanics and how the game works will be discussed and explained.
Firstly the Start Menu will be explained. Then, the explore scene will be exaplined along with the pause menu. Finally, the Mini Game Scene will be explained.
when explaininng how each secne works, the methods of creating the scenes will be outlined aswell as how they were coded. The techniques used to write the scripts in C#will be discussed and the different models and assets will be shown and how they were created.

The Main Menu has three different options to choose from 'EXPLORE', 'MINI GAME', and 'QUIT'. The UI for the menu was created by creating a canvas object in the hierarchy, creating a panel, adding a script to the panel, and then adding buttons and text to the Panel. the script that was added to the Main Menu Game Object was a script called 'Main Menu.cs'.

Below is the code use in the MainMenu class to give the buttons functions so they would switch to the required scenes:

![image](https://user-images.githubusercontent.com/55544176/145683479-e0d74862-33bd-4310-9d11-742d95f88fc0.png)

Next Image Shows the Main Menu Screen:

![image](https://user-images.githubusercontent.com/55544176/145683605-f252c2f6-ecdf-43f9-94fc-932ba778726d.png)

The Next Scene is the Explore Scene. This scene consists or a procedurally generated terrain and forest, with a procedurally generated Sea. This scene allows the user to look at the terrain through the main camera. The camera moves on a specific track thorughout the scene to give the user a look at all the terrain. The explore scene has Five Scripts. 'PauseMenu', 'MeshGenerator', 'ForrestGenerator', 'TerrainGeneratorForest' and a 'CameraPath' script.

The 'PauseMenu' Script is attached to the PauseMenu canvas object and it allows the user to pause the game by pressing the ESC button on the keyboard, and select either resume or exit which brings the user back to the main menu. Below is the Code used in the Pause Script and an image of the pause menu. The PauseMenu can be used in the mini game and the Explore scene.

![image](https://user-images.githubusercontent.com/55544176/145684090-03fe36c7-3bfc-423e-9477-e84dbdc89925.png)

![image](https://user-images.githubusercontent.com/55544176/145817887-ed22eae9-a57a-4c5e-861a-fd9e31146d10.png)

The 'MeshGenerator' script us used to generate the Sea using perlin noise. this script was taken from a tutorial and then modified. the gizmos method and coroutine were taken out and the script was modified in other areas to work accordingly.

![image](https://user-images.githubusercontent.com/55544176/145819430-422ea73f-dee4-4a47-92e6-88ad553d7ed8.png)
![image](https://user-images.githubusercontent.com/55544176/145819441-e47aa316-706b-48b7-8b27-e7df1dadc6e3.png)

Image of Sea Below:

![image](https://user-images.githubusercontent.com/55544176/145819674-9839da20-eef6-4c07-a462-bea8ae88db0f.png)

The two main scripts that were used to generate procedural terrain and a forest to go with it were the 'forrestGenerator' and 'TerrainGeneratorForest' scripts. These scripts were used to generate the forests in all the scenes.

A forest game object was created and the 'forrestGenerator script was attached to it. This script allows you to choose the size, element spacing and the different models of trees, rocks or bushes you want to put into your forest. this was done bycreating arrays for the prefabs to go in. Then multiple vector3s were created to randomize the placements of all the prefabs to make the forest look more realistic.

code for size variable, spacing varaible and array for the prefabs to be added to:

![image](https://user-images.githubusercontent.com/55544176/145821614-f8a12918-4f11-4dd9-a0dd-0691dc645a4f.png)

Snippet of rnadomizing the rotation for the vector3 rotation:

![image](https://user-images.githubusercontent.com/55544176/145821713-dc945d38-3295-43fb-9390-6718fbc7f5ef.png)

the TerrainGneratorForest script uses perlin noise to create the terrain. because I have created a forest i needed to make sure that the forest was placed at the correct positions as the terrain. I did this by passing the heightmap array from this script in the forestGnerator script. this means that when the forest generates it generates at the same heights as the proccedural terrain and os not spawned in at a random position.

Snippets of the forrestgenrator scripts using the heightmap array and the tearrinGneratorforest script creating the two dimensional array that the forest script uses to access the heighmap alongside the reference for the forestgenerator script:

![image](https://user-images.githubusercontent.com/55544176/145822617-2ed5de6b-ae95-4344-9588-13ce52093e8f.png)
![image](https://user-images.githubusercontent.com/55544176/145822669-ebb18064-e715-4989-afff-18d59c151855.png)

Forest generated with terrain:
![image](https://user-images.githubusercontent.com/55544176/145822915-cf5e7382-51e4-4fac-b43b-56c50cc7e59e.png)

All the prefabs that were used and put into the elements array were created by creating a tree object and modelling the trees from there. all the mmodelling was done myself. The materials were created by creating a new material and using png images from google images to create the bark materials and the leaf materials.

When creating the trees and the bushes I worked in a separate scene:
Below are the material and models i create aloing with the scene i created it in:

![image](https://user-images.githubusercontent.com/55544176/145823376-224f1960-7479-4079-843b-04002464567d.png)


All models and material for the forest prefabs were put into a separate folder:
![image](https://user-images.githubusercontent.com/55544176/145823754-b5aef7d8-75ff-4aeb-be6b-ec9478c21278.png)


In the Explore scene the CameraPath script was used to create a track for the camera to take. This was done by creating tiny target sphere ojects and using the script to create gizmos from each target to the others. Red lines were drawn to show track route. 

Below is code of the Gizmos function and the track in the scene view:

![image](https://user-images.githubusercontent.com/55544176/145824243-f6ab1cc6-c3d8-45e3-ae4d-ea6736bb65ad.png)
![image](https://user-images.githubusercontent.com/55544176/145824379-53ed54c2-888e-4f55-8736-fa0f895dcf4d.png)




# List of Classes/Assets in the Project and whether they were made yourself or modified or if they are from a Source, with References.
| Scripts and Assets | Source |
| ------------- | ------------- |
| BackgoundAudio Prefab  | Downloaded Audio Source from "Mixkit.com"  |
| Wall Prefabs  | Self made  |
| CameraPath.cs  | Self Written, Used Gizmos Lab for Reference  |
| Pause Menu and prefabs | Self made  |
| PauseMenu.cs  | Followed Tutorial  |
| MainMenu.cs  | Self Written  |
| Mini Game Materials  | Self made  |
| Mini Game Prefabs | Self made  |
| EnemyScript.cs | Self Written  |
| MarbleMove.cs | Self Written  |
| OrbittingScript.cs | Self Written, Used Tutorial for help |
| PlayerSpawn.cs | Self Written  |
| SkyBox Assets | Downloaded from Asset Store |
| TerrainGeneratorForest.cs | Self Written  |
| ForrestGenerator.cs | Self Written  |
| MeshGeneratort.cs | Modified Perlin Noise Script given by Lecturer  |
| All Tree Models | Self Made |
| All Bush Models | Self Made |
| All Grass Models | Self Made |
| Leaves Material | Self Made |
| Bark Material | Self made  |
| Rocks and material | Self Made |
| UI Canvas's for menu's | Self Made |
| Dust Particle system prefab | Downloaded asset |
| River Water Material | Downloaded asset |

All ASSETS NOT lISTED THAT ARE IN UNITY PROJECT, WERE NOT USED IN FINAL BUILD AND WERE NOT USED IN THE ASSIGNMENT.

# References

# What I am most proud of in the Assignment

# Other Information
