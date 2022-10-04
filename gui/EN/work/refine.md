# refine-target
Refine the structure with, e.g.,
- CTRL+R
- >>'refine'
- >>'refine 4 4'


# refine-settings-target
Open the refinement settings


# draw-target
Make an image of the structure using the current settings


# draw-settings-target
Open the drawing settings


# report-target
Generate a report


# report-settings-target
Open the report settings


# Refinement Program
Apart from its own refinement engine (olex2.refine), Olex2 also supports all variants of ShelXL. Depending on the refinement package, different refinement methods are available.

## olex2.refine
The refinement engine built into Olex2. It supports all ShelXL instructions, plus a number of new restraints and constraints that are not available from ShelXL. One can switch between this engine and ShelXL, and Olex2 will not 'forget' the special instructions that are available only in olex2.refine, but of course ShelXL won't heed them.

## Methods for olex2.refine
The **Gauss-Newton (GN)** algorithm URL[https://en.wikipedia.org/wiki/Gauss-Newton_algorithm,WIKIPEDIA] is normally used with olex2.refine. Use the more strongly damped **Levenberg-Marquardt (LM)** algorithm URL[https://en.wikipedia.org/wiki/Levenberg-Marquardt_algorithm,WIKIPEDIA] when the refinement converges poorly.

## ShelXL-20XX
Since 2012, updated versions of ShelXL have been released periodically by George Sheldrick. Please check the SHELX website regularly to ensure that the latest versions of the SHELX programs are installed -- these are the **only versions** that should be used. Older versions will still work, however, as long as they are 'on the PATH' and are called 'shelxl'. See Ilia Guzei's manual under the Olex2 Home tab for instructions on how to add a folder to the PATH. Our recommendation is to make a folder called 'CrystallographyPrograms' on the root of one of your drives and then add that folder to the PATH. Any known executable in that folder will be available for use within Olex2.

## Methods for ShelXL
LS stands for full matrix Least squares refinement (most suited for small molecule structures). CGLS refers to conjugate gradient least squares refinement (faster than LS when the number of parameters is large, and therefore most suited for early stages of macromolecular structure refinement).

## Cycles
This sets the maximum number of refinement cycles for olex2.refine; if the refinement converges earlier, the refinement process will stop. For other refinement programs such as ShelXL, this is the actual number of refinement cycles that will be carried out.

## Peaks
This specifies the number of residual electron density peaks (Q peaks) to display after refinement.

## From the Command Line
|`refine 12 5`| This line command will carry out 12 cycles of refinement, after which five residual electron density peaks will be displayed. This number of cycles and peaks will persist in future refinements until changed. |


# Set Reflection File
The reflection file is specified here; it contains in a condensed form all the data that were collected during the X-ray diffraction experiment.

## hkl
The standard format for a reflection file is the **hkl** file. Choose the file against which to refine your model from this drop-down menu. There is no need to rename anything -- just choose the file and click **refine**.

## Other File Formats
Olex2 can also handle file formats such as **raw** and others.


# Weights, Extinction and ACTA
|`weight`| A weighting scheme should be applied to the diffraction data once the model is nearly finished and all atoms have settled into their respective positions. |

All refinement programs will suggest a suitable weighting scheme. Clicking on the coloured line applies the suggested weighting to the data. By ticking the box, Olex2 will automatically update to the suggested values after each refinement cycle. (In practice, this reduces to simply ticking the **Weight** tickbox after the model has settled and running additional cycles of refinement until the numbers in the **Weight** boxes turn green.)

## Extinction Correction
Extinction is a physical phenomenon affecting the intensity of reflections and can result in systematically absent reflections being observed under certain conditions. The **EXTI** parameter is designed to account for the intensity changes associated with extinction. The method used is a compromise to cover both primary and secondary extinction. In general this correction should not be included in refinement until all of the non-hydrogen atoms have been located. (In practice, first click on the **percent sign** next to R1 at top to display the Fobs vs Fcalc graph, and if it shows visible downward curvature at high Fcalc, tick the **EXTI** tickbox and run additional cycles of refinement until convergence is reached.)

## ACTA
From the drop-down menu, select **No ACTA** to omit writing a CIF file, **ACTA NOHKL** to write a CIF file without an embedded hkl file, and **ACTA** to write a CIF file with an embedded hkl file.

# Refinement Masks
In some structures, solvent disorder can be so severe that modelling this disorder using atomic sites (i.e. partially occupied atoms) is neither possible nor sensible. In these cases, it is better to not even attempt to model the 'affected area' - but to simply leave the measured electron density in place. This technique requires the calculation of the area that should be 'taken out of the refinement' - and defining *that* depends on the current structure.
<br>
<br>
Watch the video! URL[https://youtu.be/3jC2CVqSkgc,YOUTUBE]
<br>
<br>

Our implementation of solvent masking is based on the **BYPASS** paper by P.van der Sluis and A.L. Spek.
URL[https://doi.org/10.1107/S0108767389011189,PAPER]

### Use solvent mask
Include in the refinement a solvent contribution to the structure factors as the discrete Fourier transform of the electron density in the solvent area. The solvent mask can be calculated and displayed under Tools > Maps > Masks. When used with smtbx-refine, the solvent contribution is added internally to that calculated from the ordered part, whilst with SHELXL the solvent contribution is subtracted from the observed data before passing a modified hkl file to the external refinement program.

### Recompute mask before refinement
When ticked, the solvent mask will be recomputed before the start of the refinement. This can lead to an improved solvent mask, particularly if the ordered part of the structure was poorly converged before the initial mask search.

### Solvent r
Only grid points within cavities _larger_ than a certain solvent radius (r) are considered. The default value is **1.2 &Aring;**. This avoids adding voids where nothing can possibly live in!

### Truncation
TBI


# Refinement Settings Extra
Some refinement programs may have associated extra settings (i.e. those not covered by the general GUI. This is where you find them!
