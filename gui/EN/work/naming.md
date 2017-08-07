# Naming 
This GUI can be used for naming atoms in a molecule. However, in some cases it might be better to use the command line to name atoms more efficiently.

## Using The Gui
After pressing the 'GO' button, you will be in a mode. That means, that something# will happen to all subsequently clicked atoms. In this case:

### Start
The clicked atom will be named with the Current atom type (unless 'Type' is set to something else) and numbered starting from the number that is entered in this box.

### Suffix
A suffix will be given to the atom, with all other settings in place.

### Type
The atom type of the atom will be changed as well as all other settings will be applied.
**Note**: When you are in a mode, the mouse pointer changes. In some modes it simply becomes a hand-symbol, but in other cases the pointer will tell you what will happen if you click on an atom.

## Using the Command Line

`name sel type` - Will change all currently selected atoms into the new type.

`name sel integer` - Will renumber all currently selected atoms in the order of which they were selected starting from.
