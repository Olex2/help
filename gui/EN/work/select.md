# Select Atoms 
Selects the atom types listed. 

## Exclusive  
Selects only the types that are clicked on. 

## Additive
Adds the clicked types to the selection.

## Command Line Examples   
`sel $c` (Selects all C atoms)

`sel -u` (Deselects everything)

`sel c1` (Selects C1)

`sel $c $n` (Selects all C and N atoms) 

# Selections 
XXX

## Invert
Inverts the current selection.

`sel -i`

## Deselect
Deselects (Unselects) the all selected atoms.

`sel -u` 

## Delete
Deletes all selected atoms. Same as pressing the 'Delete' key. Undo with `Ctrl`+`Z`.

`kill sel` 

## Previous Selection
Re-select all atoms of the previous selection. 

`selback` 

# Select Criteria 
To select all atoms for which Uiso is within user defined parameters. 

# Select Rings 
Select all rings of the specified type (for example) C6, C5N, C5, C5O within the structure. You can type your own ring criteria in the box. 
