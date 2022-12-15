# Elemental Analysis
Elemental analysis, molar mass and simulated mass spectrum.

## Elemental Analysis: CHN
Click this button to calculate the expected values of a CHN analysis from the structure model. The molar mass (molecular weight) in g/mol and a full elemental analysis are also provided. The equivalent line command is '<c>calcCHN</c>'.

## Calculate Molecular Isotope Pattern: Mass Spec
Calculates a simulated molecular isotope pattern for the structure using the natural abundances of all isotopes. Equivalent to typing '<c>calcms</c>' at the command prompt. 


# Molecular Volume
Total molecular volume and polyhedral volume of individual atoms.

## Molecular Volume
Calculates the total molecular surface area in &Aring;<sup>2</sup> and molecular volume in &Aring;<sup>3</sup>. The line command is '<c> vvol</c>'.

## Calculate Polyhedral Volume
Calculates the volume of a polyhedron defined by the selected atom (line command '<c>calcvol</c>').


# Molecular Bounding Box
Rectangular bounding box and R/S designations for chiral carbons.

## Molecular Bounding Box
Click this button (or type '<c>wbox</c>') to display a rectangular box surrounding the structure on the screen. The structure will be shown in space-filling view, and the dimensions and volume of the box will be printed on the screen. To remove the box, right-click on it with the mouse and select **Hide**. To return to a ball-and-stick view of the structure, type '<c>pers</c>'.

## List R/S designations of chiral carbons
Clicking this button prints a list of all the chiral carbons in the asymmetric unit along with the R/S configuration of each. The equivalent line command is '<c>rsa</c>'.

# Geometry Index
Four 4-coordinate and 5-coordindate geometries, this will calculate the **Geometry Index** URL[https://en.wikipedia.org/wiki/Geometry_index,WIKIPEDIA]. The procedure and relevant citations can be found in the linked Wikipedia article

## 4-coordinate
A parameter &tau; is calculated from the bond angles, and this parameter is a measure whether the geometry around the selected central atom is square planar (&tau; = 0) or tetrahedral (&tau; = 1).
An additional parameter &tau;' is also calculated, which will always be less or equal to &tau;, so the deviation from ideal tetrahedral geometry is more visible.

## 5-coordinate
A parameter &tau;5 is calculated from the bond angles, and this parameter is a measure whether the geometry around the selected central atom is square pyramidal (&tau;5 = 0) or trigonal bipyramidal (&tau; = 1).

