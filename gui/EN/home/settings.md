# H2_SETTINGS-TARGET
General Settings for Olex2

# Atom r
Change the radius of the selected atoms (in PERS mode). Clicking on `SET` will make this the default.

# Bond r
Change the radius of the selected bonds. Clicking on `SET` will make this the default.

# Background
The background of the main Olex2 window can be set in various ways.

## Colour/White
F2 will toggle between the solid colour background (as defined in the scene settings) and a solid white background.

## Graduated Background
F4 toggles between the solid background and the graduated background. The colour of the graduated background can be set with the `grad` command.

# GUI Width
Set the width of the GUI

# GUI left/right
Set whether the GUI should be on the left or right of the screen

# Tooltips
If selected, tooltips will be shown on hovering over items.

# Legend
A pictogram of all current atom types appears in the main window. With the left mouse and the pressedn SHIFT key, this can be moved to any position. This legend can be switched on and off by typing `legend`.

# Info
If selected, more information on a structure is shown in the top panel. The keyboard command for this is `showwindow info true|false`


# Alerts
The `Reset` link will reset all alerts.

# Console Lines
In order to avoid too much clutter on the GUI, we have decided to provide the console output behind the molecule. Here you can set the number of lines of output you would like to see. The command:

`lines 10`

will set the console to only show 10 lines.

`lines -1`

will show all lines.

# Save View
When active, drawing settings such as styles and backgrounds will be saved with the structure. This is somewhat experimental; if things go wrong, you may have to reload the chosen style for that particular structure.

When this option is **not** active, then a structure will be loaded with the same style as the previous structure.


# Close Settings
I have no idea what these things do!

## Swap Solid Colour / White
This toggles between the chosen solid colour and a white background. Also <b>F2</b>

## Graduated Background
This switches the graduated background on or off. Also <b>F4</b>

## Choose Grad Colours
Set the colours for the four corners of the graduated background.


# Modules-Update_Notification-help
If updates to extension modules are availabe, a pop-up box will appear after Olex2 is started. This can be switched off here.
