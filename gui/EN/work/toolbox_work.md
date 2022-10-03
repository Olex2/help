# toolbox work-target
A collection of useful tools
- Make all peaks Carbon
- Move Atoms
- Show/Hide Peaks
- Expand Short Contacts
- Peak Slider
- Disorder Tools


# shift-move-target
Move Atoms
- Hold down SHIFT
- Move atoms with left mouse button
Split Atoms
- Click on an atom to split it


# Labels
It is possible to customise the labels in the model display. If a particular property is not applicable to any atom, there will be no label, e.g., if 'labels -o' (see below) is typed and all atoms have occupancy 1, no atoms will be labelled.

|`help labels`|To see all options for the 'labels' command|

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
|`labels -lo`| If atoms are linked, the link code will be shown. (FVAR 21/-21 in ShelXL language) |

## H Atom Labels
| `labels -h -l` | This will include the hydrogen atom labels along with the atom name and Q-peak labels |

## Fixed Parameters
| `labels ?????` | Enter text here for "fixed parameters" labels |

## Variables
| `labels -v` | Displays any atoms where the occupancy is linked to any variable |

## AFIX Commands
| `labels -a -h` | This is useful to check the AFIX commands that are being applied to the structure |

## Q-Peak Intensities
| `labels -qi` | Relative intensities of the Q-peaks will be displayed on the structure |

## Ueq
| `labels ?????` | Enter text here for "Ueq" labels |

## Label + residue rumber
| `labels ?????` | Enter text here for "label + residue number" labels |

## Residue Numbers
| `labels -rn` | Show the number of the residue an atom belongs to |

## Residue Class
| `labels -rc` | Show the number of the residue class an atom belongs to |


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


# Disorder Tools
These are an extremely useful set of commands for dealing with crystallographic disorder.


# PART Links
This is a selection of quick-links regarding displaying of PARTs in the structure. The command-line equivalents are also very useful to know:

| `showp 0 1` | Shows all atoms in no particular part and all atoms in PART 1 |

| `showp 0 2` | Shows all atoms in no particular part and all atoms in PART 2 |

| `showp 1` | Shows only the atoms PART 1 |

| `showp` | Shows all PARTs|

| `sel part 1` | Selects all atoms in PART 1 |

The use of the **UP** arrow key to repeat recently issued commands is particularly useful in this context!


# Fit and Split Group
The fit and split tools operate on one or more selected atoms. To **fit** an atom (or group of atoms) is to move it to a desired location in the model. To **split** an atom (or group of atoms) is to divide it into two parts by creating a duplicate, which can then be moved to a desired location, e.g., to model disorder in the structure.

## Fit or Split One Atom
Left-click on an atom to highlight it. To **fit** the atom, click the **Fit** button. The color of the atom changes. Now hold down the **SHIFT** key and drag the atom with the left mouse button to any desired position. Press the **ESC** key to exit the Fit/Split mode. The **fitted** atom will remain in its new position.<br><br>To **split** the atom in two, click the **Split** button. The color of the atom changes as before, but dragging the atom with the **SHIFT** key pressed moves only ONE of the two atoms that were created by the **Split** command (the other atom can be moved with a separate **fit** command, as above). The occupancies of the two atoms are linked, and the atoms will now have different PART numbers. Press the **ESC** key to exit the Fit/Split mode; the moved atom will remain in place.

## Fit or Split Two Atoms
Select two atoms, then click either the **Fit** or the **Split** button. Split will generate a duplicate pair, fit will not. The color of the atoms changes. Drag the atoms with the mouse while pressing the **SHIFT** key to move them together as a group to any desired position.<br><br>To rotate the atoms about their midpoint instead of moving them, press the **CTRL** key while dragging with the mouse. Press **ESC** to exit the Fit/Split mode; the moved pair of atoms will remain in place.

