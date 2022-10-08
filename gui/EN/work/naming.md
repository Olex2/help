# naming-help

# Naming
This tool tab is for naming atoms in a molecule. However, in some cases it might be more convenient to use the command line to name atoms more efficiently.

## Using the Naming Tools
Clicking the **Name&** button enters the naming mode. Once in this mode, the first atom clicked will be named with its element symbol according to the settings specified on this line, and any subsequently clicked atoms will be named sequentially after the first. Press '<c>ESC</c>' to exit the mode, and '<c>CTRL+Z</c>' to undo the naming.

**Note**: When you are in this mode, the mouse pointer changes. In some modes it simply becomes a hand-symbol, but in other cases the pointer will tell you what will happen if you click on an atom.

### Start
The first atom clicked will be named with its element symbol and the number in this box (usually 1).

### Suffix
Appends an optional suffix (e.g., A, _, ') to the atom name.

### Type
If an element is specified in this box, any atom clicked will be converted to this element, and all other settings on this line will be applied. If no element is specified, any atom clicked will simply be named using its element symbol.

## Using the Command Line
|`name sel type`| Will change all currently selected atoms into the element specified by *type*, e.g., '<c>name sel N</c>' will convert currently selected atoms to nitrogen. |

|`name sel integer`| Will re-number all currently selected atoms according to the order in which they were selected, starting from *integer*, e.g., selecting four carbon atoms and typing '<c>name sel 3</c>' will name them C - C6 in the order of selection. |
<br>
<br>
'<c>CTRL+Z</c>' undoes this change.

# Automatic Hydrogen Naming
Olex2 will keep track of the naming of hydrogen atoms automatically. This feature can be switched off by unticking the 'Automatic Hydrogen Naming' box, if any hydrogens need to be named manually.

# Match Naming
If the structure contains two or more identical moieties, it is only necessary to name one of them, as Olex2 is capable of applying the same naming scheme to any others. This is helpful when naming atoms in structures with *Z*' > 1 and also in structures containing a metal center coordinated to more than one ligand of the same type. In the latter case it is necessary to set the maximum number of bonds for the metal to 0 before naming the equivalent fragments. This is done by right-clicking the metal, then setting Bonds to 0 in the menu that appears.
<br>
<br>

Name all the atoms in the first moiety. Enter a suffix in the **Suffix** box; this will be appended to the names of the other identical moieties. Click **any one atom** of the first moiety, then the **corresponding atom** in the *other* moiety (or moieties). Click the **Equivalent Fragments (*Z*' > 1)** link to name all moieties appropriately. (Reset the number of bonds to the metal center, if necessary.)
<br>
<br>

Some line commands useful for naming are described below. Some of these commands have no equivalent in the GUI.

## Add a Suffix
|`match sel -n=suffix`| First select two corresponding atoms of two identical moieties. Typing this command will apply the naming scheme used for the first moiety to the second moiety; atom names in the second moiety will have the 'suffix' character appended. For example, '<c>match sel -n=A</c>' will add the suffix 'A' to the names of the second moiety. |

## Replace a Suffix
|`suffix'>match sel -n=$suffix`| This is similar to **Add a Suffix**. However, instead of adding a suffix, this command replaces the first character of the original naming scheme with another character. This is useful, for example, if carbons in one ligand are named C101, C102, C103 ... and corresponding atoms in the other ligand are to be named C201, C202, C203 ...|

## Replace last character
|`suffix'>match sel -n=-suffix`| As in **Replace a Suffix**, but the last character of the atom name is replaced instead. |

