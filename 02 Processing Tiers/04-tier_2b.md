# Tier 2b - Full Processing without Restrictions
To process at the Tier 2b level, begin after deduplication in Tier 2 and follow the additional steps below. If you are following these steps as part of a Tier 3 processing project, complete the Tier 3 steps related to restrictions before following the instructions below.

Record Tier 2b actions and observations in a .txt readme file, digital processing plan, or media log spreadsheet (recommended for large, complex collections). 

# Workflow
* [Normalize Files](#normalize-files)
* [Arrange Files](#arrange-files)
* [TAR Files](#tar-files)
* [Bag Files](#bag-files)
* [Directory Listing](#directory-listing)
* [Upload to Keep](#upload-to-keep)
* [Finding Aid Edits](#finding-aid-edits)
* [Upload to Reading Room Server](#upload-to-reading-room-server)

[Examples](#examples)

---

## Normalize Files
The instructions below work best for text and image files. They may be applied to all files in a collection or a subset. 

This step is no longer required in all cases, as most text and image files can be used in their original formats. It is still recommended when files are in uncommon formats and will not be usable by researchers using standard reading room access tools. If the files of concern are not text or image files that can be converted to PDF or JPG using the scripts, a digital archivist will identify alternative tools or suitable manual processes.

### In BitCurator/Ubuntu
1. Locate the *convertFINAL.bash* file on the desktop. Double-click to open the file in the text editor. 
2. In the text editor, select all of the text and right-click to copy (or do ```Ctrl+C```)
3. In the collection folder, navigate to the WorkingFiles folder. Right-click and select "Open in Terminal"</br>
a. You can also choose each individual folder inside WorkingFiles, if that's what you prefer. </br>
4. In the terminal, double-check the file path to make sure the right folder is open in the terminal. 
5. In the terminal, right-click and select *Paste* to paste the previously copied text into the terminal window.
6. Hit *Enter* on the keyboard. 
7. Keep an eye on the terminal window as the script runs, to make sure it doesn't get stuck on anything. If it does, consult the Digital Archivist. 

### In Windows
*[Switch back to Windows](#switching-to-bitcuratorubuntu-from-windows) to normalize the files using Adobe PDF/Paint/GIMP/Excel/Word*</br>
1. For Word and Excel files, select multiple (around 10) files at once, right click and select “Convert to Adobe PDF”</br>
a. To select multiple files at once, select the first one, then hold down the "Shift" key and click the last one you want to select in the group. All the files selected should appear blue. </br>
2. Navigate to the correct folder the PDF should save in, and hit “Save” in the first dialogue box; do the same for the second dialogue box. 
3. For TIFF/BMP/PNG files, right click and choose “Open With...” and choose Paint. Do these one at a time. In Paint, choose “Save As…” and choose JPG. Navigate to the proper folder and hit “Save”
4. For Photoshop/Illustrator files, right click and choose “Open With...” and choose GIMP. Click “Ok” when GIMP asks how to read the file (so, going with normal initial settings). Go to “File” at the top and choose “Export As” and choose JPG as the file type in the pop-up box in the bottom scroll list. Slide the resolution up to 10 and hit “Export” and navigate to proper folder for it to export to. 
5. If you run into an odd or unfamiliar file type, contact the digital archivist for assistance.

---

## Arrange Files
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.* </br>
1. In the main collection folder, create a folder called [MSS_ID]_[title_statement] (Example: 1297_NathanielMackeyPapers). This folder will become the final version of the content and will live as two copies in our systems: one packaged for preservation and ingested alongside the Tier 1/original versions, and one uploaded to an access system for researcher use.
2. If you are maintaining the original groupings of the content by carrier or batch, copy and paste (ideally using TeraCopy) the content of the WorkingFiles into the new [MSS_ID]_[title_statement] folder. Within each disk-level subfolder, move any folders and files past the root folder up to the disk-level directory to reduce the number of unnecessary nested folders. (This is the most common approach except in situations where the original groupings are not meaningful and may in fact impede access. Even entire hard drives can often be handled this way, provided robust scope notes and detailed directory lists are made available to help researchers locate content.)
3. If you are instead arranging files (a) by material type (floppy disks and optical discs, hard drive model, etc.) or (b) to match series arrangement, create folders with the [MSS_ID]_[title_statement] folder based on the planned arrangement. Then copy the content of each individual folder under WorkingFiles into the appropriate new location. (This used to be our standard practice but is now uncommon because it takes more time and obscures provenance.)
4. If there are any files noted by Windows as duplicates as you copy and paste, select **See details for all files** in the pop-up window. Select **BOTH** checkboxes at the top of the list to select both copies of the materials. Windows will automatically append a "(1)" to the end of the original file title.

---

## Directory Listing
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>

[2026 note: Rewrite this section to use TreeSize Pro report instead with the original method as a backup/alternative.]

1. Navigate to the main collection folder, [collectionName]_[MSS_ID]
2. Right-click on the *[MSS_ID]_[title_statement]* folder and select **Open in Terminal**
3. In the terminal, type ```ls -FR > [MSS_ID]_[title_statement].txt```
4. Hit **Enter**
5. When the command is done running, go to the *[MSS_ID]_[title_statement]* folder in the file viewer and select the *[MSS_ID]_[title_statement].txt* file created. 
6. ```Ctrl+X``` the file and navigate to the main *[collectionName]_[MSS_ID]* folder and *Paste* it there. 
7. Double-click the TXT file just copied to open it in the text editor software. 
8. In the text editor, click on the three (3) stacked lines next to the "Save" button in the top right corner. 
9. Click the printer icon in the top middle row of icons. 
10. In the pop-up window, click the extention after "File" near the middle of the window. 
11. Navigate to the [collectionName]_[MSS_ID] folder on the hard drive in the window. 
12. In the window, edit the file name to remove the ".txt" extension and then hit "Enter" on the keyboard. This should close out the printer destination window. 
13. In the remaining window, click "Print" in the top right corner. 
14. For larger documents/collections, wait until the orange progress bar at the top of the text editor is gone to make sure the PDF is finished being printed. 
15. Check to see if the PDF is in the [collectionName]_[MSS_ID] folder on the hard drive and close the text editor. 

---

## Bag Files
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
1. In BitCurator, mount the hard drive and navigate to the [MSS_ID]_[title_statement] folder
2. Place copies of any checksum manifests, directory lists, and  other documentation from processing in the folder
3. Right click inside the folder and select “Open in Terminal”
4. In the terminal, type `bagger.py –md5 –sha1 –contact-name=[netID] ./[MSS]files`
5. Let it run
6. Once it is done running, in the terminal, type `bagger.py –validate ./[MSS]files`
7. A message should appear saying it is valid. If not, contact the digital archivist.

---

## Upload to Preservation Repository

[2026 note: Rewrite this section with instructions for LIBSAFE Go upload instead of Keep.]

*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
*Staff: Follow [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md) to upload the bagged file into the Keep. Below is the corresponding metadata to enter into the form in the Keep. *</br>
1. **Abstract:** *TAR file of files brought to Tier 2b processing, MD5 file, and original disk image*
2. **Imaging Date:** put the date the bag was created
3. **Hardware:** put the summation of the media, without count
4. **Other Information:** put *Originally [number of media (six optical discs, 120 3.5” floppy disks, etc.); summation of collection.*

---

## Upload to Reading Room Server

[2026 note: Rewrite this section with instructions for LIBSAFE Go upload instead of RR server.]

Talk with the digital archivist to upload to the reading room server. The digital archivist will remove any log files or other non-public items prior to upload.

---

## Finding Aid Edits

[2026 note: Add step for creating DO records and replace details with links to CS manual sections where appropriate so instructions are less fragmented and easier to maintain.]

1. *Extent:* at end have “[MB/GB amount] born digital material ([# files])
* *To find out the size and number of files:* In Windows, right-click on the *[MSS_ID]_[title_statement]* folder and select *Properties*. A new window will appear with size information and the number of files and folders. For the MB/GB amount, choose the first one (size).
2. *Summary:* make sure “and born digital material” is included
3. *Restrictions on access:* Access to processed born digital materials is only available in the Stuart A. Rose Manuscript, Archives, and Rare Book Library (the Rose Library). Use of the original digital media is restricted.
4. *Appraisal Note (if applicable):* Blank and/or broken disks have been discarded.
5. *Processing Note:* Born digital materials processed, arranged, and described by [name], [date]. Born digital materials include files taken from [list of items]. 
* a. *If finding aid has series:* For information as to how these materials were processed, see the processing note in the description of series [number], Born digital material. *(Or series the born digital material is found in. Add the below note to the **series level** Processing Note)*
* b. *If finding aid does not have series, put this in the main Processing Note area:* Forensic disk images were created from the [material] using [program]. Individual files were extracted using FTK Imager and scanned for viruses using McAfee’s anti-virus software; none were found. Duplicate and system files have been removed, and files were scanned for personally identifiable information; none were found. Text-based files were migrated to PDF using Adobe Acrobat and image files were migrated to JPG using Microsoft Paint. File dates have been changed from the original creation date. Access copies retain original folder titles and file names. 
6. *Scope and content:* Update the scope and content note of the finding aid as a whole and/or within the series description to reflect what types of collection materials are found from the born digital materials. 
7. *Container list XML code:* ```<c01 level="file"><did><container type="box">RRL</container><container type="folder" /><unittitle>Access copies of processed born digital material [Reading room access ONLY]</unittitle></did></c01>```

Once the files are processed, ingested, and described, mark the collection as Tier 2b (or Tier 3, if applicable) in the shelf list and update any applicable inventory notes.

---

## Examples
* [Thomas Kinsella papers](https://findingaids.library.emory.edu/documents/kinsella774/)
* [Constance W. Curry paper](https://findingaids.library.emory.edu/documents/curry818/)
* [Henry H. and Ella Pearson Mitchell papers](https://findingaids.library.emory.edu/documents/mitchell1018/)
* [AID Atlanta records](https://findingaids.library.emory.edu/documents/aidatlanta1264/)
* [Teri Darnell photographs](https://findingaids.library.emory.edu/documents/darnell1450/)
