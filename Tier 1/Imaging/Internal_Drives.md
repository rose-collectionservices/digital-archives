## Internal Hard Drives
*Overview*
* This document outlines the tools and steps involved in imaging mediaon drives (hard drives and USB)for archival 
preservation and processing using Guymager.

## Table of Contents
* [Equipment](#equipment)
* [Instructions](#instructions)

[Generating Fiwalk reports, with virus checking](#generating-fiwalk-reports-with-virus-checking)</br>
[Packaging disk images and supplemental files using BagIt](#packaging-disk-images-and-supplemental-files-using-bagit)</br>
[Ingesting packaged content into the Keep](#ingesting-packaged-content-into-the-keep)

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
2. Connect the write blocker to the drivewith both data cable and power cable.
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

---

# Generating Fiwalk reports, with virus checking

### Before you begin:

* This workflow uses tools stored as part of the BitCurator suite. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md).
* Ensure that the Digital Archives Lab workstation is not connected to the Internet by unplugging the ethernet cable.

### Run Fiwalk with the ClamAV plugin:

1. Ensure that the Digital Archives hard drive dock is powered on.
2. Locate **fiwalk.bash** on the desktop and double-click. 
3. The file should look like this: 

::

  	cd /home/bcadmin/.fiwalk

	for i in [MSSnumber]_{ID..ID} 
		do
		fiwalk -c clamconfig.txt -X /media/bcadmin/New\ Volume1/digitalArchives/diskImages/
		[collectionName]_diskImages/$i/fiwalk.xml /media/bcadmin/New\ Volume1/digitalArchives/
		diskImages/[collectionName]_diskImages/$i/$i.img *enter*
		done
		
4. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to scan. 

*For example*

::

	cd /home/bcadmin/.fiwalk

	for i in 123_{01..06}
		do
		fiwalk -c clamconfig.txt -X /media/bcadmin/New\ Volume/digitalArchives/diskImages/
		Mackey_diskImages/$i/fiwalk.xml /media/bcadmin/New\ Volume/digitalArchives/
		diskImages/Mackey_diskImages/$i/$i.E01
		done
		
5. **SAVE** the file and close it. 

	*If you do not save the file, the script will not run correctly*

6. Open a terminal window but right-clicking anywhere on the Desktop and selecting **Open Terminal**.
7. In the terminal, navigate to the Desktop using

    ```cd Desktop```

8. Type **bash fiwalk.bash** and hit **enter**
	
### Review fiwalk.xml:
Using the **virus.bash** file, fiwalk reports can be read for an entire collection in one step. The script searches for the ``<clamav_infected>`` tag within the XML reports, and returns whether there is a ``"Cannot determine file system type"`` error, if there is a virus identified or if the report is clear. If you notice that one or more files are contaminated, consult the digital archivist.

**NOTE:** The *.bash* file and the Python file of the same name must be in the same directory. One does not work without the other.

1. Open the **virus.bash** file. 
2. Edit the file path to direct to the collection folder, similar to how you did above. 
	* If you type an invalid file path and run the file, an error message will appear.
3. **SAVE** the file. 
4. Open a terminal window but right-clicking anywhere on the Desktop and selecting **Open Terminal**.
5. In the terminal, navigate to the Desktop using

    ```cd Desktop``` 

6. Type **bash virus.bash** and hit **enter**
7. The results of the scan will appear in the terminal window. 
	* **NOTE:** This script will run on the entire folder as a whole, so if you're doing a collection in stages, you'll see previous results as well. It's best to wait to run it all at once. 
	* NOTE: If there are no ``<clamav_infected>`` tags in the XML file, the scan result will say ``"Cannot determine file system type"`` error, so those files will need to be inspected further.
  
[Back to top](#table-of-contents)

---

# Packaging disk images and supplemental files using BagIt

### Before you begin:

* This workflow uses tools stored in BitCurator. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md).
* Ensure that the Digital Archives Lab workstation is not connected to the Internet by unplugging the ethernet cable.

### Create folders:

1. Ensure that the Digital Archives hard drive dock is powered on. 
2. Ensure that the Digital Archives hard drive is mounted inside BitCurator. If necessary, double-click the **New Volume** icon in the toolbar on the left-hand side of the screen. Once the Digital Archives hard drive is mounted, a **New Volume** icon will appear on the Desktop.
3. Double-click the **New Volume** icon on the Desktop and navigate to the **Mackey_diskImages** folder.
4. Create a new folder inside the **Mackey_diskImages** folder. Name the folder using your netID or name.
5. Move into the folder created at step 4.

**NOTE:** Before beginning the process of creating bags, each forensically packaged disk image (.E01) must be placed with any supplemental files inside a folder named using the MSSnumber_ID (e.g., 1297_01). There are two ways to create these folders:

To get to the correct directory, in the netID folder you just created, right click and select **Open in Terminal**
	
	
a. Type the following command to create all 20 folders at once and hit **enter**

    mkdir 1297_{[ID]..[ID]}
    
*For example*

    mkdir 1297_{150..170}
	
6. Each folder needs to contain the following files:
	a. The forensically packaged disk image (.E01)
	b. The ``fiwalk.xml`` file
	
### Copy files:
	
7. On the desktop, look for **copy.bash** and click on it to open. 

The file should look like this:
	
::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/
	
	for i in [MSSnumber]_{[ID]..[ID]}
		do
		cp ./$i/*.E01 ./$i/*.xml 
		./[new netID folder]/$i
		done
		
8. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to copy. 
		
*For example*::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/
	
	for i in 123_{01..05}
		do
		cp ./$i/*.E01 ./$i/*.xml ./bedwa/$i
		done
		
9. In the terminal window, navigate to the desktop using 

    ```cd Desktop```

10. Type in **bash copy.bash** and hit **enter**

### Create and Validate a Bag:

11. On the Desktop, locate the file **bagger.bash** and click to open it.

The file should look like this: 

::
	
	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/[netID]
	
	for i in [MSSnumber]_{[ID]..[ID]}
		do
		
		bagit.py --md5 --sha1 --contact-name=[netID] ./$i
		bagit.py --validate ./$i
		echo
		
		done
		
*For example*::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/bedwa
	
	for i in 123_{01..05}
		do
		
		bagit.py --md5 --sha1 --contact-name=bedwa24 ./$i
		bagit.py --validate ./$i
		echo
		
		done

12. Edit the information located in the brackets [] to match your collection information. The ID numbers should equal the folder numbers you are wanting to bag. 
		
13. **SAVE** the file and close it.
	*If you do not save the file, it will not run correctly.* 
	
14. In the terminal window, navigate to the desktop using 

    ```cd Desktop```
	
15. Type in **bash bagger.bash** and hit **enter**

[Back to top](#table-of-contents)

---

# Ingesting packaged content into the Keep

## Move packaged content to the server:

### Before you begin:

* This workflow uses tools stored in Windows. If necessary, restart the Digital Archives Lab workstation and boot to the 
Windows hard drive. You can find instructions on how to do this 
[here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md).

* Ensure that the Digital Archives Lab workstation **is** connected to the Internet by plugging in the ethernet cable if 
necessary. Unlike many of our processes, ingest into the Keep does require a network connection.

### Connect to the VPN:

1. Launch the BIG-IP Edge Client from the Windows by double-clicking the icon pinned  
   to the taskbar at the bottom of the screen.
2. Click **Connect**.
3. Log-in using the stored Emory NetID and password. If no stored log-in details are 
   available, you may contact either John, Carrie, or Elizabeth.  
4. Wait until the connection status has changed to **Connected**. Once connected, the BIG-IP Edge Client window will close automatically.

### Connect to the server via SFTP:

5. Launch Filezilla by double-clicking the Filezilla icon on the Desktop.
6. From the drop-down **File** menu, select **Site Manager...**
7. Find and double-click your netID from the list of sites on the left-hand side of the **Site Manager...** window.
8. Enter your password and hit **OK**.
9. Filezilla will connect to the server.

**Note:** When looking at the Filezilla window, the file tree for your local computer will be listed on the left-hand side. Once connected to the server, you will see the file tree for the server on the right-hand side. Moving files stored locally to the server simply requires that you drag them from the local file tree and drop them into the relevant folder in the server file tree.

### Move Bags to the server:

10. In the local file tree, navigate to your Bags' location. This is probably D:\digitalArchives\diskImages\Mackey_diskImages.
11. One by one, drag and drop your verified Bags from their local folder to the **diskimage** folder on the server side.
12. View the **Successful Transfers** tab at the bottom-left of the Filezilla window to verify that transfer has been completed successfully.

## Ingest Bags from the server into the Keep:

### Before you begin:

* The following steps can be performed from your own computer and do not require that you be in the Digital Archives Lab.

### Ingest Bag into the Keep:

13. Log into the Keep at https://keep.library.emory.edu. 
14. Click **ingest uploaded content**.
15. In the **Collection** box, begin typing **Mackey** and select **1297 Nathaniel Mackey papers** from the list that pops up.
16. From the **File to ingest** drop-down menu, select the first of your Bags.
17. Hit **Submit**.

### Complete Keep object metadata record:

18. Click on the newly-ingested object's PID in order to view its metadata record.
19. Complete **Descriptive Metadata**:
	
	The following fields should auto-populate:
		
	* Collection
	* Title
	* Resource Type
	* Genre
	* Identifier
		
	Refer to the floppy disk label. If the label contains any notes regarding dates or content, enter them where relevant. 
		
	* Dates can be added to the **Covering Dates** field. Neither a date range nor full dates are required, so add as much or as little information as you have.
	* Other label information can be added to the **Abstract** field.
		
20. Complete **Technical Metadata**:
	
	The following fields should be completed:
		
	* **Imaging Date:** Enter the date on which you imaged the disk.
	* **Creating Application:** From the drop-down menu, select the application used to create the disk image. For all of our internal drives, this will be **GuyMager (BitCurator 1.0) 0.7.3-1**.
	* **Original Environment Software:** Type *none* in all three **Original * Environment Software** fields.
	* **Hardware - Name:** Type *Internal hard drive*.
	* **Hardware - Type:** Select **removable media** from drop-down menu.
	* **Other information:** Type *Image created using GuyMager in BitCurator environment*.
		   
21. Complete **Rights Metadata**:
	
	The following field should be completed:
		
	* **Access Status:** Select **13: Metadata only** from the drop-down menu.
		
22. Hit **Save**.

### Repeat for remaining Bags:

23. For each remaining Bag, repeat from step 14.

[Back to top](#table-of-contents)
