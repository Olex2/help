# toolbox work-target
A collection of useful tools
- Make all peaks Carbon
- Move Atoms
- Show/Hide Peaks
- Expand Short Contacts
- Peak Slider
- Disorder Tools


# Labels
It is possible to customise the labels in the model display. If a particular property is not applicable to any atom, there will be no label, e.g., if 'labels -o' (see below) is typed and all atoms have occupancy 1, no atoms will be labelled.

|`help labels`| To see all options for the 'labels' command. |

## Labels OFF/ON
This is to display or hide atom or Q-peak labels. It will switch other types of labelling off, but selecting it again will display atom name labels. [F3] does the same thing.

## Atom Names
|`labels -l`| All atom names of **non-hydrogen atoms** will be displayed next to the atoms. |

## Crystallographic Occupancy
|`labels -o`| This displays the crystallographic occupancy of any atoms which are not 100% occupied i.e. their occupancy is not 1. |

## Chemical Occupancy
|`labels -co`| Displays the 'chemical occupancy' on the labels. Basically, the occupancy values for atoms that are located on symmetry elements are not shown. |

## Parts
|`labels -p`| Displays PART numbers for any atoms not in PART 0. |

## Link Code
|`labels -lo`| If atoms are linked, the link code will be shown (FVAR 21/-21 in ShelXL language). |

## H Atom Labels
| `labels -h -l` | This will include the hydrogen atom labels along with the atom name and Q-peak labels. |

## Fixed Parameters
| `labels -f` | Labels atoms with fixed occupancy. |

## Variables
| `labels -v` | Displays any atoms where the occupancy is linked to any variable. |

## AFIX Commands
| `labels -a -h` | This is useful to check the AFIX commands that are being applied to the structure. |

## Q-Peak Intensities
| `labels -qi` | Relative intensities of the Q-peaks will be displayed on the structure. |

## Ueq
| `labels -u` | Labels atoms with their Ueq values. |

## Label + residue rumber
| `labels -l -rn` | Displays both atom label and residue number. |

## Residue Numbers
| `labels -rn` | Show the residue number to which an atom belongs. |

## Residue Class
| `labels -rc` | Show the residue class to which an atom belongs. |


# Toolbar Model
This is a collection of three basic tools needed for model building.

## Assign Atom Types
Each element currently in the formula is represented by a small button.

### Using the GUI
|$spy.MakeElementButtonsFromFormula('mode')|All atoms present in the model are shown. The '...' button opens the Periodic Table if more elements need to be added.|

Clicking on an element button launches the atom type assignment mode for this particular element. Any atoms clicked subsequently become that element. Pressing the 'ESC' key exits the mode. Alternatively, selecting atoms first and then clicking an element button turns them all into that element. The buttons will be red or blue if there is a mismatch between the number of atoms of that element in your model and those in the chemical formula. They turn green if the numbers agree.

### Using the Command Line
It is usually much more efficient to assign elements using the keyboard. Here are three frequently used commands:

|`name sel C` | Turns all selected atoms to carbons. |
|`mode name C` | Enter atom naming mode; once in the mode, all atoms clicked will turn to carbons. |
|`name \$Q C` | Turns all Q peaks to carbons. |

## Geometrically Place Hydrogen Atoms
Clicking this button will cause Olex2 to place hydrogen atoms geometrically on any selected atom(s). If no atoms are selected, hydrogens will be placed on all possible atoms, to complete the structure.

|`hadd`| Adds hydrogen atoms to selected atoms (or to all atoms, if none are selected). |
|`hadd 137`| Will use specifed AFIX **if possible**. (137 adds three hydrogen atoms to a methyl group, for example.) |
|`hadd -137`| If the connectivity does not allow the addition of the specified AFIX atoms, it is still possible to place them in this way. Two atoms must be selected to define a vector, with the atom to which hydrogen atoms are to be added selected *first*. |

## Toggle Isotropic/Anisotropic
These buttons make the selected atoms either isotropic (sphere button) or anisotropic (ellipsoid button). If no atoms are selected, this change will be applied to all atoms.

|`isot`| All selected atoms will be refined **isotropically**. |
|`anis`| All selected atoms will be refined **anisotropically** (ellipsoids will result). |

