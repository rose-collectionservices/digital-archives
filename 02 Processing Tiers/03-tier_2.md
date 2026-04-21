# Tier 2(a) - File Extraction and Light Processing
In addition to steps specific to Tier 2, this page contains general steps required to make processed content available for researchers to use. If processing at Tier 2b or 3, leave this page at the point indicated below then return here for the final steps, which are identical for Tiers 2, 2b, and 3.

Tier 2 focuses on making preservation copies of content available for researchers to use and is divided into two sublevels. All processing begins with the first, Tier 2(a); this level is sufficient when no usable content remains at the end of the steps outlined below or when the content that remains is straightforwardly arranged with easily renderable formats and requires no further intervention for access. An archivist may proceed to Tier 2b as necessary, typically when extracted content requires normalization or arrangement beyond original groupings.

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

As of 2026, this is not part of the workflow. Skip it unless a digital archivist indicates it is necessary when working on a legacy collection.

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

### Content Review (required)
At this point, take a look to see if there is anything in the folders that is not system or program files—content with likely research value, like Word files, photographs, etc. If the collection is large or complex, you will likely need to divert to Tier 2b at the point indicated below and complete a more thorough content analysis.

If potentially usable content remains after the Tier 2 steps, proceed to [Tier 2b](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202b) (ingest, description, possible arrangement and normalization) and then, if appropriate, Tier 3 (content review and restriction). 

If you were unable to image or extract content from anything in the collection, or if you found only have out-of-scope material (e.g., system files, software, corrupted files, files we have no viable way to make accessible), use the language below to edit the collection's finding aid to reflect nothing of research value to the collection was found. Mark the collection as Tier 2 in the shelf list and processing stats spreadsheet. 

---

## Finding Aid Edits (complete if no useful content remains, then stop after this step)
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

## Reroute to Tier 2b and/or 3 (if needed)
If the steps above yielded content with research value but it requires normalization, arrangement, restrictions, or other higher-level intervention, pause here to complete those steps before returning to the remaining steps in this workflow.

Go to [Tier 2b - Full Processing without Restrictions](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/04-tier_2b.md).
Go to [Tier 3 - Full Processing with Restrictions](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/05-tier_3.md).

---

## Directory Listing (required)

### Current method, as of 2026
*This step should take place in Windows.*

1. After the ProcessedFiles subfolder is reviewed, arranged, and organized to your satisfaction and you're certain any non-public files have been moved elsewhere, open TreeSize Pro.
2. In the address bar, browse to the appropriate ProcessedFiles folder on the working drive and click the green arrow to begin a scan.
3. When the scan is complete, click the "Export" button in the toolbar.
   1. Browse to the PDI folder on the working drive as the save location, and enter MSS/EUA###_ProcessedFilesInventory.html as the file name.
   2. Make sure the export format is HTML.
   3. Click "Customize Export."
4. In the export options menu that opens, configure the following settings: 
   1. In the export format list on the left, select HTML.
   2. Uncheck all chart and list options except for "Directory Tree."
   3. Make sure "Export Depth" is set to "Full Directory Tree" and "Exported Elements" to "Folders, [Files] item and single files."
   4. Under "Exported Columns," select "Use custom column settings." Choose the following column options: Name, Size, Files, Folders, Last Modified, Type, Folder Path, File Extension.
   5. Click "OK" to save your export settings.
