#bad-reflections-target
Tools for dealing with reflections that no not fit well

#OMIT REFLECTIONS
The 'OMIT' button allows you to omit all reflections where |Error/esd| > than <value> in the box. The 'Clear omits' clears **all** omits -- all previously omitted reflections will be back for refinement (except those that are omitted with a general OMIT, e.g. 'OMIT -3 52')

#SORT BAD REFLECTIONS
No entry

#LIST BAD REFLECTIONS
**AA list of those reflections that have been flagged by the refinement program ShelXL will be shown in this panel.**

##Omit all equivalents of a reflection
You may choose to omit a reflection totally by pressing the OMIT link. This will insert the appropriate OMIT instruction.

##Omit a particular instance of a reflection
You can also choose to omit a particular reflection (e.g. because it was under the beam-stop). To do so, click the <a href=edithkl>Edit Reflections</a> link at the bottom of the list of bad reflections. This will bring up a window with all the reflections in your reflection file, grouped by equivalent reflections. By adding the minus symbol '-' in front of a particular reflections, this reflection will be moved to the bottom of the .hkl file (after the '0 0 0' instruction, which tells the refinement program to ignore it.

#EXCLUDE BY H K AND L
No entry

#SHOW HKL FILE
No entry
