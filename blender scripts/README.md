use these scripts instead of the ones found in the scripts\addons\io_scene_x3d for blender, These ones trim out things which are not used by pokecube, change some default settings to ease up exporting models.

To export from blender, you need to make sure that you select the correct axes for forward and up.

For the entire process of converting a model to x3d, and adding to a resource pack, see below:

Step 0: 
Replace/add the default blender x3d export script and __init__.py with the ones found here

Step 1: 
Import the model to blender.
Make sure that the textures are mapped properly. take note of the name of the texture file Blender is assigning, this will be needed later.

Step 2: 
Split the model into the various body parts, ensure to move their part origins to the correct locations.

Step 3: 
In the gui normally on the right in blender, drag the parts such that they are heiarchially assigned as children of what they should be attached to.

Step 4: 
rename the parts appropriately, make sure each part has texture assigned, textures can also be assigned per material.

Step 5:
Export the model from blender via the script in step 0. make sure that the forward/up axes matches your model.
Make sure to name the model exactly the same as the name of the pokemon, as it is found in the database spreadsheets here: https://github.com/Thutmose/Pokecube/blob/master/Pokecube Core/src/main/resources/assets/pokecube/database/baseStats.csv

Step 6:
Place the model in the resource pack, in assets/pokecube_ml/models/pokemobs.
Place an xml file (same name as model file) in assets/pokecube_ml/models/pokemobs, see any of the other XML files for what needs to be inside it.
Place the textures with the same names as the ones assigned in blender in assets/pokecube_ml/textures/entities.
Place the resource pack in the vanilla minecraft resourcepacks directory. This step is also needed on servers, where you need to make the resourcepacks directory.

Step 7:
Run minecraft, select your resource pack, join world, look for pokemon you just added. If you right click with the modelreloader item, it will bring up a gui for seeing the models, type the name of the pokemon in the lower right text box to skip to it, or use the next/previous buttons to scroll there.
If you use an un-zipped resource pack, you can then edit the x3d model and xml file while in game, then press the F5 button in the modelreloader gui to refresh to any changes you made to the xml/model, This lets you fix/test issues without restarting the game.
