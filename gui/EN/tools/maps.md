# Map View

# Map View

## Available Display Modes
The **plane**, **contour**, **surface**, **wire**, and **points** options shown under the **View** drop-down menu are different viewing styles available for displaying maps and masks in Olex2.

### plane, contour, contour+plane
These three views show an interactive 2D slice of a map, i.e., a display of a parameter such as the calculated electron density, in the plane of the screen. The structure can be rotated, moved or zoomed while the map is displayed, and the 2D slice will change accordingly as different portions of the structure pass through the plane.

### Colours
Select the number of colours in the colour scale of a 2D map display in **plane** and **contour+plane** modes from this drop-down menu.

### surface, wire, points
These three views show a 3D display of a parameter, such as the calculated electron density, overlaid on the structure. If there is insufficient electron density, however, only the 2D display will the shown. If the computer struggles to display these maps, first adjust the display levels in the **points** view, then select **wire** or **surface**, since the latter are more computationally demanding graphics displays. 
<br>
<br>

In the **surface**, **wire**, and **points** display modes, positive values of electron density are shown in green and negative values (holes) in red, providing a very powerful tool for checking the validity of a structure during refinement. Thus, for example, if the **diff** (difference between Fobs and Fcalc) map for a structure is displayed in the **wire** view and a hydrogen atom is encased in a red blob, with a green blob nearby, then that hydrogen should probably be moved to the position of the green blob if the new position is chemically reasonable. A useful keyboard shortcut to display the **diff** map is '<c>CTRL+M</c>'.

### Extended
Ticking this box will extend the map display out from one unit cell to 27 adjacent unit cells, a 3 x 3 x 3 stack. This is very useful for viewing the shapes, sizes, and distribution of voids in the structure.

### Edit
Click this button to edit the colour properties of the various map surfaces.


# 2D Map Contours
This slider selects either the maximum number of contour lines (for the **contour** and **contour+plane** view) or the number of colours (for the **plane** and **contour+plane** views). In **contour** view, regions of positive electron density are displayed as solid lines, whilst regions of negative electron density (holes) are displayed as dashed lines. A contour map will be included in any PostScript drawing created whilst the map is displayed.
<br>
<br>

~Hint:~ If symmetrical maps around 0 are desired, then select, e.g., 21 contours, giving 10 above 0, 10 below 0 and one for the 0 level itself. 


# 2D Map Scale
This option sets the maximum and minimum of the electron density in a map. Clicking **Automatic** (the default setting) will adjust the map display so that the minimum and maximum on the map legend match the minimum and maximum electron density in the *current* map slice. **Static**, on the other hand, leaves these minimum and maximum values fixed at the *global* minimum and maximum, respectively, no matter what slice is currently shown.


# 2D Static Map Scale

## Min
Use this slider to define the minimum value of the parameter displayed on the map. The slider adjusts the minimum in quarter-integer values but also accepts manual input in the text box next to it.

## Step
This slider defines the step size between two adjacent contours/colours. As with **Min**, this slider has pre-defined slider values (difference 0.02), but a specific value can also be typed into the text box.


# 2D Map Position and Size

## Depth
This slider controls the depth of the map plane "into" the screen. More negative values of **Depth** move the map further into the screen until the map is "behind" the model. More positive values move the map further out of the screen until the map is "in front" of the model. Different parts of the structure will move through the 2D slice as **Depth** is changed. Alternatively, to move the map perpendicular to the screen (i.e., into or out of the screen), hold down the '<c>SHIFT</c>' key while dragging the left mouse button in the map area. A little care must be taken to drag in an area of the map itself, not on the structure.
<br>
<br>

Select three or more atoms and click on the **Depth** button to align the map with the mean plane through the selected atoms. The mean plane will also be displayed; to remove it, left-click on it and press '<c>Delete<c>'.

## Size
The **Size** slider controls the size of the plotted map. Larger values will actually *decrease* the size of the map on the screen, but will *increase* the map resolution. The visible area of the map can also be adjusted by holding down the '<c>CTRL</c>' key whilst dragging the right mouse button in the map area.


# Map 3D
The **Level** slider adjusts the level of detail desired in the displayed map. A value can also be entered into the box next to the slider. If the level is set high, only the most prominent features (i.e., biggest electron density peaks and holes) will be shown. If the level is low, on the other hand, many more peaks and holes will be displayed. Below a certain cutoff level, however, the features of the map become so overwhelmed by the noise in the data that the map becomes meaningless. To avoid this, the level will be locked at and below the cutoff level.


# Calculate Voids

# Calculate Voids
Calculates the voids and channels in the structure. This calculation is based on the Olex2 internal libraries, and help is available from

|`help calcvoid`| |


# Calculate Solvent Accessible Voids


# Calculate Solvent Accessible Voids
|`calcsolv`|Calculates the solvent accessible voids. This calculation is based on the smtbx/cctbx Olex2 libraries. |


Calculates voids that are large enough to contain solvent. Probe/&Aring; adjusts the probe size (think of it as a 'sphere' rolling about the structure - a smaller sphere will fit into smaller gaps and therefore return a larger void than a larger sphere would). The Grid/ANGST is the resolution of the map that will be explored when calculating the voids. If the resolution is too high, the calculation might take a Very Long Time at not much benefit. Click on Void to toggle between displaying and not displaying solvent accessible voids. On the graphics screen the size of any solvent accessible voids that are found will be displayed.


# masks-help


# Masks
The Masks option serves as an alternative to SQUEEZE which is implemented in Platon !!!More Info Online!!!. These sorts of approaches should only be used when the solvent can't be identified or modelled, effort should be made to try and identify or model solvent. If refinement has been attempted using both ShelXL and olex2.refine the option to select either olex or an fcf files, ensure that the file from the last cycle of refinement is used.









### Select Volume
A box with moveable sides will appear. Left-click on the coloured areas and then move the sides while pressing the **SHIFT** key. The map will be calculated only inside the defined box. You can delete the box by right-clicking on it and select 'Hide'.
