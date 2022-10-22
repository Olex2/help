# Images
Olex2 can export images of a structure in a variety of formats, with many options available in this tool tab. Atoms are also labelled using the tools here.

## File name and format
Enter a name for the image file here or use the default file name provided. Options for dealing with duplicate picture file names are specified here as well. The **Default** file format for saved images is **bitmap**, but other formats may be selected from this drop-down menu.

## Atomic Labels
This attaches customisable labels to individual atoms in the structure. These labels are distinct from the ordinary labels given to atoms during refinement. The **selected** button only labels those atoms highlighted in the graphics window, **non-H** labels all non-hydrogen atoms, and **hetero** labels all atoms other than carbon and hydrogen.

## Symmetry label and Style
The **Symmetry label** drop-down menu offers several options for attaching a descriptive suffix to the labels of atoms related by symmetry to those in the asymmetric unit. The **Style** drop-down menu allows the user to select from a couple of different options for formatting that portion of the atomic label which follows the element symbol.

## Moving and Deleting Labels
Hold down the '<c>Shift</c>' key and drag a label with the left mouse button to move it. To delete a label, first make sure no atoms, bonds, etc. are highlighted (hit ''<c>Esc<c>' to deselect all). Left-click the label(s) to be deleted and hit the '<c>Delete'</c>' key. To select all labels, click on any one label and then press '<c>Ctrl+A</c>'. To delete all atomic labels, click the **DELETE all labels** link.

## Label Colour and Label Box
To alter the colour and appearance of atomic labels, click the **Choose the label colour** link to open a menu for customising a label's colour properties. Click the **Label Box** link to customise the properties of the bounding box enclosing each atomic label.

## Align and Lock

### View and Plane
Clicking on one of these links will orient and centre the structure within the display window, which can be useful before creating images. **View** centres and orients a structure on the screen using an algorithm involving the calculation of the structure's principal axes of inertia. **Plane** calculates a mean plane through the entire structure, orients the structure on the screen perpendicular to this plane, and centres the structure on the screen. Neither of these methods changes the zoom level.
<br>
<br>

A couple of other helpful line commands for realigning the structure on the screen are listed below.

| `center` | Centres the structure without changing orientation or zoom level |

| `compaq -a` | Also centres the structure without changing orientation but does resize the structure to fit within the display area. |

Note: The atom legend can be moved to any desired location on the screen, e.g., closer to the structure, by holding down the '<c>Shift</c>' key and dragging it with the mouse. The legend display can also be switched off or on with the '<c>legend</c>' line command.

### Lock
When working with images, it is sometimes helpful to lock out certain mouse functions to avoid accidentally changing the orientation or zoom. The zoom, rotation, and translation functions can be individually locked by ticking the appropriate box, or all three may be locked simultaneously by ticking the **Lock all** box. For example, if only the **Translation** box is ticked, it will still be possible to zoom in and out and to rotate the structure, but it will remain in a fixed location on the screen.


# Bitmap Images
Olex2 can produce bitmap images of structures in a variety of formats, and there is no limit on the file size of these images. All images produced are in the RGB colour space. If CMYK images are required, e.g., for publication, a separate RGB-to-CMYK conversion tool will be needed. Many such image conversion tools are available on the internet, where an uploaded RGB file is received back as a CMYK file.

# Bitmap Image Attributes

## File Format
Select a file format for your structure image, such as .png or .jpg, from this drop-down menu. The default format is .png (recommended), which involves lossless compression of images and results in relatively small files.

## Transparency
It is possible to set the background for the structure to be transparent, but this will cause purely white parts of the structure also to become transparent. To work around this, set the background of the image to some colour that does not occur in the structure (pink is usually a good choice). Then, convert all pixels of that colour to a transparent background using PowerPoint or other graphics software. If professional image processing software is available, there will be many ways to achieve a transparent background.

## Make Image
Click the **Go!** button to save an image of the structure in the current working folder. The image will not contain any displayed text besides atomic labels. However, the current background will be part of the image. To change to a plain white background, press '<c>F1</c>' once or twice.

# Bitmap Image Attributes1

## Resolution
Set the image resolution in DPI from the drop-down menu or type in a custom value.

## Width
Set the image width in inches or centimetres from the drop-down value or enter a custom width into this box. The image width in pixels will be automatically adjusted, depending on the resolution selected.

## Size
Select a value from the drop-down menu to specify the image width in pixels. The width of the image will automatically be adjusted depending on the resolution selected. It is also possible to type in a custom value into this box. If the value 100 or greater, it is interpreted as the width of the image in pixels; if it is less than 100, it is interpreted as a percentage of the display size. Thus, entering 1000 in the **Size (px)** box will generate an image 1000 pixels wide, but entering 85 will generate an image with a size 0.85 times the display area. There is no limit to the size of the bitmap file created.

|`pict molecule.png 300`| Creates a png image called **molecule.png** in the working folder with a width of 300 pixels. |


# Bitmap Image Trim

## Trim
Ticking this box adds the specified padding and border to the image. Custom values can be entered in all the drop-down menus described below.

### Padding
Adds a white padding around the image of the specified percent thickness.

### Border
Adds to the image a border of the thickness specified in the **Border (%)** drop-down menu and of the color specified in the **Colour** dropdown menu.


# Bitmap Atom Label Fonts
Set the font for the atom labels here.

# Postscript Images
Some would argue that there is no better way to represent a crystal structure on paper than a clear black and white ORTEP drawing. You can make these drawings using Olex2.

## ORTEP
There are very many different options for generating ORTEP-style drawings. Many of these can be set from this GUI, for some more exotic options you may have to consult the manual of Olex2.


# Povray Images
POVRAY is a popular format that exports your structure as a 3-D object. Not only can you do beautiful images with rendered shadows and backgrounds with this, but you can make 3-D animations (provided you know PORVRAY!).
**There are no options here**. Olex2 will export a POVRAY file and you will have to deal with this file yourself!

|`pictPR filename.pov`| Saves the popvray output file 'filename.pov' |

# Image Series
Exports a series of images, that can be put together in a movie.