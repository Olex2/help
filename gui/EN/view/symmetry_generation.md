# Symmetry Tools 
Tools for growing your structure, changing the composition/location of the asymmetric unit and viewing the basis vectors and cell. 

## Symmetry Tools 1 
The tools in this row are useful for re-organising parts of a structure if there is more than one moiety present in the structure.

### Move Near 
  1. Select the atom to which you want to move another moiety close to.
  2. Activate the mode by clicking on the 'Move Near' button.
  3. Click on on atom of each moiety that you wish to move close to the previously selected atom
  
`mode move`

### Copy Near 
  1. Select the atom to which you want to copy another moiety close to.
  2. Activate the mode by clicking on the 'Copy Near' button.
  3. Click on on atom of each moiety that you wish to copy close to the previously selected atom
  
`mode move -c`

### Assemble
In cases where parts of your structure have become fragmented or 'disjointed', this command will re-assemble the fragments. 

`compaq`  `compaq -a` 

## Symmetry Tools 2 
Tools in this row will achieve centering of the moieties in a stucture. 

### Centre on Cell 
All moieties in the structure will be centred on the cell. 

`move` 

### Centre on Largest Part  
All moieties in the structure will be centred on the largest moiety. 

`move`

## Symmetry Tools 3 
These tool switch symmetry related items on the screen on and off. 

### Show Basis  
Displays/Hides the basis vectors of this structure 

`basis`

### Show Cell  
Displays/Hides a drawing of the unit cell 

`cell` 

### Quality
Changes the quality setting in which atoms are drawn. A lower quality can be useful if the computer struggles with larger structures.

`qual -l qual -m qual -h`

## Symmetry Tools 4 

### Fuse 
Display the asymmetric unit of the structure only. All symmetry generated atoms will be removed. 

`fuse` 

### Grow All 
All symmetry equivalent atoms that are required to show the 'complete' structure will be generated. Of course, in the case of polymeric structures, this is somewhat arbitrary, and more controlled growing conditions will need to be employed. 

`grow` 

# Growing 
