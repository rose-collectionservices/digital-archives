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
[Capturing Data from Optical Discs policy](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Optical_Disc_Policy.md).

**NOTE:** Check to see if the CD is a *CD-R* or a *CD-RW*. If the CD is a **CD-RW**, you will need to create a TAR file, using [these instructions](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Imaging/TAR_Files.md). 

[Back to top](#table-of-contents)

---

### CAPTURE DISK IMAGE USING GUYMAGER:
1. Switch to the BitCurator side of the machine. See [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions. 
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
1. Switch to the Windows side of the machine. See [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions. 
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
	a. The forensically packaged disk image (.iso)
	b. The ``fiwalk.xml`` file
	
### Copy files:
	
7. On the desktop, look for **copy.bash** and click on it to open. 

The file should look like this:
	
::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/
	
	for i in [MSSnumber]_{[ID]..[ID]}
		do
		cp ./$i/*.iso ./$i/*.xml 
		./[new netID folder]/$i
		done
		
8. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to copy. 
		
*For example*::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/
	
	for i in 123_{01..05}
		do
		cp ./$i/*.iso ./$i/*.xml ./bedwa/$i
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

# Ingesting Optical Discs into the Keep

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
- The following steps can be performed from your own computer and do not require that you be in the Digital Archives Lab. 

**Ingest Bag into the Keep:**

1. Log into the Keep at https://keep.library.emory.edu.
2. Click *ingest uploaded content*.
3. In the Collection box, begin typing the collection name and select the correct one from the list that pops up.
4. From the File to ingest drop-down menu, select the first of your Bags.
5. Hit Submit.

**Complete Keep object metadata record:**

6. Click on the newly-ingested object’s PID in order to view its metadata record.
7. Complete **Descriptive Metadata**:
- The following fields should auto-populate:
- Collection
- Title
- Resource Type
- Genre
- Identifier

- Refer to the floppy disk label. If the label contains any notes regarding dates or content, 
enter them where relevant.
- Dates can be added to the *Covering Dates* field. Neither a date range nor full dates are required, so add as 
much or as little information as you have.
- Other label information can be added to the Abstractfield.

8. Complete **Technical Metadata**:
- The following fields should be completed:
  * **Imaging Date:** Enter the date on which you imaged the disk.
  * **Creating Application:** From the drop-down menu, select the application used to create the disk image. For all of our 
optical disks, this will be *Guymager (BitCurator 1.0) 0.7.3-1*.
  * **Original Environment Software:** Type *None* in all three Original Environment Software fields.
  * **Hardware Name:** Type *CD* or *DVD*.
  * **Hardware Type:** Select *removable media* from drop-down menu.
  * **Other information:** Type *Imaged using Guymager in BitCurator environment*.
9. Complete **Rights Metadata:** 
- The following field should be completed:
  * **Access Status:** Select *13: Metadata only* from the drop-down menu*.
10. Hit *Save*.

[Back to top](#table-of-contents)
