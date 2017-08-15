# Select-Atoms-help 

# Select Atoms
Selects the atom types listed. 

## Exclusive  
Selects only the types that are clicked on. 

## Additive
Adds the clicked types to the selection.

## Command Line Examples 
  
|`sel $c`|Selects all C atoms|

|`sel -u`|Deselects everything|

|`sel c1`|Selects C1|

|`sel $c $n`|Selects all C and N atoms|

# Selections-help 

# Selections
Line before a table

## Invert

|`sel -i`|Inverts the current selection.|

## Deselect

|`sel -u`|Deselects (unselects) the all selected atoms.|

## Delete

|`kill sel`|Deletes all selected atoms. Same as pressing the 'Delete' key. Undo with **CTRL+Z**.| 

## Previous Selection
 
|`selback`|Re-select all atoms of the previous selection.|

# Select-Criteria-help 

# Select Criteria
To select all atoms for which Uiso is within user defined parameters.

# Select-Rings-help 

# Select Rings
Select all rings of the specified type (for example) C6, C5N, C5, C5O within the structure. You can type your own ring criteria in the box.
