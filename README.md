# Python Animation Import / Export tool for Autodesk Maya



## What PAIE can do for you
PAIE (Python Attribute Import/Export) is a Maya based animation transfer tool which lets you save out animation or poses to a file and import them again onto same or similar characters/object allowing you to transfer animation freely and share between colleagues

## How to install it
To use the tool, place "paie.py" somewhere in your PYTHONPATH, eg: "../[username]/maya/2011-x64/scripts" or similar.

Restart maya and run PAIE by typing:
    "import paie;paie.GUI()"
in a python commandLine/scriptEditor

## How you can use it
PAIE works on your current selection and will export data from such and import by matching to the original names unless you import based on selection order.
Data is saved by writing a file in PAIEs own filetype called ".xad" where all attribute values are stored.

## The Interface
The consists of a top row with a switch between an import and an export mode, a refresh button to refresh the filelist, an 'add tab' and 'remove tab' button which enables you to have several tabs pointing to each of their directories so you kan have eg. one tab pointing to face poses, another to hand poses, another to your local animation library and then maybe one pointing to a global library where you can share poses/animation with fellow artists.

### Export Mode:

When exporting using the GUI you need to select the objects you want to export, either set your active timeline according to what animation you would like to export or uncheck 'timeline only' to export all animation on objects.
All namespaces within the selection will be exported and only unique object-naming is allowed.

### Import Mode:

Importing a file works on your current selection as well imports either to your current frame or at the animations original frame position depending on the 'Apply at Origin' checkbox.
Select the file you want to import from, select the namespace you want to use (Note: You can only import from 1 namespace and onto 1 namespace at a time)
When you import a file PAIE will by default match your import data names to your current selection and only add animation to objects that have the same name as the source (namespaces excluded). This enables you to easily import data form one rig to another rig having two different namespaces but the same naming. You can also choose to import your data according to selection order by checking the 'select order' check box. This will make PAIE consider the order in which you selected the initial objects when exporting and apply data to your current selection in the same way, disregarding naming.

## Development and License
PAIE was initially developed for Radar Film & Disco worms Aps and is published as open source under the LGPL.
Feel free to contribute



## Known Bugs:
- None atm.


## Update Log
#####  13-04-2012: v1.3.3 by Jakob Welner
- Cleaned up old hacks, browse dialog/mel callback
- Removed mel Callback hack as the Undo bug forcing it has been fixed. Don't know when tho.

#####  21-01-2012: v1.3.2 by Jakob Welner
- Fixed some OSX bugs
- Streamlined OS dependent operations

#####  01-04-2011: v1.3.1 by Jakob Welner
- changed PAIE title to correct version
- fixed a slight issue with selection after deleting files

#####  30-03-2011: v1.3.0 by Jakob Welner
- fixed browse-button for both windows and linux
- new Export All Animation and Import to original position
- fixed error on deleting files in export mode
- fixed some GUI issues
- fixed infinity again?
- added OMT header for menu support with OMToolbox (first 4 lines)
- supporting boolean attrs - didn't know that this wasn't working
- returns instance on initiating GUI, in case anyone wanna use it?
- including stack trace in error msgs
- sorting file lists alphabetically
- on Import prompting whether to change rotation order according to source
- Prints out affected controls to the script editor

#####  11-09-2008: v1.2.0 by Jakob Welner
- import now only matches to obj name - not path - and only accepts unique naming
- undo when importing has been fixed - was a bitch so you'd better be glad
- errors are now more obvious on a popup window instead of the response line
- updated file structure - NOT BACKWARD COMPATIBLE!!
- listed framerate now actually works and is reliable
- pose imports now only checks current frame for existing keys that will be overwritten
- importing onto locked and hidden attributes no longer fails
- the normal minor updates here and there
- more stable GUI on linux

#####  04-04-2008: v1.1.2 by Jakob Welner
- minor refinements
- fixed some linux issues: ProgressHandler missing 'next()' method
- fixed infinity transfer on namespaced objects
- minor change in UI - replaced export 'pose only' with radioButtons (animation/pose)

#####  02-04-2008: v1.1.1 by Jakob Welner
- fixed some stuff when handling paths with restricted permissions

#####  02-04-2008: v1.1.0 by Jakob Welner
- enabled deleting files from list using the delete key
- autoselect namespace if there is only one
- fixed tangentType transfer
- fixed some warning messages
- fixed inifinity transfer

#####  27-03-2008: v1.0.0 by Jakob Welner
- Initial release
