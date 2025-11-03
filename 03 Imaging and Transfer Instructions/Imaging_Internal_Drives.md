## Internal Hard Drives
*Overview*
* This document outlines the tools and steps involved in imaging mediaon drives (hard drives and USB)for archival 
preservation and processing using Guymager.

## Table of Contents
* [Equipment](#equipment)
* [Instructions](#instructions)

---

### Equipment

#### Hardware:
##### Write blocker and adaptors
Tableau (Newer)
- Tableau SATA/IDE Bridge
- Tableau SAS Bridge
- Tableau USB 3.0 Bridge
- Tableau FireWire Bridge
- Various cords and connectors

UltraBlock (Yellow Case)
- UltraBlock II eSATA IDE/SATA
- UltraBlock SCSI
- UltraBlock USB

Host machine 
- PC workstation 

External storage drive

#### Software:
- Guymager (available as part of the BitCurator suite) 

#### Other:
- Various screwdrivers, wrenches, storage bins, etc.
- Dr. Cool Multi Functional Router Cooler(if needed)

[Back to top](#table-of-contents)

---

### Instructions

#### Prepare media for imaging:
For internal hard drives this involves extracting the drive from the machine:
1. Locate the computer’s model and/or serial number. The model number should be on the machine; on a Mac the serial 
number should be under the battery.
2. Conduct an online search using the model/serial number(s) to confirm hardware specs. Based on the search results:
- a. Document any known issues relating to the hardware.
- b. Identify the type of hard drive:
  * i. SATA(solid state drive; launched c.2003 and currently the most common hard drive used in desktop and laptop computers)
  * ii. IDE/ATA(same format as SATA drives, but with a slightly different span; adopted as a standard in 1990 but now less 
common in modern computers)
  * iii. SCSI(Small Computer System Interface; 25 different versions; connects to host computer via SCSI-3 Interface Cable)

3. Conduct an online search for instructions on how to replace or remove the hard drive from the hardware model identified.
4. After selecting the most useful online resource, follow the instructions on how to remove the drive.
- a. Use small bins to store and track parts as you remove them. This will help you reconstruct the machine, if necessary.

#### Prepare host computer for imaging:
Ensure that the host computer is not connected to the Internet. Be sure to launch BitCurator prior to connecting the 
drive, write blocker, and host computer. 

**Connect drive, write blocker, and host computer:**
1. Locate the correct write blocker and appropriate connectors in the write blocker kit. Use the associated Tableau card 
to look for what’s needed.
2. Connect the write blocker to the drive with both the data cable and power cable.
3. If imaging an internal hard drive, use the Dr. Cool Multi Functional Router Cooler to elevate and cool the drive 
during the imaging process.
4. Connect the write blocker to the host computer.
5. Connect the write blocker to a power source and switch on. Do not turn on the write blocker before it is connected 
to the drive and host computer.
6. Once switched on, it may take the write blocker a few seconds to recognize both the drive and thehost computer. 
- a. LED lights on the write blocker will indicate if and when the host computer and drive have been recognized.
- b. The USB write blocker will not recognize disk drives until a disk has been inserted.
- c. If unsure as to whether BitCurator recognizes the connected drive, click on the small USB icon in the lower 
left-hand side of the BitCurator window.

**Image drive:**

Creating a physical image:
1. First, mount the drive. Right click on the icon which appears on the task bar on left of the screen and click 
“Safe Mount” OR double-click the icon
2. Launch Guymager (Desktop\Imaging and Recovery\Guymager).
3. In the Guymager window, select the correct drive and right click to bring up the imaging menu. Select “Acquire image.”
4. Select “Expert Witness Format, sub-format Guymager (file extension .EXX)” as file format and enter basic metadata, as 
relevant. Refer to Metadata Guidelines for guidance:
- Under “Split,” type in an amount above what the total of the drive says it is. Ex. 5 GB on a 4GB drive, 
to make sure it doesn’t split.
- *Case Number:* Record ID (MSS# then _ then a successive 2 or 3 digit number)
- *Evidence Number:* Disk Number/Title 
- *Examiner:* Imager’s Net ID (e.g., dwaugh, elfarr)
- *Description:* Brief description of media (e.g., collection name and type of drive it is, and number if 
applicable (Rita Ann Higgins flash drive 1)) and physical label, if applicable.
- *Notes:* As needed

5. Browse to directory in which newly created image will be stored.
- a. Instructions for getting to hard drive PC:
  * i. Use the browse button (...) to the right of Image directory to navigate to the folder created at step 5;
  * 1. **NOTE:** Go media/bcadmin/New Volume/ to reach the hard drive properly
- b. Back in Guymager, select newly created folder as image directory.
6. Enter file name for the image. The file name should be the record ID (MSS# then _ then a successive 2 or 3 digit number). 
If there is a virtual disk label, include this in the file name as well (MSS#_virtual disk label_successive 2 or 3 
digit number, e.g., 1061_AlicesDisk_01).

7. The information file name will automatically populate with whatever file name is entered for the image. This will be 
the file name for the metadata generated by Guymager.
8. Select all check boxesat the bottom(“Calculate MD5,”“Calculate SHA-1,”“Calculate SHA-256,”“Re-read source after 
acquisition for verifications (takes twice as long),”and “Verify image after acquisition (takestwice as long)”)
9. Hit “Start”

**NOTE:** You can check the progress of disk imaging by scrolling to the right in the Guymager window.

**NOTE:** You can review the disk image contents by right-clicking the object and selecting Scripts > Mount Disk Image. The disk 
image will be mounted on the Desktop. Double-click to open it and view files.

[Back to top](#table-of-contents)
