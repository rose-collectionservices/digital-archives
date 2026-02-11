# Table of Contents
* [Optical disc policy](#optical-disc-policy)
* [Optical disc imaging workflows](#optical-disc-imaging-workflows)
   * [Review optical disc content](#review-optical-disc-content)
   * [Capture disk image using GuyMager](#capture-disk-image-using-guymager)
   * [Capture disk image using ISOBuster](#capture-disk-image-using-isobuster)

# Optical Disc Policy
This section outlines policy for handling optical discs acquired by the Rose Library as part of manuscript collections. This will help guide decisions as to if and how digital archivists at the Rose capture data from CDs and DVDs.

Upon receiving an optical disc, an archivist reviews its content using [IsoBuster](http://www.isobuster.com), located on the Windows side of the machine.

A disc’s contents will fall into one of four categories:
1. A commercially-produced disc
2. A recordable disc containing only audiovisual data
3. A recordable disc with a single session and a single track containing many filesystems (a typical data CD)
4. A recordable mixed-mode CD, containing both audio and filesystem data

**If the disc in question is a COMMERCIALLY-PRODUCED DISC...**
- No data is captured. Due to copyright concerns, access is restricted.

**If the disc in question is contains ONLY AUDIOVISUAL DATA...**
- The disc enters the AV workflow, managed by Laura.

**If the disc in question is a DATA CD...**
- A raw disk image is created using Guymager.
- The resulting ISO file is bagged and ingested into the Keep using our normal workflows.

**NOTE:** Check to see if the CD is a *CD-R* or a *CD-RW*. If the CD is a **CD-RW**, you will need to create a TAR file, using [these instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Imaging/TAR_Files.md). 

**If the disc in question is a recordable mixed-mode CD...**
- A disk image is created using the BIN/CUE file format, using either FTK Imager or IsoBuster.
- *WHY IS THE BIN/CUE FORMAT REQUIRED FOR MIXED-MODE DISCS?*
1. Unlike single session CDS, mixed-mode CDs store data in multiple sessions and multiple tracks. 
One session will contain audio tracks, the other will contain filesystem data. 
A BIN/CUE file is a multi-part object: the BIN file contains the raw data from the disc, while the CUE file 
contains metadata thatrecordshow the raw file should be broken into sessions and tracks. 
The CUE file is required in order to properly render data from mixed-mode discs.
2. The BIN/CUE format also capturesthe full sector width, unlike an ISO file. This is essential forany discs 
containing audiotracks, as audio dispenses with one layer of error correction and uses the full 2352 bytes for data.

- Current repository infrastructure does not support BIN/CUE files (or any other single multi-part objects). 
As a result, these files should be bagged and stored on Digital Archives Lab storage until ingest becomes possible.

# Optical Disc Imaging Workflows

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
11. Change the file extension from *.dd* to *.iso*. (**NOTE:** As of 2026, renaming files to change their extensions is no longer necessary.)

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
