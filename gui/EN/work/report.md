# Report Settings
This is a collection of tools to create (a) a report about the structure in HTML format, and (b) a CIF file for the structure.

# h3-collection-help
# Collection
Enter data collection information here, including **Sample ID**; **Submitter** and **Operator** names; and various dates.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit CIF Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# h3-crystal-help
# Crystal
Enter information here pertaining to the actual crystal used for the diffraction experiment: the **Systematic Name** of the compound, if known (enter '?' if unknown); **Colour** (usually extracted automatically from .CIF_OD file); **Size** (dimensions in mm) and **Shape** (crystal description chosen from drop-down menu); synthesis method used to make the compound (**Preparation Details**); **Crystallisation Details** (technique used for growing the crystal); and **Crystal Mounting** technique.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit CIF Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# Crystal Image
Any photographs taken of the crystal present in the 'movie' folder in the working folder for the structure will be viewable here. A series of photographs (e.g., of the mounted crystal rotating on the goniometer) can be played as an animation by pressing the Play button in this panel.


# h3-diffraction-help
# Diffraction
Enter information about the diffraction experiment here: **Diffractometer** type; other diffractometer/diffraction details (click the **Definition File** link to select a diffractometer from the window that opens); and **Diffraction** and **Cell Measurement** temperatures. Other **Special Details** of the experiment and of the refinement (e.g., disorder treatment, solvent masking) may be typed into the respective boxes provided.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit CIF Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.

# h3-absorption correction-help
# Absorption Correction
Information about the type of absorption correction employed in the experiment (**Type**; **Details** of the correction method; absorption **Tmax** and **Tmin**) will be automatically extracted from files created during the experiment and entered into these boxes. If any information is missing, it can be entered manually here.


# h3-publication-help
# Publication
Enter the following details related to publications here, to be included in the CIF file: **CCDC number** for the structure (if known); **Contact author** and any additional authors on the article (added from the user database); **Journal** name; and **Journal style** (general or Acta Cryst.). Click the **Contact Letter** link to type an entry for the _publ_contact_letter field of the CIF.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit CIF Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# Citations
Olex2 automatically creates literature citations for all software, including plugins, used during structure determination (if invoked through Olex2 or found in the source files).


# Reference
Further details about the journal in which the structure is published may be entered here: the **CSD Refcode** for the structure (if known); list of **Authors** on the article; and **Journal** name, **Volume** number, **Page** numbers, and publication **Year**. A **Comment** on the publication may be entered in the final box in this panel.
<br>
<br>

**Information entered in these boxes will take precedence over information provided in other files when the CIF file is written**. If the CIF information is edited using the **Edit CIF Info** button below, then that will take precedence over what is entered here, and those new values will be displayed in these boxes.


# h3-source files-help
# Source Files
This tool tab lists the source files used by Olex2 to construct a CIF file for the structure and prints a warning if there is conflicting information among the sources.


# Metadata Sources
Olex2 searches the working folder for sources of metadata such as diffractometer information and data collection parameters, for incorporation into the final CIF file created for the structure after refinement is complete. Such details are normally recorded during the diffraction experiment in a .CIF_OD file. If no files containing metadata are found, Olex2 prints out a brief message to that effect.


# Metadata Conflicts
Olex2 automatically extracts relevant information from metadata source files for inclusion in the final CIF, but the process is not always straightforward because the sources may contain conflicting information. In this case, Olex2 prints an error message and the user has to resolve the conflicts manually, i.e., choose the correct information source for the CIF data. Collapse the **Report** tab and re-expand it, then resolve the conflicts in the window that opens. Olex2 then prints a message indicating no conflicts remain. The **Show ALL** link lists all the sources of CIF data and the **Reset Previously Resolved Conflicts** link removes any manually entered information (and any previous conflicts will reoccur).


# CIF-Part-1-help
# CIF Part 1
This section deals with the creation and modification of the CIF file. The CIF contains everything known about the structure in a format defined by the IUCr. A complete and correct CIF file is vital for the successful publication of a structure in any peer-reviewed journal. Creation of the CIF is normally handled automatically by Olex2, but these tools are provided in case the CIF needs to be modified.

## Edit CIF Info
Pressing this button will open a file containing all the information that Olex2 will be adding to the CIF file when it is created. Information entered in the above tool tabs (**Collection**, **Crystal**, **Diffraction**, etc.) will appear here. It is possible to modify the contents of this file, and even add or remove entries. Edits made here will take precedence over any other previously entered values, and the values entered using **Edit CIF Info** will appear when the above tool tabs are reopened.

