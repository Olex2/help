# Twinning-help

# Twinning
These tools provide methods of determining whether a structure is twinned, and if so, to calculate the twin law.

## Find 2-fold
Clicking **Find 2-fold** will initiate a rapid search for 2-fold twin laws applicable to the structure. If a viable twin law is found, the corresponding transformation matrix will be printed in the output window. For example, suppose a 2-fold twin law is found with the following transformation matrix:
<br>
<br>

-1 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0
<br>
0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -1 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0
<br>
0.667 &nbsp; 0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1
<br>
<br>

The twin law search will also suggest a BASF (batch scale factor, or fractional contribution of one of the twin components). If the suggested BASF is 0.204, entering the following two statements in the .ins file will take into account the observed twinning during subsequent refinement:
<br>
<br>

TWIN -1 0 0&nbsp;&nbsp;&nbsp;0 -1 0&nbsp;&nbsp;&nbsp;0.667 0 1&nbsp;&nbsp;&nbsp;2
<br>
BASF 0.204
<br>
<br>

(The 2 at the end of the TWIN instruction is to specify a two-component twin.)

## Find all Twinning
This searches for *all* twin laws applicable to the structure, not just the common 2-fold twin laws. If any are found, the corresponding transformation matrix and BASF will be printed at the bottom of this tool tab.

## Cumulative Plot
**Cumulative Plot** opens the cumulative intensity distribution plot for the experimentally observed reflections. If the data points in the plot lie mostly along the bottom (red) line, there is a very strong likelihood that the structure is twinned.

# General
This row contains general settings for your searches, as well as an automated search which will try different procedures to attempt to find twin laws.

## Extended
This toggle causes any searches to be run in 'extended' mode, doing a more in depth search at the cost of time. If you find that no laws are found, ticking this may allow some to be found.

## Min Laws
The minimum number of viable twin laws to return. This allows the search to cut off early if it has found sufficient twin laws, but they may be inferior to later found laws. If you find that twin laws are returned but they are of poor quality, it is worthwhile increasing this.

## Threshold
The threshold at which two points are considered 'overlapping'. A greater value will cause more potential twin laws to be considered, but may erroneously return laws as useful when they do not in fact represent an overlap. Smaller values will restrict the amount of laws considered, but those which are will be more precise.

# Spherical Angle Axis
This search directly uses strong reflections, and the potential points they could map to around a sphere, calculating viable twin laws given these limitations. It is in general a faster search which searches less space whilst finding more laws, and is not restricted in the angle that the twin law rotates by.

Spherical search is strongly affected by the minimum law number, and if it gives poor results it is recommended to increase that.

## Bad Reflns
The number of bad reflections to consider before stating there are no twin laws relevant to those reflections.

## Threshold
The threshold by which the bad reflection points are considered well overlapping within the spherical search. This should be lower than the general threshold.

# Angle-Axis
This search searches step-by-step for twin laws by considering potential axes and rotations about them.

## Max index
The maximum index of axes to use. Axes are taken from integer points in both direct and reciprocal space. Increase this to search a greater variety of twin laws.

## Rot Fract'n
The rotation fraction 'n' gives us the angle = 360/n by which we try to rotate about each axis. Increase this to search a more fine stepping of twin laws.