## Fit or Split Three or more Atoms
Select three or more atoms, then click either the **Fit** or the **Split** button. As before, split will generate a duplicate group, but fit will not, and the atoms will change color. The entire group can be moved to any desired position by dragging it while holding down the **SHIFT** key (or rotated if the **CTRL** key is held down instead).<br><br>It is also possible to rotate the group about one of its bonds. First **activate** the bond about which you wish to rotate the group by **right-clicking** on it. Now, dragging the group while holding down the **CTRL** key rotates the group around this activated bond. Press **ESC** to exit this mode; any moved atoms will remain in their new positions.<br><br>This is one of the most powerful tools in Olex2. If a grouping of atoms is disordered, and one of the parts can be modelled (no matter how badly), the **Split** button will be very useful. (Typing **mode fit -s same** is equivalent to clicking the **Split** button.) Note that the SAME restraint is applied by default in Olex2 when splitting a group; other restraints may be selected from the drop-down menu. Everything will be restrained, so if the disorder *can* be modelled, the refinement process will sort it out automatically, though sometimes a large number of refinement cycles is needed.


# Electron Density
The electron density viewer will calculate various electron density maps and allowsthe display of these in a variety of formats.
Note: Close to zero, these maps become very messy (and slow to display). Olex2 therefore does not display these regions.

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

|`CalcFourier`| Calculates the map according to the settings set in the map tool.|


# Peak & Uiso Sliders

## Electron Density Peak Slider
Electron Density Peak Slider Move the slider to the **left** to filter out strongest peaks first, or to the **right** to filter out weakest peaks first. You can then do things like `name $Q C` - and this will only apply to the currently visible peaks. The same goes for the Select and Delete buttons.

## Uiso Select Slider
This tool allows the selection of atoms according to their Ueq values.

### Slide to the RIGHT
This will select atoms where the Ueq value is LARGER than the value indicated by the slider.

|`sel atoms where xatom.uiso > 0.06 xatom.type!='Q'`| |

### Slide to the LEFT
This will select atoms where the Ueq value is SMALLER than the value indicated by the slider.

| `sel atoms where xatom.uiso > 0.08` | Selects all atoms where the Uiso value is larger than 0.08|


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

## Mode Grow
|`mode grow`|Similar to grow, but now this command will be executed only after you click on an object. When you enter a growing mode, clickable 'growing bonds' will sprout from atoms where the kind of growing you have asked for is applicable.|

There are various modifiers for this command:

### Short Contacts
|`mode grow -s`|Will show these growable 'bonds' to those atoms where 'short interactions' exist.|

### Selection
|`mode grow -r`|Will show growable 'bonds' to other occurances of the currently selected atoms.|

###Van der Waals Radii
|`mode grow -v 2.0`|Will show growable 'bonds' to other occurances of the currently selected atoms that are at least the indicated distance away from the selected atom.|

### Move
|`mode grow -a`|When you click on growable bonds the symmetry equivalent atom will be moved to the new position. This is really useful when you are trying to assemble a meaningful asymmetric unit for extended structures (polymers).|

### Shells
See above.

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



# Finishing

## Quick Sort
TBI - still!

## Quick Images
TBI


# Split Group
The tools on this line will fully SPLIT the atom you click next into two atoms.

## No Restraints
This will simply generate two atoms (at the focal points of the ellipsoids) and set the occupancies for each atom to 0.5. One of the atoms will be in PART 1, the other in PART 2. After the splitting has occured, you can move the newly 'generated' atoms to where you would like them to be (by holding the SHIFT key while moving them).

| `mode split` | Splits subsequently clicked atoms |

## EADP
| `mode split -r=EADP` | This will split the atom as above, but will restrain the ADP values for both atoms to be the same. This is useful early on, and should probably be removed once the disorder model is nearly complete. You might want to apply the DELU restraint instead.|

## ISOR
| `mode split -r=ISOR` | This will split the atom as above, and reply an ISOR restraint to each of the two atoms. |

## SIMU
| `mode split -r=SIMU` | As above, but with a SIMU restraint. |