## Merge CIF
Clicking **Merge CIF** will take the metadata from the source files, the tool tabs above, and information entered using the **Edit CIF Info** button, and merge them into the CIF created during the last cycle of refinement. This final CIF will then be opened in the default text editor.

## Include/Exclude HKL and RES in your CIF
Select from the drop-down menu how reflection data and refinement instructions will be included in the final CIF. **Leave as is** includes the .hkl and .res files as returned by the refinement program. ShelXL includes the HKL and RES information as plain text by default. **Include** incorporates the HKL/RES information in the CIF as a loop (IUCr format). **Exclude** leaves out both the HKL and RES information - this option is strongly discouraged.


# CIF-Part-2-help
# CIF Part 2
The IUCr offer a free error-checking service called ~checkCIF~ for validating CIF files.

## IUCr checkCIF Report
Click the **IUCr checkCIF** button to send the merged CIF to this service for checking. The resulting ~checkCIF~ report may be received in PDF or in HTML format (select from drop-down menu). The report helps identify potential problems with the structure. For full validation of both the CIF and the structure factors, it will also be necessary to upload the structure factors as a .fcf file. For this and other ~checkCIF~ options, see the URL[https://checkcif.iucr.org/,checkCIF] website.

## Depositing a structure with the CCDC
There are two types of submissions to the Cambridge Crystallographic Data Centre (URL[https://www.ccdc.cam.ac.uk/,CCDC]).

### Request CCDC Number
Submitting a structure to the ~Cambridge Structural Database~ (URL[https://www.ccdc.cam.ac.uk/solutions/csd-core/components/csd/,CSD]) is now a requirement for most journals. Click this button to send the CIF file and the optional structure factor file to the CCDC. Once the CIF has been processed, a unique CCDC number will be assigned to the structure and sent by email to the depositing author, usually within a few days. This is the number that needs to be provided to the journal in which the structure is to be published.

Note: To expedite processing, it is important that *all* the required data are provided, i.e., the CCDC forms need to be filled out as completely as possible.
<br>
<br>

If any structure is not published within three years and no other instructions have been received, the CCDC will attempt to contact the depositing author and the corresponding author by e-mail. If no response is obtained, the CCDC will retain the data indefinitely pending future publication. 

### Publish as CSD Communication
Sometimes, a structure is not intended for publication in a scientific journal, but is deposited with the CSD to make it available to other scientists. In such cases, it is possible to publish the structure as a "CSD Communication" by authorising the CCDC to include it directly in the CSD. This occurs as soon as the structure is processed by the CCDC.
<br>
<br>

Please refer to this URL[https://www.ccdc.cam.ac.uk/Community/blog/2018-06-CSDComm1/,blog] and these URL[https://www.ccdc.cam.ac.uk/Community/depositastructure/CSDCommunications/,instructions] for more details about CSD Communications.


# CIF-Part-3-help
# CIF Part 3
One of the really strong points of Olex2 is that it will keep CIF information synchronised throughout the entire solution and refinement process. This is quite a tricky thing to do, but if it all works the way it should, it will never be necessary to edit a CIF by hand again.

## Merge CIF 1
This tick-box is included here only for the very rare cases when problems occur in merging CIF data from the refinement program and information obtained by Olex2. If this box is ticked, the files that are listed on this line will all be merged with the CIF information.

## metacif
The **metacif** link opens the file in which Olex2 collects all the information available about the structure. It is also possible to open this file using the **Edit CIF Info** button above, and any edits made will take precedence over all other sources of information, as mentioned earlier. If anything goes dreadfully wrong here with the construction of the final CIF file, untick this box. However, this is really not recommended, and if it ever necessary to untick the box, please send an email describing the problem to support@olex2.org so that the issue can be fixed.

## Add local/default CIF
This features allows information from an external CIF file to be added to the CIF file being constructed for the current structure. Click **local** if the external CIF file is in the current working folder or **default** to access any of the built-in CIF files of Olex2, e.g., to add diffractometer information.

# CIF Part 4
Tick this box to merge **metacif** items even if they have been previously marked for skipping.

# ABS STR
The value of the Flack parameter *x* and Hooft parameter *y* are given here for chiral structures. For a correctly determined absolute structure, both are close to 0. If they are close to 1, then it may be necessary to invert the structure with '<c>inv -f</c>'. Select from the drop-down menu the method used to determine the absolute structure (most commonly it is **Anomalous dispersion**).