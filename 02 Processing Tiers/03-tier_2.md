# Tier 2 - File Extraction and Light Processing
Record Tier 2 actions and observations in a .txt readme file, digital processing plan, or media log spreadsheet (recommended for large, complex collections). 

---

## Workspace Setup (if needed)
*This step should take place in the Windows environment. See [Switching between BitCurator and Windows](https://github.com/rose-collectionservices/digital-archives/blob/master/04%20Other%20How-Tos/Switching_BitCurator_Windows.md) for instructions.*

1. Place selected hard drive in dock, connect the dock to a USB port on the computer, and power on the dock. The Windows file explorer should automatically open once the hard drive is mounted and recognized by the computer.
2. If a folder for the collection doesn't already exist, follow the instructions in [Setting Up Folders](https://github.com/rose-collectionservices/digital-archives/blob/master/04%20Other%20How-Tos/Setting_Up_Folders.md) to create a collection folder with three subfolders (for original files, extracted files, and working files). 
3. In the ExtractedFiles folder, create subfolders for each disk image/batch you successfully transferred and expect to extract content from. *If a number is skipped in the Keep files, delete that folder from Originals and ExtractedFiles. This means that specific number either did not image or there was an issue uploading into the Keep. Check the media log or processing plan for more information.*
4. Ideally you will be working on the same hard drive used during Tier 1 and therefore already have the disk images/logical copies on hand. If they are no longer on the working drive or you don't have enough space on drive used for Tier 1, start by downloading the preservation copies from the relevant repository and putting them in the appropriate subfolder under Originals:
 * Pulling down from Keep
   *  Log into the Keep using your netID and search for the collection or specific image you want to extract.
   *  Once you locate the disk image in the Keep, click on it to open the metadata form. You should see an option to download "Original Disk Image" at the very top. If you do not, talk with Katherine Fisher to double-check your Keep access level.
   *  Download only the disk image or tar file, not any accompanying material.
   *  Place the downloaded file into the appropriate location in the Originals subfolder.
   *  *Note that these will pull down with their PIDs as the identifying titles, so be sure to pay attention to which one you are on and make sure it goes into the proper folder.*
 * Pulling down from LIBSAFE Go
   * Log in and navigate to the appropriate collection container.
   * Check in to explore content, then right click on each disk image or folder you need and choose "download."
   * Place the downloaded file into the appropriate location in the Originals subfolder.

---

## Extraction (required)
*The following steps should take place in the Windows environment.*

The instructions below assume you are extracting files from a disk image. If the files were transferred as a logical copy, a tar file, or any other non-disk-image form, you may use TeraCopy, 7-Zip, or another appropriate tool to copy a usable version of the content from Originals to ExtractedFiles. See a digital archivist for help.

**Using FTK Imager in Windows to extract the files**
1. Launch FTK Imager from the Desktop.
2. From the drop-down File menu, select “Add Evidence Item.”
3. Choose “Image File” and click “Next.”
4. Browse to image file in Originals and click “Finish.”
5. The selected image file will appear in the Evidence Tree pane. Click the small + mark to the left of the image file. 
6. The next sub-folder down will note the file system in brackets alongside the virtual disk label. Right-click over this sub-folder and select “Export Files.”</br>
a. You’re looking for the [root] folder or the most granular folder you can find. 
•	Note: If all you see is “Unallocated space” or "Unrecognized file system", there was an issue with the image, and the folder number can be deleted from ExtractedFiles ONLY – keep the original disk image
7. Navigate to the ExtractedFiles folder and the corresponding ID number for the image you have open, and hit “Enter”
8. Click “OK.”
9. Once the export has finished, a dialogue box will open with details of how many folders and files have been exported. Click “OK.”
10. Continue doing these one at a time, paying attention to what number you are on so it exports to the correct folder in ExtractedFiles.
11. If you did not generate a fiwalk report (or alternatively, export a directory listing and checksum manifest from FTK Imager) during Tier 1, create reports now.
    * To get a directory listing, right click on the top level of the disk image in the Evidence Tree pane and select "Export Directory Listing." Enter the object/batch ID followed by "_directorylisting" as the file name.
    * To get a checksum manifest, right click on the second level of the tree and select "Export File Hash List." Enter the object/batch ID followed by "_hashes" as the file name.
    * Save both resulting csv files in a convenient place within the collection folder on the working drive—in a PDI folder or at the top level, but preferably not in ExtractedFiles to avoid getting them mixed in with actual collection content. (If the originals were not bagged prior to ingest, you may decide to add the reports to the Originals subfolders in LSG; if the originals were bagged, the reports should instead be stored in the collection's PDI folder in LSG so as not to interfere with future bag validation.)

---

## Virus Scanning (required)
*This step should take place in the Windows environment.*

Note that lab workstations have a Crowdstrike virus and malware detection sensor installed, as required by Emory IT policy. This means most viruses will likely be detected and removed in the background without our knowledge or the ability to record those results in our metadata or collection files. This is not ideal, and we are looking for a solution so we can transparently document any Crowdstrike actions.

Running an additional virus scan so we can view the results ourselves is preferred; however, it is acceptable to record in the log spreadsheet that Crowdstrike was used as the AV tool (with the date of extraction as the AV date, since the scan happens automatically when the computer detects the files).

Legacy practice note: In different points in the past, we've used Avast, McAfee, and ClamAV (as a fiwalk plugin) for this step. These options are not part of the current workflow, and documentation mentioning them may be out of date.

1. Once the files are extracted, select all of the folders in ExtractedFiles folder (Ctrl+A).
2. Right click and select “Scan with Microsoft/Windows Defender.”
3. A window will pop up showing how many files are being scanned.
4. When done, it will indicate the scan is complete and display a count of infected files.
5. If any files are infected, let the digital archivist know right away.

---

## XML Files (legacy—usually not needed)
*This step should take place in the BitCurator/Ubuntu environment.*

As for 2026, this is not part of the workflow. Skip it unless a digital archivist indicates it is needed for work with a legacy collection.

This step involves the original hard drive the images were created on. Locate the corresponding hard drive where the original disk images are stored (see the shelf list or legacy disk image inventory to identify the correct drive).

1. Before turning on the hard drive dock, insert the hard drive with the original disk images into the **LEFT** slot on the dock. 
2. Turn on the hard drive dock and mount both hard drives in BitCurator (open file directory and click on each hard drive ONCE to mount them). Right-click one of the hard drives and select "Open in new window" so you can see contents of both hard drives simultaneously. 
3. Locate “Copy2.bash” on the desktop and double-click to open in the text editor. 
4. Edit “Copy2” to match the correct file paths to copy all XML files from the collection on the original hard drive to the corresponding folders in WorkingFiles on the new hard drive. </br>
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

---

## WorkingFiles Preparation and MD5 File Creation (required)
*This step should take place in the BitCurator/Ubuntu environment.*

You might have previously created checksum manifests during fiwalk or FTK Imager steps, but this step should be done anyway and will result in a single list for all extracted files. If you need an alternative method, such as a Windows-based tool, talk to a digital archivist.

1. Copy all the folder and files in ExtractedFiles to WorkingFiles. Anything you do from this point forward to weed, arrange, or otherwise alter the files should happen in WorkingFiles. ExtractedFiles should remain untouched in case you need to backtrack.
2. Select all the folders in WorkingFiles.
3. Right click and select “Scripts,” "File Analysis," and then “Calculate MD5.”
4. After the script runs, a file called md5 should appear in the main WorkingFiles folder.
5. Open it to make sure the script ran recursively and the file appears to have md5 checksums for all items.
6. Rename the file as MSS/EUA###_WorkingFiles.md5 and save the file in PreservationDescriptionInfo to upload to the collection's PDI folder in LSG.

---

## Content Review and Weeding (if needed, using one or more methods)

### Deduplication with FSLint
*This step should take place in the BitCurator/Ubuntu environment.*

1. On the desktop, click the Forensics and Reporting folder.
2. Double click FSLint to launch it.
3. Once open, click the “+Add” button at the top left and navigate to the hard drive and WorkingFiles folder. 
4. Double click the first folder in WorkingFiles.
5. Remove the “/” from the top box using the “X Remove” button under the “+Add” button.
6. Make sure the tab on the left is set to “Duplicates.”
7. Click the “Find” button on the bottom left of the screen to start finding duplicates within the one folder.
8. In the results screen, right click and choose "within groups," then “select all but newest” then click “Delete” in the bottom right corner.
9. Click “Find” again to make sure everything else got deleted.
10. On the left, choose the “Empty Directories” tab and click “Find.”
11. Delete all the empty directories which appear.
12. Do the same for the “Temp Files” tab.
13. Repeat this process for other folders in the collection, removing and adding each one every time.
14. Once done with the individual folders, add the WorkingFiles folder as a whole and run the “Duplicates,” “Empty Directories,” and “Temp Files” options against everything at once. This is to triple-check there are no more lingering duplicate files or empty directories in the collection. 

### Size and format analysis with TreeSize Pro
*This step should take place in Windows.*

1. Open TreeSize Pro and scan the WorkingFiles folder.
2. In the results, look for files or folders that are particularly large, possibly duplicative, in problematic formats, etc. At this stage, do not assess or make decisions about individual files, but look for patterns and problem areas.
3. If you find folders that are clearly out of scope, delete them from WorkingFiles.
4. If you notice anything that requires more careful review or intervention, flag it and consider taking the collection to Tier 3.
5. Record any relevant information that will help with writing more accurate description later.

### After weeding
At this point, take a look to see if there is anything in the folders that is not system or program files—content with likely research value, like Word files, photographs, etc. 

If potentially usable content remains after the Tier 2 steps, proceed to [Tier 2b](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202b) (ingest, description, possible arrangement and normalization) and then, if appropriate, Tier 3 (content review and restriction). 

If only system files, program files, or corrupted/unconvertable files are left at this point, use the language below to edit the collection's finding aid to reflect nothing of research value to the collection was found. Mark the collection as Tier 2 in the shelf list and processing stats spreadsheet. 

---

## Finding Aid Edits (if not proceeding to 2b/3)
*This can be done on a regular staff laptop with ArchivesSpace access, although being in the lab to refer to the processing materials and logs can be helpful.*  

Processing Note: 
1. *If the material did not image:* 
```Born-digital materials processed by [name], [date]. No data could be recovered from the [material] due to degradation.```
2. *If image files were successfully created, but nothing usable was extracted:* 
```Born-digital materials processed by [name], [date]. Forensic disk images were created from the [material] using [program]. [Name] attempted recovery of individual files from the images using [program]. No data could be recovered from disks due to degradation. [Alternatively, if data is recoverable but it's all system files, software, etc.: No usable original files were present.]``` 
3. *If something could be imaged but nothing extracted AND there is something that couldn’t be imaged (Mann Bond):* 
```Born-digital materials processed by [name], [date]. Forensic disk images were created from the [material] using [program]. Individual files were attempted to be extracted using FTK Imager and scanned for viruses using McAfee’s anti-virus software; those found were removed. The hard drive from Julia Bond's computer could not be imaged, and no data could be recovered from the floppy disks due to degradation.```
4. *Another example of failed file conversion language (Mari Evans):* 
```Born-digital materials processed by [name], [date]. Forensic disk images were created from the [material] using [program]. Individual files were extracted using FTK Imager and scanned for viruses using McAfee’s anti-virus software; none were found. Files could not be converted due to technological constraints.```

Digital Object Records:
If you ended up with a disk image or other copy stored in a preservation system, even if it's not processed or usable, make sure the AO corresponding with that content has a DO record with an unpublished file version pointing to the preservation copy. Follow [Emory's metadata guidelines for digital archival objects](https://emory.sharepoint.com/:w:/r/sites/EmoryUniversityLibraries/Shared%20Documents/Staff/Committees%20%26%20Working%20Groups/Metadata%20Policy%20Committee/Archival%20Description%20Sub-Committee/Policy%20Documentation/Metadata%20Guidelines%20for%20Digital%20Archival%20Objects%20in%20ArchivesSpace%20at%20Emory.docx?d=w25158557429b4a4a867cf6fe6fd0946d&csf=1&web=1&e=5tb8UU) when creating DO records and file versions.

Access Notes:
Recommended at the collection level when processing doesn't produce usable content for some or all media: "Due to technical complications, the Rose Library is currently unable to provide access to unprocessed born-digital materials.
Recommended at the file level when processing doesn't produce usable content: "Due to technical complications, the Rose Library is currently unable to provide access to this unprocessed born-digital material."

---

## Examples
Morris B. Arbam papers
Elizabeth Dewberry papers
Horace Mann and Julia W. Bond family papers
Mari Evans papers
