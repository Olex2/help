# Report Settings
Here is a collection of tools that can help you to form a report about your structure.


# h3-collection-help
# Collection
Enter data collection information here, including **Sample ID**; **Submitter** and **Operator** names; and various dates.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit Cif Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# h3-crystal-help
# Crystal
Enter information here pertaining to the actual crystal used for the diffraction experiment: the systematic name of the compound, crystal colour, crystal dimensions in mm, synthesis method used to make the compound, crytallisation method, and crystal mounting technique.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit Cif Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# Crystal Image
Any photographs taken of the crystal present in the 'movie' folder in the working folder for the structure will be viewable here. A series of photographs (e.g., of the mounted crystal rotating on the goniometer) can be played as an animation by pressing the Play button in this panel.


# h3-diffraction-help
# Diffraction
Enter information about the diffraction experiment here: **Diffractometer** type; other diffractometer/diffraction details (click the **Definition File** link to select a diffractometer from the window that opens); and **Diffraction** and **Cell Measurement** temperatures. Other **Special Details** of the experiment and of the refinement may be typed into the respective boxes provided.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit Cif Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.

# h3-absorption correction-help
# Absorption Correction
Information about the type of absorption correction employed in the experiment (**Type**; **Details** of the correction method; absorption **Tmax** and **Tmin**) will be automatically extracted from files created during the experiment and entered into these boxes. If any information is missing, it can be entered manually here.


# h3-publication-help
# Publication
Enter the following details related to publications here, to be included in the CIF file: **CCDC number** for the structure (if known); **Contact author** and any additional authors on the article (added from the user database); **Journal** name; and **Journal style** (general or Acta Cryst.). Click the **Contact Letter** link to type an entry for the _publ_contact_letter field of the CIF.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit Cif Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# Citations
Olex2 automatically creates literature citations for all software, including plugins, used during structure determination (if invoked through Olex2 or found in the relevant files).


# Reference
Further details about the journal in which the structure is published may be entered here: **CSD Refcode** for the structure (if known); the list of **Authors** on the article; the **Journal** name, **Volume** number, **Page** numbers, and publication **Year**. A **Comment** on the publication may be entered in the final box in this panel.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit Cif Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# h3-source files-help
# Source Files
Olex2 reads your source files, and extracts relevant information to include into the cif file. This process is not always easy, and can result in conflicts. In this section you can inspect which files Olex2 has read.


# Metadata Sources
Sources of CIF metadata.

# CIF-Part-1-help
# CIF Part 1
This section deals with your CIF file. The CIF file contains everything that is known about your structure in a format that has been defined by the IUCr. Getting a complete and correct cif file is vital for the successful publication of your structures in any peer reviewed journals.

Ideally, the creation of the CIF file should be completely automatic and you won't have to worry about it. But just in case, we provide a number of tools here to help you with your CIF files.

## Edit CIF Info
Pressing this button will bring up a text editor, in which all the information that is known about your structure is shown. You can modify the contents of this file and even add and remove items. Your edits will take precedence over any previous values.

## Merge CIF
This will open the current CIF of your structure - a file in which the 'meta-data' has been merged with the CIF that originated from your last refinement.

## Include/Exclude HKL and RES in your CIF
Here you can determine whether you want to include the HKL/RES files in your final CIF or not. Please note: If you choose 'ignore', then nothing will be done to your CIF - the HKL/RES part will be included **exactly** as it was returned by the refinement program. ShelXL-2013 includes the HKL and RES information as plain text by default. If you select 'exclude', no HKL and res information will be included. If you choose 'include', the RES and HKL information will be included in the official IUCr/CIF definition format: as a loop.


# CIF-Part-2-help
# CIF Part 2
The IUCr offer a free checking service for your CIF files.

## The CheckCif report
This will help you to identify potential problems with your structure. Click the 'CheckCif Report' button to send your CIF file to the IUCr server and obtain your report in either html or pdf format. For a full report, you will also have to send your 'structure factors', which are contained in the fcf file. Tick the box if you want a full report.

## Merge CIF
This tick-box is included here only for the very rare case where you might experience problems with the merging of the CIF created by the refinement program and the information contained within Olex2. If you ever feel the need to untick this box, please make sure to let us know what the problem was and we will try and fix it for everyone. Thanks!

## CCDC Number
The first step in the submission to the CSD is to obtain a CCDC number. Pressing this button will do that for you: it will send your CIF file and your structure factor file (optional) to the CCDC. After a few days of processing in Cambridge, you will obtain an e-mail containing your CCDC submission number. A number will only be requested if **all** the required data is provided - so make sure you fill in all the forms as much as you can!


# CIF-Part-3-help
# CIF Part 3
One of the really strong points of Olex2 is that it will keep your CIF information synchronised throughout the entire solution and refinement process. This is quite a tricky thing to do, but if it all works the way it should, you will never need to edit a CIF by hand again.

## Merge CIF
If this box is ticked, the files that are listed in this line will all be merged with your CIF information. 'metacif' is the builtin-file where Olex2 collects all the information about your structure it can. You can edit this file using the 'Edit Cif Info' button above, and **your edits will take precedence over all other sources of information**. If something goes dreadfully wrong here, you may choose to untick this box. However, we really don't recommend this and if you feel that you need to do this, please contact us and we will try and find a solution to your problem. Thank you!


# Request CSD Number
The structure will be deposited with the CCDC, and you will receive an e-mail shortly containing your CCDC number for this structure. This is the number you need to tell your chosen journal if you are ready to publish.


# Publish as CSD Communications
The structure is not intended for publication in a scientific journal, but I wish to make it available to other scientists through the CSD. I am therefore authorising the CCDC to include this data directly into the CSD. This will happen ASAP.


# CCDC Deposition Options
There are two 'types' of submissions to the CCDC

## Request CSD Number Only
The structure will be deposited with the CCDC, and you will receive an e-mail shortly containing your CCDC number for this structure. This is the number you need to tell your chosen journal if you are ready to publish.

If any structure is not published within three years and no instructions have otherwise been received, the CCDC will attempt to contact you and the corresponding author by e-mail. If no response is obtained, the CCDC will retain the data indefinitely pending future publication. 

## Publish as CSD Communications
The structure is not intended for publication in a scientific journal, but I wish to make it available to other scientists through the CSD. **I am therefore authorising the CCDC to include this data directly into the CSD**. This will happen ASAP.

Please refer to this URL[https://www.ccdc.cam.ac.uk/Community/blog/2018-06-CSDComm1/,BLOG] and these URL[https://www.ccdc.cam.ac.uk/Community/depositastructure/CSDCommunications/,INSTRUCTIONS]
