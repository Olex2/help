# Hfix Quickmodes 
This is one of the older tools in Olex2 and is due for refurbishment soon! 
Common Hydrogen constraints  Hover over the little symbols and it will show you the constraints that will be inserted on the selected atoms (in Shelx-speak!). You can always type the code yourself after having made the selection.

# Toolbar Hydrogen_2 
This is one of the older tools in Olex2 and is due for refurbishment soon! 

## HFIX  
You can enter any HFIX command in the box and then press the button - hydrogen atoms will be placed geometrically on subsequently clicked atoms according to your choice, regardless of the geometry involved. 

## H 'Improve' 
Another command taken straight from the XP syntax. This will move the selected hydrogen atoms along the bond axis to the distance typed in the box (or the one selected from the pre-set values in the drop-down box. The distances in the box are typical bond distances as observed by neutron diffraction. 

`himp 0.983`

# Toolbar Hydrogen_3 
This is one of the older tools in Olex2 and is due for refurbishment soon! 

## Add Hydrogen  
This will geometrically place hydrogen atoms and constrain them depending on the environment the hydrogen atoms are in. If you want to refine them freely, select the atoms and type AFIX 0 `HADD`

## Show Hydrogen Labels  
`labels -h -l` 

## Hide Hydrogen Labels  
`labels -l` 

## Show AFIX constraints  
`labels -h -a`

# Htab Slider
XXX

# Hydrogen Bond Slider
XXX
