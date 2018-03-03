# Bitfab's onboarding tutorial, 3D printing workflow basics


## Skills

* Basic git workflow with Github Desktop
* Basic 3D modelling with FreeCAD
* 3D printing slicing
* 3D printing
* Markdown


## Prerequisites


### Accounts

* Github account.
	* Add user to Bitfab team
* Slack
	* Add user to Bitfab community


### Installed software

* Github Desktop: https://desktop.github.com/
* FreeCAD: https://www.freecadweb.org/
* Cura: https://ultimaker.com/en/products/ultimaker-cura-software
* Text editor, for example, Sublime text: https://www.sublimetext.com/
* Slack mobile app and/or desktop app: https://slack.com/
* Inkscape: https://inkscape.org


## Tutorial


### Creating a new Github issue

* Create a new issue asking for the new tool holder
* Assign it to the operator in training
* A new message will appear in Slack with the new issue (not instantly)
* Clarification: Github issues are not always going to be the entry point of new tasks or jobs, but we need to know how to create one because they are part of the workflow at Bitfab.


### Cloning the repository with Github Desktop

* Go to https://github.com/Bitfab-io/onboarding-tutorial
* Clone repository with Github Desktop
	* Suggested paths: `user/repos/onboarding-tutorial`, `user/repos/Bitfab/onboarding-tutorial`
* Open local repository

If you only need to download the content of the repository and you are not planning on contributing with the changes you can use the option "Download as a ZIP".

![](https://raw.githubusercontent.com/Bitfab-io/onboarding-tutorial/master/media/clone_repo.png)

### Creating a new operator folder

* In your local repository, go to the subdirectory `operators`
* Create a new folder with your name to upload your project

### Designing a new tool holder with FreeCAD

Copy the harvesting tool holder design following the video tutorial: https://www.youtube.com/watch?v=VHa3Fn03R-Q

![](https://github.com/Bitfab-io/onboarding-tutorial/raw/master/media/harvesting_tool_holder.png)

#### Exporting STL file

`.stl` is the file extension most used for exchangind 3D printing models. Is the file that we are going to feed to the slicer software to generate the 3D printing job.

* Open a FreeCAD file
* Open the Mesh Design workbench
* Select the feature you want to export to STL
* Go to `Meshes > Create mesh from shape`
* You can use the default tesellation method or Standard with 0.1mm surface deviation or choose any other. Click OK.
* Select the mesh that has been generated
* Go to `Meshes > Export mesh`
* Choose a name and export the mesh to the directory of your choice.

### Pushing changes to Github

* Open Github Desktop
* Select files that you have changed and want to commit. Try to commit together the same type of changes.
* Write a good commit message title and description.
* Commit changes
* Sync when you want to push changes to the remote repo.


### Slicing


#### Most important slicing parameters

* **Noozle diameter**
	* Choose the nozzle diameter that is installed in the printer.
	* Higher nozzle diameters give faster printing times but lower print quality in the XY plane.
	* Typical values: 0.4mm or 0.8mm nozzles.
* **Layer height**
	* Higher layer heights give faster printing time but lower print quality in the Z axis.
	* Typical values: 0.2mm is the most used value, 0.1 or 0.3mm can also be used.
* **Speed**
	* Higher speeds give faster printing times but lower print quality.
	* Typical values: Between 30 and 60mm/s
* **Temperatures**
	* Nozzle and bed temperatures should be set in the range suitable for the printing material. There are not good reasons for tweaking the temperatures between prints once the best settings have been found. Nevertheless, given a certain material: 
		* Higher nozzle temperatures give easier flow but can result in material degradation, molten plastic oozing out of the noozle and part overheating issues.
		* Higher bed temperatures can provide better first layer adhesion up to a certaing point but can cause overheating issues.
	* PLA typical values: 200-220ºC nozzle, 50-60º bed. PLA can be printed in an unheated bed.
	* PETG typical values: 230-240ºC nozzle, 70-80º bed. PETG cannot be printed in an unheated bed.
	* Other materials: check manufacturer information or determine experimentally.
* **Retraction**
	* Retraction lengths and speeds depend on the extrusion system:
		* Bowden setups require longer retraction lengths than direct drive setups (several millimiters).
		* PTFE hotends accept longer retraction lengths than all metal hotends (several millimiters vs about one millimiter or less).
		* Retraction speed can be set high as long as the extruder can keep up with the work (40mm/s and up).


#### Configuring a slicing profile from scratch

* Make a new slicing profile from a stock profile in the slicer


#### Downloading the default profiles

We don't have a repo yet with the default profiles.

## Sending a job to the priter

* SD card
* Octoprint

### Documenting the print

* Markdown
* Technical drawings
* Exploded views or assemblies? Maybe with the slot and tools
* Photo of the print
* Documenting in 2D with Inkscape

### Closing the issue

* Close the Github issue



## Additional resources

* Obijuan tutorials
	* [Github + FreeCAD](https://www.youtube.com/watch?v=7JCSnGJ5kkk&list=PLmnz0JqIMEzXThALT6gTUH1rlW1gS-GzU)
	* [FreeCAD season 1](https://www.youtube.com/watch?v=2_DbFzFV9D4&list=PLmnz0JqIMEzWQV-3ce9tVB_LFH9a91YHf)
	* [FreeCAD season 2](https://www.youtube.com/watch?v=tvevj-esu_E&list=PLmnz0JqIMEzUqEM-nxqhZoDaqszVXijOb)


