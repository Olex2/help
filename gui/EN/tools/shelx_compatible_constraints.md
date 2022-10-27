# Shelx Constraints
These are SHELX constraints. All of these will also apply to a refinement using olex2.refine.

## AFIX
The **AFIX** instruction is for placing hydrogen atoms in idealized (riding) positions.

## EXYZ
The **EXYZ** instruction is for specifying that two or more atoms share the same *x*, *y*, and *z* coordinates (used when two or more elements share the same site in the structure, as commonly occurs in minerals). Often combined with **EADP**.

## EADP
Specifies that the same anisotropic displacement parameters are to be used for two or more atoms, e.g., the three fluorines of a CF<sub>3</sub> group.

# AFIX
AFIX instructions are for placing hydrogen atoms in idealized (riding) positions in a structure.

## Syntax of the AFIX command
Usage: **AFIX mn d[number] sof[11] U[10.08]**
<br>
<br>
From the ShelX manual:<br>
"AFIX applies constraints and/or generates idealized coordinates for all atoms until the next AFIX instruction is read. The digits mn of the AFIX code control two logically quite separate operations. m refers to geometrical operations which are performed before the first refinement cycle (hydrogen atoms are idealized before every cycle), and n sets up constraints which are applied throughout the least-squares refinement. n is always a single digit; m may be two, one or zero digits (the last corresponds to m = 0)." For more details, refer to the URL[https://shelx.uni-goettingen.de/shelxl_html.php, ShelX Manual].
<br>
<br>

## Number drop-down menus
In this row, the first two drop-down menus *after* the constraint menu refer to m and n, respectively, in the AFIX command.

## clear
Select any atom(s) to which an AFIX command has been applied. Clicking **clear** will remove the AFIX command.

## de
Click **de** to enter a mode in which all AFIX instructions being applied to the structure are displayed. Also in this mode, the AFIX command currently specified in this tool tab can be applied to individual atoms by clicking on them.

## go
Click **go** to apply the AFIX command currently specified in this tool tab.