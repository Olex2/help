# images-target
This tool contains everything that is needed to output your structure as images in various formats.

# Images
Olex2 can export images in a variety of formats and there are many options available. Atom labelling is also done from here. Options as to what to do if a picture file with the same name already exists are also provided.

## Move Labels
You can move the labels using the left mouse button while holding the SHIFT key.

## Delete Labels
In order to delete a label, make sure no atoms are highlighted (hit ESC first!) and then select the label(s) you wish to delete and hit the DELETE key. You can select all labels by pressing CTRL+A after you've selected ONE label.


# Bitmap Images
Olex2 can produce bitmap images of your structures in a variety of formats. There is no limit to the size these bitmap images can take. 

![Hello!](X:\olex2-trunk\etc\documentation\images\EXTERN_0000.png)

## Colour Space
At the moment, Olex2 saves images in the RGB colour space. If you require CMYK images for your publications, you will find many image conversion services available on the web, where you can upload your RGB file and will get a CMYK file back. 

## Transparency
Olex2 does not currently support transparency. However, you can set the background of your image to some colour that does not occur in your structure (pink is a good choice) and it then becomes very easy to convert all pixels with that colour to
