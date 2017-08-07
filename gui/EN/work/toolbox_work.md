# Labels 

You can select what you would like to see as labels in the molecule display. If a particular property is not applicable for a particular atom, there will be no label. 

## Toggle On/Off 
This is to display or hide atom or Q-peak labels. It will switch other types of labelling off, but selecting it again will display atom name labels. [F3] does the same thing.

## Atom Names 
All atom names of **non-hydrogen atoms** will be displayed next to the atoms. `labels -l`

## Crystallographic Occupancy 
This displays the crystallographic occupancy of any atoms which are not 100% occupied i.e. their occupancy is not 1. `labels -o`

## Chemical Occupancy
Same as above, but the occupancy values for atoms that are located on symmetry elements are not shown.

## Parts 
Displays PART numbers for any atoms not in PART 0. `labels -p`

## Link Codes
If atoms are linked, the link code will be shown. (FVAR 21/-21 in ShelXL language) `labels -lo`

## H Atom Labels
This will include the hydrogen atom labels along with the atom name and Q-peak labels `labels -hl`

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
