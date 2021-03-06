# Images
Olex2 can export images in a variety of formats and there are many options available. Atom labelling is also done from here. Options as to what to do if a picture file with the same name already exists are also provided.

## Move Labels
You can move the labels using the left mouse button while holding the **SHIFT** key.

## Delete Labels
In order to delete a label, make sure no atoms are highlighted (hit **Esc** first!) and then select the label(s) you wish to delete and hit the **Delete** key. You can select all labels by pressing **Ctrl+A** after you've selected **one** label.


# Bitmap Images
Olex2 can produce bitmap images of your structures in a variety of formats. There is no limit to the size these bitmap images can take.

## Colour Space
At the moment, Olex2 saves images in the RGB colour space. If you require CMYK images for your publications, you will find many image conversion services available on the web, where you can upload your RGB file and will get a CMYK file back.

## Transparency
You can set the background to the structure as transparent -- but purely white parts of your structure will also become transparent. However, you can set the background of your image to some colour that does not occur in your structure (pink is a good choice) and it then becomes very easy to convert all pixels with that colour to a transparent background in something like PowerPoint. Of course, using professional image processing software also offers many options to achieve a transparent background.

# Bitmap Image Attributes
These are the properties of the image that will be exported from Olex2. All images will end up in the current structure folder and will not contain any text that is displayed in Olex2 (other than labels, of course!)

## Name
If the name box is empty, Olex2 will ask for the filename. Otherwise the given name will be used, regardless of whether the file already exists.

## Formats
The default format is the png file format. This format offers lossless compression and is particularly suited to save images from Olex2 while keeping file sizes quite small. There really is no reason to use any other format at all.

## Size
There is no limit to the size of the exported bitmap file. If the number given is smaller than 100, the size refers to a multiple of the screen-size. Otherwise it refers to the width of the image in pixels.

|`pict fred.png 300`| Creates a png image called **fred.png** with a width of 300px|

## Bitmap Image Trim
The image will be cropped, so that the molecule will fill the image properly.

## Bitmap Atom Label Fonts
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