5. Back in the export window, click the "Save" button.
6. Open the resulting HTML file in Notepad or another text editor.
   1. After the title tag, replace the default title with the collection identifier and title (e.g., "EUA 251, Emory University campus buildings and grounds collection").
   2. Farther down, replace the text after the h1 tag with the following heading: [MSS/EUA ###], [Title]: Inventory of born-digital material (as of [today's date] (e.g., "EUA 251, Emory University campus buildings and grounds collection: Inventory of born-digital material (as of 3/10/2026)").
   3. Delete the h3 tag and the content after it identifying the source drive and its capacity.
5. In the collection contain in LIBSAFE Go, upload the HTML file to the PreservationDescriptionInfo folder. 

### Legacy method
*This step should take place in the BitCurator/Ubuntu environment.*

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
## Upload Use Copies for Researcher Access
*This step can take place in either Windows or BitCurator/Ubuntu and requires an internet connection for LIBSAFE Go access.*

Only a digital archivist or trained processing archivist should complete this step, which requires appropriate LIBSAFE Go permissions. 

Note that these instructions describe uploading processed files using the LSG web interface. For large or complex collections, uploading through an S3 client is preferred. See a digital archivist for help.

1. Log into LIBSAFE Go, navigate to the Rose Reading Room (RRR) node, and check in to the "Processed Born-Digital Files" container.
2. Create a folder for the collection, if one does not already exist, following the convention you see used for other collections (MSS/EUA###_TitleStatement).
3. Open the collection folder you just created, click the upload button, click "add files," browse to the ProcessedFiles folder on the working drive, select all of the files/folders within it, and click "open."
4. Check the status window periodically to make sure files are uploading successfully.
5. If ProcessedFiles had any checksum manifests, log files, or other non-public items still present at the time of upload, delete those files from the LSG access copy.
6. Upload a copy of the TreeSize report within the collection folder.

***NOTE: The archivist who uploads the processed files should take care to exclude any restricted files or other content that should not be available in the reading room but is not required to tag files or assign metadata in the RRR node. The digital archivist is responsible for maintaining any metadata needed in this node. These instructions, and possibly the order in which we ingest access and preservation copies, will be revised later when LSG updates their metadata functionality.

---
## Bag Processed Files (required)
*This step can take place in either Windows or BitCurator/Ubuntu.*

Following the [BagIt/Bagger instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/04%20Other%20How-Tos/Packaging_with_BagIt.md), package the ProcessedFiles subfolders as bags. If necessary, you can package the entire ProcessedFiles directory as a single bag.

---
## Ingest Processed Files for Preservation (required)
*This step can take place in either Windows or BitCurator/Ubuntu and requires an internet connection for LIBSAFE Go access.*

### LIBSAFE Go upload (default as of 2026)
1. Log into LIBSAFE Go, navigate to the MSS or EUA node, and open the container created for the collection during Tier 1 processing (or create a new container using the default template if one doesn't yet exist). If needed, rename the top-level directories with the actual collection identifier (the template will populate the folder structure but with placeholder names).
2. Locate any checksum manifests, directory lists, and other documentation from processing on the working drive and upload these to the PreservationDescriptionInfo folder. (If the originals were not bagged prior to ingest, you may decide to add the reports to the Originals subfolders in LSG instead; if the originals were bagged, however, the reports should be stored in the collection's PDI folder so as not to interfere with future bag validation.)
3. Upload the bagged version of ProcessedFiles to the ProcessedFiles folder in the LSG container.
4. Select the bag and use the validate function to ensure it uploaded correctly. 
5. Click through the LSG processing workflow for the container and ensure any remaining steps are complete, including assigning object metadata and creating DO records. (See [LIBSAFE Go documentation](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/03-LIBSAFE_Go_Documentation.md) for details.)

### Keep upload (legacy—do not use)
*This step should take place in the Windows environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
*Staff: Follow [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md) to upload the bagged file into the Keep. Below is the corresponding metadata to enter into the form in the Keep. *</br>
1. **Abstract:** *TAR file of files brought to Tier 2b processing, MD5 file, and original disk image*
2. **Imaging Date:** put the date the bag was created
3. **Hardware:** put the summation of the media, without count
4. **Other Information:** put *Originally [number of media (six optical discs, 120 3.5” floppy disks, etc.); summation of collection.*

---
## Finding Aid Edits (required)
*This step can take place on any computer in any operating system.*

[2026 note: Replace details with links to CS manual sections where appropriate so instructions are less fragmented and easier to maintain.]

Add or updating the following fields in the resource record:
1. *Extent:* at end have “[MB/GB amount] born-digital material ([# files])
* *To find out the size and number of files:* In Windows, right-click on the *[MSS_ID]_[title_statement]* folder and select *Properties*. A new window will appear with size information and the number of files and folders. For the MB/GB amount, choose the first one (size).
2. *Summary:* make sure “and born-digital material” is included
3. *Restrictions on access:* Access to processed born-digital materials is only available in the Stuart A. Rose Manuscript, Archives, and Rare Book Library (the Rose Library). Use of the original digital media is restricted, but media is available to view upon request.
*If you did not normalize the files and know there are some in formats that will not render in LIBSAFE Go, add:* Some digital files might not be accessible in their current form for technical reasons. Contact Rose Library to inquire about alternative possibilities for access.
*If a particular carrier had no useful recoverable content despite successful initial imaging, add a file-level access note:* Due to technical complications, the Rose Library is currently unable to provide access to this unprocessed born-digital material.
4. *Appraisal Note (if applicable):* Blank and/or broken disks have been discarded.
5. *Processing Note:* Born-digital materials processed, arranged, and described by [name], [date]. Born-digital materials include files taken from [list of items]. 
* a. *If finding aid has series:* For information as to how these materials were processed, see the processing note in the description of series [number], Born-digital material. *(Or series the born-digital material is found in. Add the below note to the **series level** Processing Note)*
* b. *If finding aid does not have series, put this in the main Processing Note area:* Forensic disk images were created from the [material] using [program]. Individual files were extracted using FTK Imager and scanned for viruses using McAfee’s anti-virus software; none were found. Duplicate and system files have been removed, and files were scanned for personally identifiable information; none were found. Text-based files were migrated to PDF using Adobe Acrobat and image files were migrated to JPG using Microsoft Paint. File dates have been changed from the original creation date. Access copies retain original folder titles and file names. 
6. *Scope and content:* Update the scope and content note of the finding aid as a whole and/or within the series description to reflect what types of collection materials are found from the born-digital materials. 
7. *Archival object records:* If appropriate, update the AO title and date based on additional information available after processing.
8. *Digital object records:* Create or update the DO records to include all instances of each AO. In most cases, each AO will correspond to one media carrier or file batch and have a single associated DO. That DO might have up to three file versions: one of the unprocessed copy of the content in a preservation repository, one for the processed copy in a preservation repository (if different from the original copy), and one for the user-facing access copy. The DO record and the user-facing file version should be published; any other file versions should remain unpublished. Follow [Emory's metadata guidelines for digital archival objects](https://emory.sharepoint.com/:w:/r/sites/EmoryUniversityLibraries/Shared%20Documents/Staff/Committees%20%26%20Working%20Groups/Metadata%20Policy%20Committee/Archival%20Description%20Sub-Committee/Policy%20Documentation/Metadata%20Guidelines%20for%20Digital%20Archival%20Objects%20in%20ArchivesSpace%20at%20Emory.docx?d=w25158557429b4a4a867cf6fe6fd0946d&csf=1&web=1&e=5tb8UU) when creating DO records and file versions.
9. *Other Finding Aids:* An inventory of the individual born-digital files available in the collection is <extref xlink:href="[TreeSizeReportURL]">available to researchers as an HTML page</extref>. [Not yet implemented—waiting for confirmation on file hosting location.] 

---
## Inventories and Tracking (required)
Once the files are processed, ingested, and described, make sure your work is recorded:
* Mark the collection as Tier 2, 2b, 3 in the shelf list. Update other shelf list fields as needed.
* Update the media log and upload a new copy to the LIBSAFE Go PDI folder.
* Update the annual processing statistics spreadsheet.

---
## Tier 2 Examples
* Morris B. Abram papers
* Elizabeth Dewberry papers
* Horace Mann and Julia W. Bond family papers
* Mari Evans papers
