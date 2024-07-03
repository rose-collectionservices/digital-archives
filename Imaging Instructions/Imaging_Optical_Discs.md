# Table of Contents
* [Review optical disc content](#review-optical-disc-content)
* [Capture disk image using GuyMager](#capture-disk-image-using-guymager)
* [Capture disk image using ISOBuster](#capture-disk-image-using-isobuster)
* [Generating Fiwalk reports, with virus checking](#generating-fiwalk-reports-with-virus-checking)
* [Packaging disk images and supplemental files using BagIt](#packaging-disk-images-and-supplemental-files-using-bagit)
* [Ingesting optical discs into the Keep](#ingesting-optical-discs-into-the-keep)

### REVIEW OPTICAL DISC CONTENT:
1. Launch IsoBuster from the Desktop (Windows side).
2. Insert disc. After a few seconds, the disc’s file tree should load in the IsoBuster window.
3. Review the file tree to identify the contents of the disc:
- a. If the disc contains audiovisual data only, it should be re-routed through the AV workflow;
- b. If the disc contains non-audiovisual data only (e.g., documents, digital photographs), image using Guymager;
- c. If the disc contains mixed-mode data (both audiovisual and filesystem data), image using IsoBuster.

**NOTE:** For more information about the Rose Library’s approach to optical discs, see the 
[Capturing Data from Optical Discs policy](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Optical_Disc_Policy.md). Right click to open in a new tab. 

**NOTE:** Check to see if the CD is a *CD-R* or a *CD-RW*. If the CD is a **CD-RW**, you will need to create a TAR file, using [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Imaging/TAR_Files.md). Right click to open in a new tab. 

[Back to top](#table-of-contents)

---

### CAPTURE DISK IMAGE USING GUYMAGER:
1. Switch to the BitCurator side of the machine. See [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions. Right click to open in a new tab. 
2. Right-click anywhere on the Desktop to create a new folder. Name it collectionName_diskImages_cds 
(e.g., Cleage_diskImages_cds).
3. Insert disc, if not already loaded.
4. Double-click the *Imaging Tools* folder on the Desktop.
5. Double-click *Guymager*.
6. Select the CD/DVD drive from the list.
7. Right-click and select *Acquire image*.
8. In the Acquire image window, complete the following:
- a. Select *Linux dd raw image*;
- b. De-select *Split image files*;
- c. Use the browse button (...) to the right of Image directory to navigate to the folder created at step 2;
    * i. NOTE: Go media/bcadmin/New Volume/ to reach the hard drive properly
- d. Enter an Image filename. Use *MSS#_ID* (e.g., 1000_01).
- e. Check every box underneath Hash calculation / verification (Calculate MD5, Calculate SHA-1, 
Calculate SHA-256, Re-read source after acquisition for verifications (takes twice as long), and Verify 
image after acquisition (takes twice as long))
9. Hit *Start*.

**NOTE:** You can check the progress of disk imaging by scrolling to the right in the Guymager window.

10. In the folder created at step 2, right-click the disk image file and select *Rename*.
11. Change the file extension from *.dd* to *.iso*.

**NOTE:** You can review the disk image contents by right-clicking the object and selecting Scripts > Mount Disk Image. 
The disk image will be mounted on the Desktop. Double-click to open it and view files.

**NOTE:** If you are doing multiple CDs at once, after you load the CD into the drive, hit “Rescan” in the top left corner of 
Guymager to have it appear in the list. 

[Back to top](#table-of-contents)

---

### CAPTURE DISK IMAGE USING ISOBUSTER:
1. Switch to the Windows side of the machine. See [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions. Right click to open in a new tab. 
2. Power on the hard drive dock and create a new folder in the diskImages directory, named 
collectionName_diskImages (e.g., Cleage_diskImages).
3. Launch *IsoBuster*.
4. Insert disc, if not already loaded. After a few seconds, the disc’s file tree should load in the IsoBuster window.
5. Select the disc and right-click to open the *Extraction menu*.
6. Select *Extract CD <Image> > RAW (*.bin, *.iso)*.
7. Navigate to the directory created at step 2 and enter a file name for the disk image. Use MSS#_ID (e.g., 1000_01).
8. From the dropdown menu, change the *Save as* type to *.bin.
9. Hit *Save*.

**NOTE:** If IsoBuster encounters an unreadable sector, an error message will ask if you want to retry imaging, 
select one of four options and proceed with imaging, or quit. One selection will be checked by default 
(probably *Replace with User Data All Zeroes*). Leave the default selection checked and hit *Selection*. 
- *An Error(s) occurred during reading* window will ask if you want to delete the file.
- Click No. 
- Click *Save* on the next window that appears, saving it as a *.cue file. 

[Back to top](#table-of-contents)
9. Complete **Rights Metadata:** 
- The following field should be completed:
  * **Access Status:** Select *13: Metadata only* from the drop-down menu*.
10. Hit *Save*.

[Back to top](#table-of-contents)
