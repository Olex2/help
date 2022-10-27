# Shelx Constraints
These are SHELX constraints. All of these will also apply to a refinement using olex2.refine.

## AFIX
The **AFIX** instruction is for placing hydrogen atoms in idealized (riding) positions.

## EXYZ
The **EXYZ** instruction is for specifying that two or more atoms share the same *x*, *y*, and *z* coordinates (used when two or more elements share the same site in the structure, as commonly occurs in minerals). Often combined with **EADP**.

## EADP
Specifies that the same anisotropic displacement parameters are to be used for two or more atoms, e.g., the three fluorines of a CF<sub>3</sub> group.