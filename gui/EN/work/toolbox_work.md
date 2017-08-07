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
