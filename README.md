Versus Saxton Hale
==================

The predecessor to [Freak Fortress](https://github.com/50DKP/FF2-Official).

### Installing
- Copy the `addons` folder to the server's `tf/` folder.  
- The `scripting` folder within is unnecessary unless you are a modifying the gamemode.  

### Updating
- Make sure you are updated to Sourcemod 1.6.3 or greater. v1.50+ is now incompatible with older versions.  
- Generally, with Team Fortress 2, Valve updates say you almost always have to use the latest [SM snapshots](http://www.sourcemod.net/snapshots.php) anyway.  

Also be sure to install [TF2Attributes](https://forums.alliedmods.net/showthread.php?t=210221).

TF2Attributes is used for Hale's anchor ability and for giving mantreads their increased jump height.  
It will be used automatically if VSH detects the plugin. VSH no longer has to be recompiled to change this.  

Look through the folders inside the `addons/sourcemod/` folder.

The folders necessary to be updated or checked are:
* `plugins/`
* `translations/`
* `configs/saxton_hale/saxton_spawn_teleport.cfg`
* `tf/models/player/` - Added new Saxton Hale and Vagineer models.
* `tf/materials/models/player/` - Added new materials for the new Saxton Hale model.

configs/, scripting/, don't require updating. However, if you're updating from v1.53 specifically you will need to update `tf/cfg/sourcemod/SaxtonHale.cfg` for updated Goomba Stomp integration.

You should never really update configs or scripting if you've changed them, as you'd be reverting them to defaults anyway, with the exception of when new CVARs are added or old ones are removed (not very common).

The following files are no longer needed and can be deleted:
* `gamedata/equipwearable.txt`
* `gamedata/saxtonhale.txt`

### To disable the Easter Bunny
Find the line `#define EASTER_BUNNY_ON` in `saxtonhale.sp`, put a ```//``` in front of the ```#define```, and recompile the plugin using include files from a recent snapshot of [SourceMod](http://www.sourcemod.net).

### To restore legacy Mediguns
'Legacy Mediguns' being Medics granted a custom Kritzkrieg instead of overriding all Medigun attributes.
Find the line `#define OVERRIDE_MEDIGUNS_ON` in `saxtonhale.sp`, put a ```//``` in front of the ```#define```, and recompile the plugin using include files from a recent snapshot of [SourceMod](http://www.sourcemod.net).

Remember: TF2Items, Sourcemod 1.6.3 or higher, and morecolors.inc are **required** to be able to compile it.

If you use them, the Steamtools, TF2Attributes, RTD, and Goomba includes must also be used.
Not including any of these in the compilation will completely disable their features, even if you have those plugins running.
