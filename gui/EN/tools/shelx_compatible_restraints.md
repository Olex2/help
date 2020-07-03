# Shelx Restraints
These are the SHELX restraints. All of these will also apply to a refinement using the olex2.refine.

See a detailed description on the [Shelxl manual](https://shelx.uni-ac.gwdg.de/SHELX/shelxl_html.php)

# DFIX
## DFIX d s[0.02] atom pair(s)
Fixes a distance **d** between pairs of atoms to a given value in &Aring; within an estimated standard deviation of &plusmn; **s** (standard setting 0.02 &Aring;)

**Example:** *DFIX 1.54 0.01 C1 C2 C2 C3 C3 C4*

Gives a butane carbon atom chain with bond distances between 1.53 and 1.55 &Aring;.<br>

![0.3 n-butane](images/butane.jpg)

# DANG
## DANG d s[0.04] atom pair(s)
This instruction is interpreted in exactly the same way as DFIX, but the default value of s is twice the value of DFIX (0.04). It is usually used to restrain 1,3 distances, i.e. distances between two atoms that are both bonded to the same atom. 

**Example:** *DANG 2.52 0.04 C1 C3 C2 C4*

Gives a butane carbon atom chain with 1,3 distances of 2.52ang or and angle of 113deg.

# SADI
## SADI s[0.02] atom pairs
Fixes bond lengths between given atom pairs to a the same distance within an estimated standard deviation of &plusmn; **s** (standard setting 0.02 &Aring;).<br>

**Example:** *SADI 0.005 C1 F1 C1 F2 C1 F3*

Models a CF<sub>3</sub> group with same C-F distances within 0.005 &Aring; deviation.

# CHIV
## CHIV V[0] s[0.1] atomnames
The chiral volumes of the named atoms are restrained to the value V (in Å³) with standard deviation s. The chiral volume is defined as the volume of the tetrahedron formed by the three bonds to each named atom, which must be bonded to three and only three non-hydrogen atoms in the connectivity list.

# FLAT
## FLAT s[0.1] four or more atoms
Lie the atoms in a plane.

**Example:** *FLAT C1 C2 C3 C4 C5 C6*

Restrain a phenyl ring to be planar.

# DELU
## DELU s1[0.01] s2[0.01] atomnames
All bonds in the connectivity list connecting atoms on the same DELU instruction are subject to a 'rigid bond' restraint, i.e. the components of the (anisotropic) displacement parameters in the direction of the bond are restrained to be equal within an effective standard deviation s1. The same type of restraint is applied to 1,3-distances as defined by the connectivity list (atoms 1, 2 and 3 must all be defined on the same DELU instruction).

**Example:** *DELU C1 C2 C3 C4*

# SIMU
## SIMU s[0.04] st[0.08] dmax[2.0] atomnames
Atoms closer than dmax are restrained with effective standard deviation s to have the same Uij components ignoring the connectivity table. If (according to the connectivity table, i.e. ignoring attached hydrogens) one or both of the two atoms involved is terminal (or not bonded at all), st is used instead as the esd.

# ISOR
## ISOR s[0.1] st[0.2] atomnames
The named atoms are restrained with effective standard deviation s so that their Uij components approximate to isotropic behavior; however the corresponding isotropic U is free to vary.

# RIGU
## RIGU s1[0.004] s2[0.004] atomnames
Apply enhanced rigid bond restraints with esds s1 for 1,2-distances and s2 for 1,3 distances [Thorn, Dittrich & Sheldrick, Acta Cryst. A68 (2012) 448-451](http://dx.doi.org/10.1107/S0108767312014535).

U<sub>33</sub>, U<sub>13</sub> and U<sub>23</sub> are restrained to be equal on bonded atoms in a local coordinate system defined as such:
(i) the z axis is along the bond A—B;
(ii) the x axis is arbitrary but perpendicular to the z axis; and
(iii) the y axis completes a direct orthonormal coordinate system.
