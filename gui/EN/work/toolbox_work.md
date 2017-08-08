# Labels
You can select what you would like to see as labels in the molecule display. If a particular property is not applicable for a particular atom, there will be no label. To see all the command line options for the labels, type `help labels`.

## Toggle On/Off
This is to display or hide atom or Q-peak labels. It will switch other types of labelling off, but selecting it again will display atom name labels. [F3] does the same thing.

## Atom Names
All atom names of **non-hydrogen atoms** will be displayed next to the atoms. 

`labels -l`

## Crystallographic Occupancy
This displays the crystallographic occupancy of any atoms which are not 100% occupied i.e. their occupancy is not 1. 

`labels -o`

## Chemical Occupancy
Same as above, but the occupancy values for atoms that are located on symmetry elements are not shown.

## Parts
Displays PART numbers for any atoms not in PART 0. 

`labels -p`

## Link Codes
If atoms are linked, the link code will be shown. (FVAR 21/-21 in ShelXL language) 

`labels -lo`

## H Atom Labels
This will include the hydrogen atom labels along with the atom name and Q-peak labels 

`labels -h -l`

## Variables
Displays any atoms where the occupancy is linked to any variable.

## AFIX Commands
This is useful to check the AFIX commands that are being applied to the structure.

## Q-Peak Intensities
Relative intensities of the Q-peaks will be displayed on the structure. 


# Toolbar Model

This is a collection of three basic tools needed for model building.

## Assign Atom Types
All atom types that are currently in your formula are represented as a small button. You can click on one of these buttons and it will go into an atom type assignment mode for this particular atom type. Atoms you click subsequently will become that atom type. Alternatively, you can make a selection of atoms first, and then click the atom type symbol. The buttons will appear red if there are fewer atoms of that type in your model compared to the formula you have initially given. They turn green if the numbers do agree.

`name sel C` (make all selected atoms C)

`mode name C` (clicked atoms will become C)

## Geometrically Place Hydrogen Atoms
Pressing this button will cause Olex2 to place hydrogen atoms geometrically. If there is no selection of atoms, hydrogen atoms will be placed where possible. If there is a selection, they will only be added to the selected atoms.

`hadd`

`hadd 137` (will use specifed AFIX if possible)

## Toggle Isotropic/Anisotropic
With these buttons, you can make atoms either isotropic or anisotropic. If there is no selection this will apply to all atoms; if there is a selection, then this change will only apply to the selection.

`isot`

`anis`

**Note**: If the tickbox is ticked, then refinement will happen automatically after changing either `isot`/`anis` or `hadd`.

# Quicktools 

This is a selection of the tools needed for model building.

## Change Peaks to Carbon
This tool will change all visible electron density peaks to Carbon atoms, regardless of the peak height.

`name $Q C`

## Change Peaks to Hydrogen
All visible Q-peaks will be turned into Hydrogen atoms

`name $Q H`

## Tidy the Structure
Small and geometrically impossible peaks will be removed, all remaining peaks will be turned into Carbon.

`clean`

## Set Formula to what is on screen now
Once the structure on the screen is finished, you can 'synchronise' the formula contained in the files with that on the screen.

`fixUnit`

## Delete all Hydrogen atoms
Deletes all selected Hydrogen atoms from your structure. If no hydrogen atoms are selected, all will be deleted. Undo with `Ctr`+`Z`.

`kill $H`

## Show or Hide Denisty Peaks
Toggle between three states: Show electron density peaks, show them with bonds or hide them.

`showQ`

## Show or Hide Hydrogen Atoms
Toggle between three states: Show Hydrogen atoms, show them with inernal Hydrogen bonds or hide them.

`showH`

## Assemble and Center the Structure
Fragments will be assembled and the structure will be centered on the screen.

`center`

# Part Links 

This is a selection of quick-links regarding displaying of PARTS in your structure.The command-line equivalents are also very useful to know: `showp 0 1 showp` 

The use of the UP key is particularly useful in this context! 

# Split Group 

The tools on this line will fully SPLIT the atom you click next into two atoms.

## No Restraints
This will simply generate two atoms (at the focal points of the ellipsoids) and set the occupancies for each atom to 0.5. One of the atoms will be in PART 1, the other in PART 2. After the splitting has occured, you can move the newly 'generated' atoms to where you would like them to be (by holding the SHIFT key while moving them).

## EADP
This will split the atom as above, but will restrain the ADP values for both atoms to be the same. This is useful early on, and should probably be removed once the disorder model is nearly complete. You might want to apply the DELU restraint instead.

## ISOR 
This will split the atom as above, and reply an ISOR restraint to each of the two atoms.

## SIMU 
As above, but with a SIMU restraint.

# Fit Group 

This tool operates on a selection of atoms, which can consist of any number of atoms. 

## Move or Split One Atom
Select one atom, then select whether you want to fit or split the atom. If you want to fit the atom, you can now move that atom with the left mouse to any position you like by pressing the `shift` key; when you are finished, press the `esc` button.
If you want to split the atom, you will now see **two** atoms, both of which you can move with the left mouse while holding the `shift` key pressed. The occupancies of the two atoms are linked, and the atoms will now belong to different parts. 

