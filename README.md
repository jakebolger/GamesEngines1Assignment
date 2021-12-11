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

The Next Scene is the Explore Scene. this scene consists or a procedurally generated terrain and forest, with a procedurally generated Sea. This scene allows the user to look at the terrain through the main camera. the camera moves on a specific track thorughout the scene to give the user a look at all the terrain. The explore scene has Five Scripts. 'PauseMenu', 'MeshGenerator', 'ForrestGenerator', 'TerrainGeneratorForest' and a 'CameraPath' script.

The 'PauseMenu' Script is aattached to the PauseMenu canvas object and it allows the user to pause the game by pressing the ESC button on the keyboard, and select either resume or exit which brings the user back to the main menu. Below is the Code used in the Pause Script.

![image](https://user-images.githubusercontent.com/55544176/145684059-c52b59da-e518-41f5-8f18-aa0df1e783e8.png)


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
