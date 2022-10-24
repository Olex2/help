# Quick Drawing Styles

# cell-target
Draw unit cell

# base-target
Display basis vectors

# Quick Drawing Styles
A number of preset drawing styles can be selected using the buttons in this tool tab. The new style will be applied only to the current selection. If no atoms are selected, the style will be applied to all atoms.

## Balls & Sticks
|`pers`| Atoms are shown as perfect spheres. The size of the sphere depends on the radius of the element represented by the sphere. |

## Ellipsoids
|`telp n` where default n = 50%| Anisotropic atoms are shown as ellipsoids. Isotropic atoms are shown as spheres, whose size depends on the Uiso value of the individual atom represented by the sphere. |

## Ellipsoids with hydrogen
Anisotropic atoms are shown as ellipsoids, and hydrogen atoms are shown as spheres with radii proportional to their respective Uiso values.

## Wireframe
|`proj`| The structure model is shown as a wireframe. |

## Sphere Packing
|`sfil`| Atoms are represented as space-filling spheres. |

## Tubes
|`tubes`| The entire model is represented as a set of connected tubes. |

## Polyhedra
|`mask atoms 37`| Shows the structure in a polyhedral representation. |

## Default Style
|`default`| All display settings are reset to their default values. |


# Graphical objects
A variety of tools are provided here to enhance the visualisation of a structure.

## Cell
Toggles the unit cell display. If the structure is not within the unit cell, type '<c>move</c>' to relocate it within the cell.

## Base
Toggles the display of basis vectors.

## Box Function 1
Toggles the display of a translucent box of the same size and shape as the unit cell. The box can be moved and rotated independently of the structure or the unit cell.

## Box Function 2
Select two or more atoms. Clicking this button will toggle the display of a rectanglular parallelepiped enclosing those atoms. This box can also be rotated and moved independently of the structure or the unit cell.

## Align

### View
Click this link to show the suggested best view of the structure.

### Plane
This aligns the view of the structure perpendicular to its mean square plane. Typing '<c>mpln -r<c>' displays the mean plane and prints its equation in the output window. To delete the plane, click on it and press '<c>Delete</c>'.

### Locking Motions
Tick these boxes to prevent zooming, rotating, or translating the model on the screen. Prevent all motions by ticking the **Lock all** box.

# Add Fog
An artificial 'fog' can be applied to the display by clicking the **Add Fog** button. This may be helpful, for example, to emphasise the 3D nature of the structure or to highlight its front-facing portion. The **Front** and **Back** sliders govern the thickness of the 'fog'. Click **Clear Fog** to remove the fog from the display.





# Atom Styles
The visual style of the atom display can be customised. Clicking on the link will display a Periodic Table, from where you can start customising your styles.

## About Styles and Scenes
There are two types of style sheets in Olex2 - one deals with the atom objects (styles) and the other deals with the lighting and background settings (scene). Both have to be carefully tuned to each other in order to get good results. To load or save a style or scene, right-click on the background and then follow the relevant links.

## Modify an Atom Style
Right-click on the atom, then select 'Graphics>Draw Styles'. The form you will see is quite complex, and you will have to experiment with it until you are familiar with what you can do.

## Anisotropic Atoms
By default, the periodic table will open showing anisotropic atoms. Anisotropic atoms consist of the 'sphere' and the 'rims' - the visual properties of which can be set separately (see the drop-down box in the top right-hand corner of the 'Draw Styles' form).

## Isotropic Atoms
When you see the periodic table, type the word 'pers' - and you will see a sphere representation of the atoms. You can now modify the settings for the isotropic view of atoms.

# Bonds
TBI
