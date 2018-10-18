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
