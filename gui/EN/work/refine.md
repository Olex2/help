# Refinement Program 
Apart from its own refinement engine (olex2.refine), Olex2 also supports all variants of ShelXL. Depending on the refinement package, different refinement methods are available. 

## olex2.refine  
Our own refinement engine. It supports all ShelXL instructions, plus a number of new restraints and constraints that are not available from ShelXL. You can switch between this engine and ShelXL, and Olex2 will not 'forget' the special instructions that are available only in olex2.refine, but of course ShelXL won't heed them. 

## ShelXL-2013  
This is the latest version of ShelXL and is the only version that should be used. In fact, you can use any version you wish, as long as it is on the path and is called 'shelxl'. Our recommendation is to make yourself a folder on the root of one of your drives called 'CrystallographyPrograms' and then put that folder 'on the PATH'. Any (known) executable you place in that folder will be recognised by Olex2 and you will be able to use it from within Olex2 
