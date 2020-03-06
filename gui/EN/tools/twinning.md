# Twinning-help

# Twinning
These tools provide a ways to assess whether twinning is present in your structure, and to calculate viable twin laws.

## Find 2-fold
This will rapidly search for 2-fold twin laws present in your structure, and present any viable laws for your use.

## Cumulative Intensities
This will generate a graph of the cumulative intensities. If you data follows the bottom line, then your crystal is almost certainly twinned.

# General
This row contains general settings for your searches, as well as an automated search which will try different procedures to attempt to find twin laws.

## Extended
This toggle causes any searches to be run in 'extended' mode, doing a more in depth search at the cost of time. If you find that no laws are found, ticking this may allow some to be found.

## Min Laws
The minimum number of viable twin laws to return. This allows the search to cut off early if it has found sufficient twin laws, but they may be inferior to later found laws. If you find that twin laws are returned but they are of poor quality, it is worthwhile increasing this.

## Threshold
The threshold at which two points are considered 'overlapping'. A greater value will cause more potential twin laws to be considered, but may erroneously return laws as useful when they do not in fact represent an overlap. Smaller values will restrict the amount of laws considered, but those which are will be more precise.

# Spherical
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