## Move or Split Two Atoms
Select two atoms, then select whether you want to fit or split the group. Split will generate a duplicate group, fit will not.
While pressing the `shift` key, you can move the selection as a group. While pressing the `Ctrl` key, you can rotate the group around the midpoint between the two atoms. 

## Move or Split Three or more Atoms
Select three or more atoms, then select whether you want to fit or split the group. Split will generate a duplicate group, fit will not.
While pressing the `shift` key, you can move the entire group. You can now activate any bond around which you wish to rotate the group by right-clicking on it. While pressing the `Ctrl` key, you can rotate the group around this activated bond.
When you are done, press the `Esc` key.

## Split or move with `shift`
This tool can also be used to move any atom (including Hydrogen atoms) to any position. Left click on the atom while pressing the `shift` key - and you can move any atom where you would like it to be. Any constraints and restraints applied to that atom will still apply. **If you click on an atom without holding down the `shift` key, the atom will be split!** So take great care with this tool!
When you are done, press the `Esc` key.

# Electron Density 

The electron density viewer will calculate various electron density maps and allowsthe display of these in a variety of formats. **Please Note**: Close to zero, these maps become very messy (and slow to display). Olex2 therefore does not display these regions.

## Available maps

### diff 
Will calculate the difference map.

### fcalc 
Will display the calculated electron density.

### 2Fo-Fc 
Will calculate the map of 2Fobs-Fcalc.

## Available Source

### olex 
Olex2 will calculate the structure factors.

### fcf 
The structure factors will be read from a ShelXL fcf.

## Command Line
`CalcFourier`

# Peaks and USIO sliders

## Electron Density Peak Slider 
Electron Density Peak Slider Move the slider to the **left** to filter out strongest peaks first, or to the **right** to filter out weakest peaks first. You can then do things like `name $Q C` - and this will only apply to the currently visible peaks. The same goes for the Select and Delete buttons. 

## Uiso Select Slider 
This tool allows the selection of atoms according to their Ueq values.

### Slide to the RIGHT
This will select atoms where the Ueq value is LARGER than the value indicated by the slider. 

`sel atoms where xatom.uiso > 0.06xatom.type!='Q'` 

### Slide to the LEFT
This will select atoms where the Ueq value is SMALLER than the value indicated by the slider. 

`sel atoms where xatom.uiso` 

# Growing 
Olex2 shows the asymmetric unit by default. The tools combinded here in three drop-down boxes are very powerful, and will allow you to 'assemble' your structure in exactly the way you want it to be. In Olex2 you can keep refining your structure without 'destroying' the assembly you have created.

## Grow

### Grow All
All 'missing' connected symmetry equivalent atoms will be generated. 

`grow`

### Shells
This will grow atoms shell-by-shell from the currently displayed image. 

`grow -s`

### Complete
This will generate all missing symmetry equivalent atoms of an already grown structure, independent of whether these are bound to the main fragment or not. In other words: all solvent molecules and counter-ion will be generated according to what is already shown. 

`grow -w`

### Asym. Unit
Removes all symmetry equivalent atoms and displays the asymmetric unit. 

`fuse`

### Complete shown growing bonds
If you are in a growing mode, then clickable growing bonds will be shown. All of these can be grown with this command:

`grow -b`

## Mode Grow
Similar to grow, but now this command will be executed only after you click on an object. When you enter a growing mode, clickable 'growing bonds' will sprout from atoms where the kind of growing you have asked for is applicable. 

`mode grow`

There are various modifiers for this command: 

### Short Contacts
Will show these growable 'bonds' to those atoms where 'short interactions' exist. 

`mode grow -s` 

### Selection
Will show growable 'bonds' to other occurances of the currently selected atoms.

`mode grow -r` 

Van der Waals Radii
Will show growable 'bonds' to other occurances of the currently selected atoms that are at least the indicated distance away from the selected atom. 

`mode grow -v 2.0`

### Move
when you click on growable bonds the symmetry equivalent atom will be moved to the new position. This is really useful when you are trying to assemble a meaningful asymmetric unit for extended structures (polymers). 

`mode grow -a`

### Shells
This will grow atoms shell-by-shell from the currently displayed image. 

`grow -s`

## Assemble
This tool does not strictly belong to the 'growing' family of tools, but it is frequently used together with the growing tools. It allows you to re-arrange the asymmetric unit contents into a different configuration. 

### Broken Fragments
Sometimes, your structure may become 'broken' - parts that should be bonded are shown as separate fragments. This tool will bring them back together. 

`compaq -a`

### Atom-to-Atom
Similar to the 'Broken Fragments' tool, but a different algorithm is used. 

`compaq -c` 

### Metal Last
In this tool, metal ions are taken out of the equation at first (which is very useful when trying to assemble a ligand!) and then the metal ion is placed at the shortest possible distance. 

`compaq -m`

### Q-Peaks
This will move all electron density peaks as closely to existing atoms as possible. 

`compaq -q` 

# Finishing

## Quick Sort
XXX

## Quick Images
XXX