Note: If the tickbox is ticked, then refinement will occur automatically after clicking either **isot**, **anis** or **hadd**.


# Quicktools
This is a further selection of tools useful for model building.

## Change type and display of atoms
|`name \$Q C`| $spy.MakeHoverButton('toolbar-QC','name \$Q C') | This tool will change all displayed electron density peaks (Q peaks) to carbon atoms, regardless of the peak height. |

|`name \$Q H`| $spy.MakeHoverButton('toolbar-QH','name \$Q H') | All visible Q peaks will be changed to hydrogens. |

|`clean`| $spy.MakeHoverButton('toolbar-tidy','clean') | Tidy the Structure: small and geometrically impossible peaks will be removed; all remaining peaks will be changed to carbons. |

|`kill \$H`| $spy.MakeHoverButton('toolbar-killH','kill \$H')  | Deletes all selected hydrogen atoms from the structure. If no hydrogen atoms are selected, all will be deleted. Undo with **CTRL+Z**. |

|`showQ`| $spy.MakeHoverButton('toolbar-Q','showQ') | **CTRL+Q**. Toggle among three states: show electron density peaks, show them with bonds to nearby atoms, or hide them. |

|`showH`| $spy.MakeHoverButton('toolbar-H','showH') | **CTRL+H**. Toggle among three states: show H atoms, show them with H-bonds or hide them. Hydrogen atoms remain in the model, regardless of their display. |

|`compaq>>compaq-a>>center`| $spy.MakeHoverButton('toolbar-center','compaq>>compaq -a>>center') | Fragments will be assembled and the structure will be centered on the screen. |

