# Tier 3 - Full Processing with Restrictions
Tier 3 processing is done by digital archives staff **only**, as these collections are normally very large or complex, are expected to be heavily used, or have unique restrictions that require more attention. The decision to process collections at Tier 3 is generally made based on information gleaned during Tier 1 and plans for the collection as a whole. In most cases, hybrid collections prioritized for granular processing should have their born-digital components processed at Tier 3 and integrated into the overall intellectual arrangement. If a granularly processed hybrid collection has only a small amount of born-digital content, or that content is relatively homogeneous, it might be appropriate to process the digital content at Tier 2/2b instead of Tier 3.

To process at the Tier 3 level, begin with steps 1-7 of the [Tier 2 instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Processing%20Tiers/Tier%202.md). After step 7, deduplication, follow the additional steps below. While the Tier 3 steps are similar to those for [Tier 2b](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202b), there are some key differences: restrictions and arrangement. 

Restrictions set by the donor and outlined in the Deed for physical material should be carried over to born digital materials, unless explicitly stated otherwise. There may also be cases where there are additional restrictions on born digital material, separate from physical material. For more information about arrangement, see [part 10, Arranging Files](#arranging-files).

**Note:** To open links in a new tab, right-click (Cmd+click on Mac) on the link.

# Table of Contents
8. [Bulk Reviewer/BulkExtractor](#bulk-reviewerbulkextractor)
9. [Normalizing Files](#normalizing-files)
10. [Arranging Files](#arranging-files)
11. [TAR Files](#tar-files)
12. [Bagging Files](#bagging-files)
13. [Directory Listing](#directory-listing)
14. [Uploading to Keep](#uploading-to-keep)
15. [Finding Aid Edits](#finding-aid-edits)
16. [Upload to Reading Room Server](#upload-to-reading-room-server)

[Examples](#examples)

---

## Bulk Reviewer/BulkExtractor
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
1. [Official Bulk Reviewer documentation](https://bulk-reviewer.readthedocs.io/en/latest/) (Right-click to open in new tab) 
2. [Bulk Reviewer GitHub page](https://github.com/bulk-reviewer/bulk-reviewer) (Right-click to open in new tab)

*Notes:* 
* Bulk Reviewer is already downloaded on the lab computer. The application is in the Forensics and Reporting folder on the desktop. Bulk Extractor is located in the same folder, and comes pre-installed in BitCurator. 
* Following the official documentation is the easiest way to use Bullk Reviewer. 
* If using a regular expressions text file to search for specific terms or topics that are restricted, make sure it is placed on the Desktop and then copied to the hard drive once the scan is complete. 
* For the regular expressions file, use only one word per line. Phrases or names like "Billy Bob Joe" will need to be on a single line each. There will also need to be a capital version and a lower-case version (ex. "Bob" and "bob"). There is no need for quotation marks within the text file itself. </br>
*Example:* </br> ```Billy```</br> ```billy``` </br> ```Bob``` </br> ```bob``` </br> ```Joe``` </br> ```joe``` </br>
*Note:* This will often bring up other content, but Bulk Reviewer has a preview function which shows in-context placement, so you can quickly identify if it needs to be restricted or not. </br>
* Save any reports to a folder on the Desktop (ex. BurkeBR), since it doesn't like to save to the hard drive due to the naming convention of the hard drive. 
* Sometimes there will be an error code, but it will still show the results. Sometimes it's really an error code, so keep an eye on it. 

[Back to top](#table-of-contents)

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
3. In the other window, navigate to the *WorkingFiles* folder. 
4. In the WorkingFiles folder, navigate to the individual folders and copy the files in there past the ```[root]``` folder (if applicable). If there are any folders in the directory, copy those as a whole. 
5. In the *[MSS_ID]_[title_statement]* folder, create folders either: (a) by material type (floppy disks and optical discs, hard drive model, etc), or (b) arrange to match series arrangement. 
6. In the *[MSS_ID]_[title_statement]* folder, paste the files copied directly into where they belong. 
7. Repeat this process for the rest of the individual folders in WorkingFiles. 
a. If there are any files noted by Windows as duplicates, select **See details for all files** in the pop-up window. Select **BOTH** checkboxes at the top of the list to select both copies of the materials. Windows will automatically append a "(1)" to the end of the original file title. 

[Back to top](#table-of-contents)

---

## TAR Files
1. In [collectionName]_workingFiles, create a folder called [MSS]files
2. Create TAR files for the Original Disk Images and the Working Files folders </br>
•	Create TAR file containing both of these folders/files following [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Imaging/TAR_Files.md) (Right-click to open in new tab)
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
*Staff: Follow [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md)(Right-click to open in new tab) to upload the bagged file into the Keep. Below is the corresponding metadata to enter into the form in the Keep. *</br>
1. **Abstract:** *TAR file of files brought to Tier 3 processing, MD5 file, and original disk image*
2. **Imaging Date:** put the date the bag was created
3. **Hardware:** put the summation of the media, without count
4. **Other Information:** put *Originally [number of media (six optical discs, 120 3.5” floppy disks, etc.); summation of collection.*

[Back to top](#table-of-contents)

---

## Finding Aid Edits
*This step should take place in the Windows environment, or on a shared department computer with access to Oxygen XML. Talk with Elizabeth Russey Roke to gain access. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>

1. *Extent:* at end have “[amount] born digital material ([# files])
* *To find out the size and number of files:* In Windows, right-click on the *[MSS_ID]_[title_statement]* folder and select *Properties*. A new window will appear with size information and the number of files and folders. For the MB/GB amount, choose the first one (size).
2. *Summary:* make sure “and born digital material” is included
3. *Restrictions on access:* Access to processed born digital materials is only available in the Stuart A. Rose Manuscript, Archives, and Rare Book Library (the Rose Library). Use of the original digital media is restricted.
4. *Appraisal Note (if applicable):* Blank and/or broken disks have been discarded.
5. *Processing Note:* Born digital materials processed, arranged, and described by [name], [date]. Born digital materials include files taken from [list of items]. 
* a. *If finding aid has series:* For information as to how these materials were processed, see the processing note in the description of series [number], Born digital material. *(Or series the born digital material is found in. Add the below note to the **series level** Processing Note)*
* b. *If finding aid does not have series, put this in the main Processing Note area:* Forensic disk images were created from the [material] using [program]. Individual files were extracted using FTK Imager and scanned for viruses using McAfee’s anti-virus software; none were found. Duplicate and system files have been removed, and files were scanned for personally identifiable information; none were found. Collection-level restrictions have also been applied to born digital materials. Text-based files were migrated to PDF using Adobe Acrobat and image files were migrated to JPG using Microsoft Paint. File dates have been changed from the original creation date. Access copies retain original folder titles and file names. 
6. *Scope and content:* Update the scope and content note of the finding aid as a whole and/or within the series description to reflect what types of collection materials are found from the born digital materials. 
7. *Container list XML code:* ```<c01 level="file"><did><container type="box">RRL</container><container type="folder" /><unittitle>Access copies of processed born digital material [Reading room access ONLY]</unittitle></did></c01>```

[Back to top](#table-of-contents)

---

## Upload to Reading Room Server
Talk with the Digital Archivist or Elizabeth Russey Roke to upload to the Reading Room server. 

[Back to top](#table-of-contents)

---

## Examples
* [Alice Walker papers](https://findingaids.library.emory.edu/documents/walker1061/)
* [Rita Ann Higgins papers](https://findingaids.library.emory.edu/documents/higgins1194/)
* [Southern Christian Leadership Conference records](https://findingaids.library.emory.edu/documents/sclc1083/)
* [Eamon Grennan papers](https://findingaids.library.emory.edu/documents/grennan1150/)
* [Tracy K. Smith papers](https://findingaids.library.emory.edu/documents/smith1468/)
* [Alli Royce Soble papers](https://findingaids.library.emory.edu/documents/soble1315/)

[Back to top](#table-of-contents)
