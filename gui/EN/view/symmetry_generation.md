# Symmetry Tools
This tool tab features a set of buttons for changing the appearance/location of the asymmetric unit; expanding ('growing') a structure on the screen; viewing the basis vectors and unit cell; and other similar tasks.

# symmetry tools 1
The tools in this row are useful for re-organising parts of a structure if the structure contains more than one moiety.

## Move Near
This is useful for moving moieties of a structure close to a particular atom of interest.
<br>
<br>

  1. Click on an atom near which another moiety is to be moved.
  2. Activate the mode by clicking on the **Move Near** button (or typing '<c>mode move</c>').
  3. Click on an atom of each moiety that is to be moved close to the initially selected atom.

|`mode move`| |

## Copy Near
This is a slightly different method for collecting moieties of a structure close to a particular atom of interest.
<br>
<br>

  1. Click on an atom near which another moiety is to be copied.
  2. Activate the mode by clicking on the **Copy Near** button (or typing '<c>mode move -c</c>').
  3. Click on an atom of each moiety that is to be copied close to the initially selected atom.

|`mode move -c`| |

## Assemble

|`compaq`| This command brings the various fragments of a structure as close together as possible on the screen. |

|`compaq -a`| Brings fragments of a structure together as above, but also assembles any 'broken' fragments. |

# symmetry tools 2
Tools in this row will achieve centering of the moieties in a stucture.

## Centre on Cell


|`move`| All moieties in the structure will be centred on the cell.|

## Centre on Largest Part

|`move`| All moieties in the structure will be centred on the largest moiety.|
# symmetry tools 3
These tool switch symmetry related items on the screen on and off.

## Show Basis

|`basis`|Displays/Hides the basis vectors of this structure.|

## Show Cell

|`cell`|Displays/Hides a drawing of the unit cell.|

## Quality

|`qual -l` , `qual -m` , `qual -h`|Changes the quality setting in which atoms are drawn. A lower quality can be useful if the computer struggles with larger structures.|

# symmetry tools 4

## Fuse


|`fuse`|Display the asymmetric unit of the structure only. All symmetry generated atoms will be removed.|

## Grow All


|`grow`|All symmetry equivalent atoms that are required to show the 'complete' structure will be generated. Of course, in the case of polymeric structures, this is somewhat arbitrary, and more controlled growing conditions will need to be employed.|

# Growing
Olex2 shows the asymmetric unit by default. The tools combined here in three drop-down boxes are very powerful, and will allow you to 'assemble' your structure in exactly the way you want it to be. In Olex2 you can keep refining your structure without 'destroying' the assembly you have created.

## Grow

### Grow All

|`grow`|All 'missing' connected symmetry equivalent atoms will be generated.|

### Shells
|`grow -s`|This will grow atoms shell-by-shell from the currently displayed image.|

### Complete
|`grow -w`|This will generate all missing symmetry equivalent atoms of an already grown structure, independent of whether these are bound to the main fragment or not. In other words: all solvent molecules and counter-ion will be generated according to what is already shown.|

### Asym. Unit
|`fuse`|Removes all symmetry equivalent atoms and displays the asymmetric unit.|

### Complete shown growing bonds
|`grow -b`|If you are in a growing mode, then clickable growing bonds will be shown. All of these can be grown|

# Mode Grow
|`mode grow`|Similar to grow, but now this command will be executed only after you click on an object. When you enter a growing mode, clickable 'growing bonds' will sprout from atoms where the kind of growing you have asked for is applicable.|

There are various modifiers for this command:

### Short Contacts
|`mode grow -s`|Will show these growable 'bonds' to those atoms where 'short interactions' exist.

### Selection
|`mode grow -r`|Will show growable 'bonds' to other occurances of the currently selected atoms.|


###Van der Waals Radii
|`mode grow -v 2.0`|Will show growable 'bonds' to other occurances of the currently selected atoms that are at least the indicated distance away from the selected atom.|


### Move
|`mode grow -a`|when you click on growable bonds the symmetry equivalent atom will be moved to the new position. This is really useful when you are trying to assemble a meaningful asymmetric unit for extended structures (polymers).|


### Shells
|`grow -s`|This will grow atoms shell-by-shell from the currently displayed image.|

## Assemble
This tool does not strictly belong to the 'growing' family of tools, but it is frequently used together with the growing tools. It allows you to re-arrange the asymmetric unit contents into a different configuration.

### Broken Fragments
|`compaq -a`|Sometimes, your structure may become 'broken' - parts that should be bonded are shown as separate fragments. This tool will bring them back together.|

### Atom-to-Atom
|`compaq -c`|Similar to the 'Broken Fragments' tool, but a different algorithm is used.|

### Metal Last
|`compaq -m`|In this tool, metal ions are taken out of the equation at first (which is very useful when trying to assemble a ligand!) and then the metal ion is placed at the shortest possible distance.|


### Q-Peaks
|`compaq -q`|This will move all electron density peaks as closely to existing atoms as possible.|


# Packing
Packing options to display the packing of your structure.

## Pack Close Contact
Use the slider bar to set the distance from atoms that you want clickable growing options to be displayed.

## Pack Radius
Move the slider to adjust the radius around the original molecule where symmetry equivalent molecules should be shown.

## Pack to limits

### Pack to limit
Packs the structure within the limits defined for a, b and c.

### Fill Unit Cell
Displays all atoms within the unit cell.

### Complete Fragments
Completes any fragments that are only partially displayed as a result of the various packing options.