## Specifying the formula of the structure
|*Z*'| Set the value of *Z*' here. (*Z*' is the number of formula units in the asymmetric unit.) For a molecular structure, *Z*' is typically 1. If there are two independent molecules on the screen, *Z*' must be set to 2. If the molecule sits on a symmetry element and has to be grown to be displayed in full, *Z*' will smaller than 1 (often 0.5). |

|`fixunit`| $spy.MakeHoverButton('toolbar-OK','fixunit') | Adjusts the sum formula to what is currently present in the model, taking the value of *Z*' into account. |


# Electron Density Quick Maps
This tool tab provides options for the calculation of various electron density maps, which can be displayed in different 2D or 3D formats using the tools in this tab. However, when the **Level** setting (see **Maps** tool tab help) approaches zero, electron density maps become very messy (and slow to display), and Olex2 therefore does not display these regions.

## Available maps
### diff
Will display the difference map, Fobs-Fcalc. Make sure to select **surface**, **wire**, or **points** from the **View** drop-down menu under the **Maps** tool tab (accessed through **Map Settings** in this tool tab) for this map to be displayed correctly. The corresponding line command is '<c>CalcFourier -diff -r=0.1 -m</c>' or simply '<c>CTRL+m</c>'. This is an extremely important tool for checking the validity of a model. Red regions of the map represent areas of missing electron density and green regions represent areas of excess electron density.

### Fcalc
Will display the calculated electron density.

### 2Fo-Fc
Will display the map of 2Fobs-Fcalc.

### Fobs
Will display the observed electron density map.

### Deformation
Will display a deformation electron density map (deviations from spherical atom model).

### PDF
Will display a PDF map.
<br>
<br>

### Show/Hide Map
Turns the display of the currently selected map on and off.

### Map Settings
This opens the **Maps** tool tab under **Tools** for further customising the map display.


# Disorder Tools
These are extremely useful commands for dealing with crystallographic disorder.


# PART Links
This is a selection of quick-links for displaying selected PARTs in the structure. The command-line equivalents are also very useful to know:

| `showp 0 1` | Shows all atoms in no particular PART (equivalently, in PART 0) and all atoms in PART 1 |

| `showp 0 2` | Shows all atoms in no particular PART (equivalently, in PART 0) and all atoms in PART 2 |

| `showp 1` | Shows only the atoms PART 1 |

| `showp` | Shows all atoms in all PARTs|

| `sel part 1` | Selects all atoms in PART 1 |

If the **Sel** box is ticked when **0|1** or **0|2** is clicked, atoms in PART 1 or PART 2, respectively, will be selected in the display. If the **Unique** box is ticked, a list of unique atoms in the structure will be printed in the output. Atoms will be marked with the parameter selected in the drop-down menu, e.g., **Occupancy** will indicate the occupancy of any partially occupied sites as a decimal number, **PART No** will show any non-zero PART numbers of atoms, and **Labels** will display atom labels.
<br>
<br>

The use of the **UP** arrow key to repeat recently issued commands is particularly useful here!


# Fit and Split Group
The fit and split tools operate on one or more selected atoms. To **fit** an atom (or group of atoms) is to move it to a desired location in the model. To **split** an atom (or group of atoms) is to divide it into two parts by creating a duplicate, which can then be moved to a desired location, e.g., to model disorder in the structure.

## Fit or Split One Atom
Left-click on an atom to highlight it. To **fit** the atom, click the **Fit** button. The color of the atom changes. Now hold down the **SHIFT** key and drag the atom with the left mouse button to any desired position. Press the **ESC** key to exit the Fit/Split mode. The **fitted** atom will remain in its new position.<br><br>To **split** the atom in two, click the **Split** button. The color of the atom changes as before, but dragging the atom with the **SHIFT** key pressed moves only ONE of the two atoms that were created by the **Split** command (the other atom can be moved with a separate **fit** command, as above). The occupancies of the two atoms are linked, and the atoms will now have different PART numbers. Press the **ESC** key to exit the Fit/Split mode; the moved atom will remain in place.

## Fit or Split Two Atoms
Select two atoms, then click either the **Fit** or the **Split** button. Split will generate a duplicate pair, fit will not. The color of the atoms changes. Drag the atoms with the mouse while pressing the **SHIFT** key to move them together as a group to any desired position.<br><br>To rotate the atoms about their midpoint instead of moving them, press the **CTRL** key while dragging with the mouse. Press **ESC** to exit the Fit/Split mode; the moved pair of atoms will remain in place.

## Fit or Split Three or more Atoms
Select three or more atoms, then click either the **Fit** or the **Split** button. As before, split will generate a duplicate group, but fit will not, and the atoms will change color. The entire group can be moved to any desired position by dragging it while holding down the **SHIFT** key (or rotated if the **CTRL** key is held down instead).<br><br>It is also possible to rotate the group about one of its bonds. First **activate** the bond about which you wish to rotate the group by **right-clicking** on it. Now, dragging the group while holding down the **CTRL** key rotates the group around this activated bond. Press **ESC** to exit this mode; any moved atoms will remain in their new positions.<br><br>This is one of the most powerful tools in Olex2. If a grouping of atoms is disordered, and one of the parts can be modelled (no matter how badly), the **Split** button will be very useful. (Typing **mode fit -s same** is equivalent to clicking the **Split** button.) Note that the SAME restraint is applied by default in Olex2 when splitting a group; other restraints may be selected from the drop-down menu. Everything will be restrained, so if the disorder *can* be modelled, the refinement process will sort it out automatically, though sometimes a large number of refinement cycles is needed.


# Peak & Uiso Sliders
This tool tab provides tools for selecting Q peaks and atoms according to their properties.

# Electron Density Peak Slider
This tool enables the selection of Q peaks by intensity.<br><br>Starting from the middle of the scale at 100, move the Peaks slider to the **left** to filter out the weakest Q peaks first, or to the **right** to filter out the strongest Q peaks first. Any commands issued after filtering will only apply to the remaining visible peaks. For example, the line command 'name $Q C' will convert all visible Q peaks to carbons, and clicking **Select** or **Delete** will select or delete the peaks, respectively.

# Uiso Select Slider
This tool allows the selection of atoms according to their Uiso values.

## Slide to the RIGHT
Starting from the middle of the scale, move the Uiso slider to the **right** to select atoms whose Uiso value is LARGER than the value indicated next to the slider.

|`sel atoms where xatom.uiso < 0.02`| Selects all atoms whose Uiso value is less than 0.02. |

## Slide to the LEFT
Starting from the middle of the scale, move the Uiso slider to the **left** to select atoms whose Uiso value is SMALLER than the value indicated next to the slider.

|`sel atoms where xatom.uiso > 0.04`| Selects all atoms whose Uiso value is greater than 0.04. |


# Growing
Olex2 shows the asymmetric unit by default. This tool tab contains very powerful techniques for 'assembling' a structure model on the screen exactly as desired. It is then possible to refine the model repeatedly in Olex2 without dismantling this assembly.

# Grow
## Growing
**Growing** here is used as a general term for adding atoms to the existing model on the screen in some systematic way, e.g., by adding symmetry-equivalent atoms to visualize an entire molecule when *Z*' < 1 for the structure.

### Grow All

|`grow`| Generates all 'missing' connected symmetry-equivalent atoms. |

### Shells
|`grow -s`| This adds atoms in concentric shells outward from the currently displayed image. |

### Complete
|`grow -w`| Generates all missing symmetry-equivalent atoms of an already grown structure, whether bound to the main fragment or not. Thus, this command will display symmetry-equivalent solvent molecules and counter-ions not generated by a plain **grow** command. |

### Asymmetric Unit
|`fuse`| Removes all symmetry-equivalent atoms and displays the asymmetric unit. |

### Complete shown growing bonds
|`grow -b`| Shows growable 'bonds' in a growing mode (see **Mode Grow** below). Click on any of these bonds to grow the structure. |

## Mode Grow
|`mode grow`| Similar to **grow**, but now the **grow** command will be executed only when an object is clicked. Upon entering a growing mode, growable 'bonds' will sprout from atoms satisfying the chosen growing conditions. |

There are various modifiers for this command:

### Short Contacts
|`mode grow -s`| Shows growable 'bonds' to atoms involved in 'short interactions' (e.g., hydrogen bonds) with the currently displayed structure. |

### Selection
|`mode grow -r`| Shows growable 'bonds' to other occurrences of the currently selected atoms. |

### Van der Waals Radii
|`mode grow -v 2.0`| Shows growable 'bonds' to other occurrences of the currently selected atoms that are at most 2.0 &Aring; away from the selected atom. |

### Move
|`mode grow -a`| When a growable 'bond' is clicked, the symmetry-equivalent atom is moved to the new position. This is really useful when trying to assemble a meaningful asymmetric unit for extended structures (polymers). |

### Shells
|`mode grow shells`| Shows growable 'bonds' that can be clicked to grow the structure outward in concentric shells. |

## Assemble
Strictly speaking, this tool does not belong to the **grow** family of tools, but it is frequently used together with the growing tools. It is used to rearrange components of the asymmetric unit for a more compact or chemically sensible display of the model.

### Broken Fragments
|`compaq -a`| Sometimes, parts of a model may become 'broken' - parts that should be bonded are shown as separate fragments. This tool will bring them back together. |

### Atom-to-Atom
|`compaq -c`| Similar to the 'Broken Fragments' tool, but using a different reassembly algorithm. |

### Metal Last
|`compaq -m`| In this tool, metal ions are first taken out of the reassembly process (which is very useful when trying to assemble a ligand!), after which they are placed at the shortest possible distance to the other atoms in the structure. |

### Peaks
|`compaq -q`| This moves all electron density peaks as close to existing atoms as possible. |


# Finishing
The buttons in this tool tab are for convenient access to elementary versions of more powerful sorting and drawing tools elsewhere in Olex2.


# QuickSort
The **Sort with Current Settings** button sorts the atoms in the model according to the options currently set under the **Sorting** tool tab. Clicking the pencil icon opens the **Sorting** tool tab, where the sort settings can be edited.


# QuickImages
The **Selected** button adds labels to selected atoms and bonds in the model. If nothing is selected, all atoms and bonds will be labelled. The **non-H** button adds labels to all non-hydrogen atoms, and the **No Labels** button removes all labels from the model. Clicking the **Go** button will create an image of the labelled model in the current working folder. To edit all image file options, open the **Images** tool tab by clicking the pencil icon next to the **Go** button.












# shift-move-target
Move Atoms
- Hold down SHIFT
- Move atoms with left mouse button
Split Atoms
- Click on an atom to split it


