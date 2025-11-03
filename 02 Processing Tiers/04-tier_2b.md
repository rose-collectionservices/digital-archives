# Tier 2b - Full Processing without Restrictions
Tier 2b processing is done by staff, students, and interns as deemed appropriate. Tier 2b builds upon what was started with [Tier 2](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202). Tier 2b collections are those that contain relevant collection material and do not have any restrictions put on them as determined in the Deed. These can be large or small, depending on the collection. 

To process at the Tier 2b level, begin after step 7, deduplication, in Tier 2 and follow the additional steps below. Once the files are normalized and arranged, complete the [finding aid edits](#finding-aid-edits), [upload to the reading room server](#upload-to-reading-room-server), and mark the collection as Tier 2b in the shelf list.

**Note:** To open links in a new tab, right-click (Cmd+click on Mac) on the link. 

# Table of Contents
8. [Normalizing Files](#normalizing-files)
9. [Arranging Files](#arranging-files)
10. [TAR Files](#tar-files)
11. [Bagging Files](#bagging-files)
12. [Directory Listing](#directory-listing)
13. [Uploading to Keep](#uploading-to-keep)
14. [Finding Aid Edits](#finding-aid-edits)
15. [Upload to Reading Room Server](#upload-to-reading-room-server)

[Examples](#examples)

---

## Normalizing Files
### In BitCurator/Ubuntu
*To stay in BitCurator/Ubuntu:*
1. Locate the *convertFINAL.bash* file on the desktop. Double-click to open the file in the text editor. 
2. In the text editor, select all of the text and right-click to copy (or do ```Ctrl+C```)
3. In the collection folder, navigate to the WorkingFiles folder. Right-click and select "Open in Terminal"</br>
a. You can also choose each indivudal folder inside WorkingFiles, if that's what you prefer. </br>
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

[Back to top](#table-of-contents)

---

## Arranging Files
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.* </br>
1. In the main collection folder, create a folder called [MSS_ID]_[title_statement] (Example: 1297_NathanielMackeyPapers)
2. Right-click the folder you just created, and choose "Open in New Window." 
3. In the original window, navigate to the *WorkingFiles* folder. 
4. In the WorkingFiles folder, navigate to the individual folders and copy the files in there past the ```[root]``` folder (if applicable). If there are any folders in the directory, copy those as a whole. 
5. In the *[MSS_ID]_[title_statement]* folder, paste the files copied directly, with no organization. 
6. Repeat this process for the rest of the individual folders in WorkingFiles. </br>
a. If there are any files noted by Windows as duplicates, select **See details for all files** in the pop-up window. Select **BOTH** checkboxes at the top of the list to select both copies of the materials. Windows will automatically append a "(1)" to the end of the original file title. 

[Back to top](#table-of-contents)

---

## TAR Files
1. In [collectionName]_workingFiles, create a folder called [MSS]files
2. Create TAR files for the Original Disk Images and the Working Files folders </br>
•	Create TAR file containing both of these folders/files following [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Imaging/TAR_Files.md)
3. Put this TAR file in the [MSS]files folder, along with a copy of the MD5 file created above

[Back to top](#table-of-contents)

---

## Bagging Files
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
1. In BitCurator, mount the hard drive and navigate to the [collectionName]_workingFiles folder
2. Right click inside the folder and select “Open in Terminal”
3. In the terminal, type `bagger.py –md5 –sha1 –contact-name=[netID] ./[MSS]files`
4. Let it run
5. Once it is done running, in the terminal, type `bagger.py –validate ./[MSS]files`
6. A message should appear saying it is valid </br>
•	If not, contact the digital archivist</br>

[Back to top](#table-of-contents)

---

## Directory Listing
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
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

[Back to top](#table-of-contents)

---

## Uploading to Keep
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
*Staff: Follow [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md) to upload the bagged file into the Keep. Below is the corresponding metadata to enter into the form in the Keep. *</br>
1. **Abstract:** *TAR file of files brought to Tier 2b processing, MD5 file, and original disk image*
2. **Imaging Date:** put the date the bag was created
3. **Hardware:** put the summation of the media, without count
4. **Other Information:** put *Originally [number of media (six optical discs, 120 3.5” floppy disks, etc.); summation of collection.*

[Back to top](#table-of-contents)

---

## Finding Aid Edits
*This step should take place in the Windows environment, or on a shared department computer with access to Oxygen XML. Talk with Elizabeth Russey Roke to gain access. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>

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


[Back to top](#table-of-contents)

---

## Upload to Reading Room Server
Talk with the Digital Archivist or Elizabeth Russey Roke to upload to the Reading Room server. 

[Back to top](#table-of-contents)

---

## Examples
* [Thomas Kinsella papers](https://findingaids.library.emory.edu/documents/kinsella774/)
* [Constance W. Curry paper](https://findingaids.library.emory.edu/documents/curry818/)
* [Henry H. and Ella Pearson Mitchell papers](https://findingaids.library.emory.edu/documents/mitchell1018/)
* [AID Atlanta records](https://findingaids.library.emory.edu/documents/aidatlanta1264/)
* [Teri Darnell photographs](https://findingaids.library.emory.edu/documents/darnell1450/)

[Back to top](#table-of-contents)
