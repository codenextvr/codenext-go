# codenext-go

## Create A New Unity Project

Create a new project, and name it "codenext-go"

<details>
  <summary> Pic </summary>
  <img src="/images/new-project.png">
</details>


### Import the GoogleVR SDK

Go to Assets > Import Package > Custom Package and select the GoogleVRForUnity_1.100.1.unitypackage

<details>
  <summary> Pic </summary>
  <img src="images/import-gvr.png">
</details>

##### Deselect libs folder

Remember to scroll down to "Plugins", and deselect that pesky "libs" folder before clicking Import.

<details>
  <summary> Pic </summary>
  <img src="images/no-lib.png">
</details>

### Set the Target Platform

Cool, now let's tell Unity that we will be building a Virtual Reality app for Android by setting the Target Platform.

* Go to File > Build Settings
* Select "Android"
* Click "Switch Platform"

<details>
  <summary> Pic </summary>
  <img src="images/switch-platform.png">
</details>

### Configure the Player Settings

Now, with the Build Settings window still open, click "Player Settings" and it will pop open.

<details>
  <summary> Pic </summary>
  <img src="images/player-settings.png">
</details>

##### Other Settings

* Click "Other Settings"
* Change the Package Name to "com.YourName.CodeNextGo"
* Change the Minimum API Level to "Android 7.0 'Nougat' (API level 24)" 

<details>
  <summary> Pic </summary>
  <img src="images/other-settings.png">
</details>

##### XR Settings

* Close "Other Settings" and Click "XR Settings"
* Select "Virtual Reality Supported"
* Click the "+" icon to add the "Cardboard" SDK

<details>
  <summary> Pic </summary>
  <img src="images/xr-settings.png">
</details>

## Creating the Ground

##### Add a cube

* Add a Cube GameObject to your scene, and name it "Ground"
* Set the position to x: 0, y: -1, z: 0
* Set the scale to x: 20, y: 1, z: 20

<details>
  <summary> Pic </summary>
  <img src="images/ground-vals.png">
</details>

##### Your Ground should look like this
<details>
  <summary> Pic </summary>
  <img src="images/ground.png">
</details>

## Camera Setup

##### Create an empty GameObject and name it PlayerCamera

<details>
  <summary> Pic </summary>
  <img src="images/create-empty.png">
</details>

##### Drag the Main Camera into this PlayerCamera

<details>
  <summary> Pic </summary>
  <img src="images/player-main.png">
</details>

##### Add a RigidBody component to the PlayerCamera

<details>
  <summary> Pic </summary>
  <img src="images/rigidbody.png">
</details>

##### In the Rigidbody Contraints, Select X, Y, Z for Freeze Rotation

<details>
  <summary> Pic </summary>
  <img src="images/freeze-rotation.png">
</details>

##### Add a Capsule Collider component to the PlayerCamera

<details>
  <summary> Pic </summary>
  <img src="images/capsule-collider.png">
</details>

##### In the Capsule Collider, change the Center - Y value to -0.5
##### In the Capsule Collider, change the Height value to 1.5

<details>
  <summary> Pic </summary>
  <img src="images/capsule-vals.png">
</details>

##### Move the PlayerCamera Y position to 2.28, and Z position to -9.46

<details>
  <summary> Pic </summary>
  <img src="images/move-player-cam.png">
</details>

##### Move the Main Camera X, Y, and Z positions to (0, 0, 0)


<details>
  <summary> Pic </summary>
  <img src="images/move-main-cam.png">
</details>

##### Your PlayerCamera should look like this
<details>
  <summary> Pic </summary>
  <img src="images/capsule.png">
</details>

## Design the Pokeball (with Special Guest - Coach Wolf!)

## Spawn the Pokeball (with Special Guest - Coach Wolf!)

##### Create a folder called "Scripts"

<details>
  <summary> Pic </summary>
  <img src="images/create-folder.png">
</details>

##### Create a C# Script in that Scripts folder called "WalkAndThrow"

<details>
  <summary> Pic </summary>
  <img src="images/walk-and-throw.png">
</details>

##### Open the WalkAndThrow script, and completely empty it

<details>
  <summary> Pic </summary>
  <img src="images/empty-script.png">
</details>

##### Copy and paste the following code into the script

````c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class WalkAndThrow : MonoBehaviour {

	public GameObject pokeball;

	// Use this for initialization
	void Start () {
		
	}
	
	// Update is called once per frame
	void Update () {
		if (Input.GetButtonDown("Fire1")) {
			Instantiate(pokeball);
		}
	}
}
````

##### The WalkAndThrow Script should now look like this

<details>
  <summary> Pic </summary>
  <img src="images/walkthrow-code.png">
</details>

##### Drag the WalkAndThrow Script onto the PlayerCamera. Now, if you click on the PlayerCamera, you will see the Script component at the bottom

<details>
  <summary> Pic </summary>
  <img src="images/walkthrow-playercam.png">
</details>

##### In that Script component, you will see a field named "Pokeball". Drag the Pokeball prefab we created onto this field

<details>
  <summary> Pic </summary>
  <img src="images/pokeball-field.png">
</details>













