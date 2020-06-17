# Tier 2b - Full Processing without Restrictions
Tier 2b processing is done by staff, students, and interns as deemed appropriate. Tier 2b is built upon what was started with [Tier 2](https://github.com/bedwards254/DAprocessingTiers/tree/master/Tier%202). Tier 2b collections are those that contain relevant collection material, and do not have any restrictions put on them as determined in the Deed. These can be large or small, depending on the collection. Once the files are normalized and arranged, follow the [Finding Aid Edits](#finding-aid-edits) and [Upload to Reading Room Server](#upload-to-reading-room-server) sections below and mark the collection as Tier 2b in the shelf list.

**Note:** To open links in a new tab, right-click (Cmd+click on Mac) on the link. 

# Table of Contents
1. [Folder Structure Setup](#folder-structure-setup)
2. [Extraction](#extraction)</br>
•	[Pull down from Keep](#pull-down-from-keep)</br>
•	[FTK Imager](#ftk-imager)</br>
3. [Virus Scanning](#virus-scanning)
4. [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows)
5. [XML Files](#xml-files)
6. [MD5 File Creation](#md5-file-creation)
7. [Deduplication](#deduplication)</br>
•	[FSLint](#fslint)</br>
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

## Folder Structure Setup
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*
1. Connect the hard drive dock to the rear USB port on the computer via USB cable. 
2. The Windows file explorer should automatically open once the hard drive is mounted and recognized by the computer. 
3. In the file explorer, double-click on the *digitalArchives* folder, then double-click the *workingFiles* folder to open it. 
4. Create a folder inside *workingFiles* called [collectionName]_[MSS_ID] (Example: Mackey_1297)
5. Inside of that folder, create 3 folders called: </br>
a. Original Disk Images;</br>
b. Extracted Files; and </br>
c. Working Files
6. In Original Disk Images, create folders for each disk image you’re pulling down from the Keep
7. Copy the folders you just made into Extracted Files

[Back to top](#table-of-contents)

---

## Extraction 
*The following steps should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
### Pull down from Keep
**Staff:** Pull down images from Keep (just images, not any accompanying material) on Windows side. To do this, log into the Keep using your netID, and search for the collection or specific image you want to extract. Once you locate the disk image in the Keep, click on it to open the metadata form. You should see an option to download "Original Disk Image" at the very top - if you do not, talk with Elizabeth Russey Roke to double-check your Keep access level. </br></br>
*Note:* these will pull down with their PID as the identifying title, so be sure to pay attention to which one you are on to click and drag it to the proper folder in Original Disk Images </br></br>
*Note:* If a number is skipped in the Keep files, delete that folder from Original Disk Images and Extracted Files - this means that specific number either did not image or there was an issue uploading into the Keep. Check the Processing Plan for more information. 

### FTK Imager
*Student/Staff:*
**Using FTK Imager in Windows to extract the files**
1. Launch FTK Imager from the Desktop.
2. From the drop-down File menu, select “Add Evidence Item.”
3. Choose “Image File” and click “Next.”
4. Browse to image file in Original Disk Images and click “Finish.”
5. The selected image file will appear in the Evidence Tree Pane. Click the small + mark to the left of the image file. 
6. The next sub-folder down will note the file system in brackets alongside the virtual disk label. Right-click over this sub-folder and select “Export Files.”</br>
a. You’re looking for the [root] folder or the most granular folder you can find. 
•	Note: If all you see is “Unallocated space”, there was an issue with the image, and the folder number can be deleted from Extracted Files ONLY – keep the original disk image
7. Navigate to the Original Disk Images folder and the corresponding ID number for the image you have open, and hit “Enter”
8. Click “OK.”
9. Once the export has finished, a dialogue box will open with details of how many folders and files have been exported. Click “OK.”
10. Continue doing these one at a time, paying attention to what number you are on so it exports to the correct folder in Extracted Files

[Back to top](#table-of-contents)

---

## Virus Scanning
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*
1. Once the files are extracted, select all of the folders in the Extracted Files folder (Ctrl+A)
2. Right click and select “Scan with McAfee Virus Defense”
3. A window will pop up showing how many files are being scanned
4. When done, it will say “Scan: Complete” and have a count of infected files below
5. If any files are infected, let the digital archivist know right away

Copy the files in Extracted Files to Working Files

[Back to top](#table-of-contents)

---

## Switching to BitCurator/Ubuntu from Windows
1. [Instructions here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md) 
2. Eject the hard drive before doing this step, and turn off the hard drive dock OR disconnect the USB cable 
3. Shut down the computer fully when switching between the two

[Back to top](#table-of-contents)

---

## XML Files
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
**Note:** This step involves the original hard drive the images were created on. Locate the corresponding hard drive where the original disk images are stored (See https://emory.box.com/s/ju2ekovp649mi5w0tbkcpegw8oxittbu for an updated list). </br>
1. Before turning on the hard drive dock, insert the hard drive with the original disk images into the **LEFT** slot on the dock. 
2. Turn on the hard drive dock and mount both hard drives in BitCurator (open file directory and click on each hard drive ONCE to mount them). Right-click one of the hard drives and select "Open in new window" so you can see contents of both hard drives simultaneously. 
3. Locate “Copy2.bash” on the desktop and double-click to open in the text editor. 
4. Edit “Copy2” to match the correct file paths to copy all XML files from the collection on the original hard drive to the corresponding folders in Working Files on the new hard drive. </br>
a. To locate the file paths, in the *original* hard drive, select the *digitalArchives* folder, right-click, and select *Properties* from the pop-up list. Check the file path to see if it says *New Volume1* or *New Volume*. If it says *New Volume1*, the code below does not need edits; if it says *New Volume*, edit the *New\ Volume* sections below. </br>

  ```cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collection_diskImages/ ```</br>
  ```for i in [MSS_ID]_{[startNumber]..[endNumber]} ```</br>
   ``` do ```</br>
    ```cp $i/*.xml /media/bcadmin/New\ Volume/digitalArchives/workingFiles/[collectionName]_[MSS_ID]/OriginalDiskImages/$i ```</br>
    ```done``` </br>

*Note:* if a folder was deleted in the steps above because there was nothing in it or didn’t exist in the Keep, these will automatically skip in this process. </br></br>
5. Once copying is complete, eject both hard drives from the computer by clicking the arrow next to their names in the file directory and then right clicking and selecting “Safely Remove Drive”</br>
6. Power off the hard drive dock and eject the left hard drive and put back in the cabinet. </br>
7. Turn back on the hard drive dock and re-mount the hard drive in BitCurator </br>

[Back to top](#table-of-contents)

---

## MD5 File Creation
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.* </br>

*Create MD5 file for Working Files folder*
1. Select all the folders in Working Files
2. Right click and select “Scripts” and then “Calculate MD5 script”
3. A pop-up box will appear showing the progress
4. Once done, a file called md5 will appear in the main Working Files folder
5. Open it to check the file has the MD5 calculations for each folder [link to example?]

[Back to top](#table-of-contents)

---

## Deduplication
*These steps should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
1. On the desktop, click the Forensics and Reporting folder
2. Double click FSLint to launch it

### FSLint
3. Once open, click the “+Add” button at the top left and navigate to the hard drive and Working Files folder. 
4. Double click the first folder in Working Files
5. Remove the “/” from the top box using the “X Remove” button under the “+Add” button
6. Make sure the tab on the left is set to “Duplicates”
7. Click the “Find” button on the bottom left of the screen to start finding duplicates within the one folder
8. In the results screen, right click and choose "within groups," then “select all but newest” then click “Delete” in the bottom right corner.
9. Click “Find” again to make sure everything else got deleted
10. On the left, choose the “Empty Directories” tab and click “Find”
11. Delete all the empty directories which appear
12. Do the same for the “Temp Files” tab
13. Repeat this process for other folders in the collection, removing and adding each one every time
14. Once done with the individual folders, add the Working Files folder as a whole and run the “Duplicates,” “Empty Directories,” and “Temp Files” options against everything at once. This is to triple-check there are no more lingering duplicate files or empty directories in the collection. 

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
•	Create TAR file containing both of these folders/files following [these instructions](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Imaging/TAR_Files.md)
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
*Staff: Follow [these instructions](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Keep_Ingest.md) to upload the bagged file into the Keep. Below is the corresponding metadata to enter into the form in the Keep. *</br>
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
