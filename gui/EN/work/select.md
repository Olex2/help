# Select-Atoms-help

# Select Atoms
This menu provides several methods of selecting or deselecting atoms with varying degrees of specificity. Press '<c>ESC</c>' at any time to deselect everything.

## Exclusive
Selects only atoms of the type clicked.

## Additive
Adds the clicked type of atom to the selection.

## Command Line Examples

|`sel $c`| Selects all C atoms. |

|`sel -u`| Deselects (unselects) everything. |

|`sel c1`| Selects atom C1. |

|`sel $c $n`| Selects all C and N atoms. |


# Selections
Once atoms and/or bonds are selected, the following links can be clicked to perform specific actions.

## Invert
|`sel -i`| Inverts the current selection, i.e., all atoms and bonds *not* not currently selected will be selected instead. |

## Deselect

|`sel -u`| Deselects (unselects) all selected atoms. |

## Delete

|`kill sel`| Deletes all selected atoms; the same as pressing the '<c>Delete</c>' key. Undo the deletion with '<c>CTRL+Z</c>'. |

## Previous Selection

|`selback`| Re-select all atoms previously selected. |

# Select-Criteria-help

# Select Criteria
To select atoms on the basis of their Uiso values, enter the Uiso value in the box. Then choose the **>**, **<**, or **=** operator from the drop-down menu and click **Select** to select only those atoms meeting the specified criterion.

# Select-Rings-help

# Select Rings
Select all rings of the specified type, e.g., C6, C5N, C5, or C5O, within the structure. It is possible to specify other rings by typing them directly into the drop-down menu, e.g., C4O will find all five-membered rings consisting of four carbons and an oxygen. Click outside the menu to highlight the specified ring.
