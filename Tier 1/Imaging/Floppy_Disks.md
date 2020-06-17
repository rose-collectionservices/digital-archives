# Table of Contents
* [Transferring data from floppy disks using the KryoFlux](#transferring-data-from-floppy-disks-using-the-kryoflux)
* [Migrating KryoFlux image files in preparation for ingest](#migrating-kryoflux-image-files-in-preparation-for-ingest)
* [Generating Fiwalk reports, with virus checking](#generating-fiwalk-reports-with-virus-checking)
* [Packaging disk images and supplemental files using BagIt](#packaging-disk-images-and-supplemental-files-using-bagit)
* [Ingesting packaged content into the Keep](#ingesting-packaged-content-into-the-keep)

---

# Transferring data from floppy disks using the KryoFlux

### Before you begin:

* This workflow uses tools  in Windows. If necessary, restart the Digital Archives Lab workstation and boot to the Windows hard drive. You can find instructions on how to do this [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md).
* **Make sure the Digital Archives' Lab workstation is not connected to the internet.** Unplug the yellow ethernet cord at the back of the computer.
* As you unpack the KryoFlux, pay attention to the labels on the data cable and the KryoFlux enclosure. These will help ensure that the floppy disk drive and the KryoFlux are connected correctly.
* As you are setting up the KryoFlux, avoid placing any drives on the metal shelves over the workstations.

### Set-up instructions:

1. Using the data cable, connect the KryoFlux to the correct floppy disk drive.

   - The data cable has three connectors: one for the KryoFlux; one for 3.5" floppy disk drives; and one for 5.25" floppy disk drives. Each connector on the cable is clearly labelled.
    - The data cable's red wire signifies pin 1. When connecting the data cable to the KryoFlux, be sure to align the red wire with the **Pin 1** label on thestored KryoFlux enclosure.
  
2. Using the USB cable, connect the KryoFlux to the lab workstation.

**Check that the associated driver is correct:**

3. In the Windows Search Box, type `device manager` and hit **enter**.
4. From the list, select **Universal Serial Bus Controllers**. If you see **KryoFlux Disk System** listed here, you can skip to the next section.
5. If you do not see **KryoFlux Disk System** listed, select **Ports (COM & LPT)**.
6. Right-click on **Bossa Program Port**.
7. Select **Update driver software**.
8. Select **Browse my computer for driver software**.
9. Select **Let me pick from a list of device drivers on my computer**.
10. At this stage you should see **KryoFlux Disk System** listed. Select it and hit **Next**. You should see the following confirmation message: **Windows has sucessfully updated your driver software**. Hit **Close**.

### Complete KryoFlux set-up:

**NOTE:** All terminal commands are case-sensitive.

11. Type `cmd` into the Windows Search Box to open a terminal window.
12. Type the following command into the terminal window in order to navigate to the DTC folder and hit **enter**:

    ```cd ..\..\"Program Files (x86)"\kryoflux_3.00_windows\dtc```

13. Type the following command and hit **enter** 

    ```dtc -c2```

**NOTE:** The resulting prompt will likely say: **Control command rejected by the device. CM: maxtrack = 0**.

*Alternate instructions:* 
* On the desktop, locate the folder titled **RunFiles**. 
* Double-click to open, and locate the file **pre-run.bat**. 
* Double-click on **pre-run.bat**, which will open the command prompt and automatically run the above command. 

14. Ensure that the power cable is plugged in and connect the power adaptor to the back of the floppy disk drive.

    - The power adaptor has two connectors: the smaller one is for 3.5" floppy disk drives and the larger one is for 5.25" floppy disk drives. Both are clearly labelled.
    - When working with the 5.25" drive, in particular, be careful to make sure that the adaptor is properly aligned.
    - When disconnecting the adaptors, grip the white plastic piece and not the wires, as these are quite fragile and easily come loose if mishandled.
  
15. Insert a floppy disk.
16. Re-type the following command and hit **enter**:

    ```dtc -c2```

**NOTE:** The resulting prompt will likely say something like: **CM: maxtrack = 83**.

*Alternate instructions:* 
* On the desktop, locate the folder titled **RunFiles**. 
* Double-click to open, and locate the file **pre-run.bat**. 
* Double-click on **pre-run.bat**, which will open the command prompt and automatically run the above command. 

### Capture stream files:

17. Ensure that the Digital Archives hard drive dock is powered on.
18. Type the following command and hit **enter**::

    ```dtc -p -fJ:\digitalArchives\diskImages\[collectionName]_diskImages\[MSSnumber_ID]\[MSSnumber_ID] -i0 -i4 -i9 -l8```

*For example*

  ```dtc -p -fJ:\digitalArchives\diskImages\Lomax_diskImages\785_01\785_01 -i0 -i4 -i9 -l8```

**NOTE:** You may need to double check the drive letter associated with the Digital Archives hard drive dock, as it may not always be ``J:``. If necessary, substitute the correct drive letter at the beginning of the file path.
19. Imaging will begin. Progress will be logged in the terminal window.

### Verify correct encoding format:

20. Review the terminal output to determine which encoding format is correct:

    - Incorrect formats will register as ``unformatted``.
    - The correct format will be listed as ``OK``.
    - If MFM is the correct format, use ``-i4`` in step 21.
    - If Apple DOS 400/800 is the correct format, use ``-i9`` in step 21.
    - If neither format is correct, make a note of this and set disk aside for further review at a later date.
  
### Capture correctly encoded disk image:

21. Type the following command and hit **enter**

   ```dtc -fJ:\digitalArchives\diskImages\[collectionName]_diskImages\[MSSnumber_ID]\[MSSnumber_ID] -i0 -fJ:\digitalArchives\diskImages\[collectionName]_diskImages\[MSSnumber_ID]\[MSSnumber_ID].img -i[4 or 9] -m1 -l8```

*For example*

   ```dtc -fJ:\digitalArchives\diskImages\Lomax_diskImages\785_01\785_01 -i0 -fJ:\digitalArchives\diskImages\Lomax_diskImages\785_01\785_01.img -i4 -m1 -l8```

22. Once imaging is complete, remove the floppy disk from the drive.
23. Label the disk with its MSSnumber\_ID. Be sure not to obscure any original labels.

### Repeat for remaining floppy disks:

24. Insert next floppy disk.
25. Repeat from step 18.

*Alternate instructions:* 
* On the desktop, locate the folder titled **RunFiles**. 
* Double-click to open, and locate the file **run.bat**. 
* *COPY* the file into the *[collectionName]_diskImages* folder. 
* Navigate to the *[collectionName]_diskImages* folder in the command prompt. 
* In the command prompt type **run.bat [MSSnumber_ID]** and hit **enter**. 

This runs both command above in one step. Once it runs, swap out the disks, hit the up arrow and edit the command to go to the next disk number. 

**Time-saving tip:** Use the up arrow to page through commands that you have previously run in the terminal window. Once you have found the correct command, you can edit it as needed before running it again.

### Disconnect the KryoFlux:

26. Click the **Safely remove hardware** icon and select **KryoFlux Disk System**.
27. Once it is safe to remove the KryoFlux, carefully disconnect the power (taking care not to pull on the wires), then the USB cable, and finally the data cable.
28. Replace all components in the KryoFlux box and return to the cabinet.

[Back to top](#table-of-contents)

---

# Migrating KryoFlux image files in preparation for ingest

### Before you begin:

* This workflow uses tools stored as part of the BitCurator suite. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md).
* Ensure that the Digital Archives Lab workstation is not connected to the Internet by unplugging the ethernet cable.

### Locate existing image files:

1. Ensure that the Digital Archives hard drive dock is powered on. 
2. Ensure that the Digital Archives hard drive is mounted inside BitCurator. If necessary, double-click the **New Volume** icon in the toolbar on the left-hand side of the screen. Once the Digital Archives hard drive is mounted, a **New Volume** icon will appear on the Desktop.
3. Double-click the **New Volume** icon on the Desktop and navigate to the **[collection]_diskImages** folder.
4. Open a terminal window but right-clicking anywhere on the Desktop and selecting **Open Terminal**.

### Run the script:

1. Locate *migration.bash* on the desktop and double-click. 
2. The file should look like this: 

:: 

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/

	for i in [MSSNumber]_{ID..ID}
		do
		
		md5sum $i/$i.img >$i/imgMD5.txt
		
		ewfacquire ./$i/$i.img -C "$i" -D "3.5 inch floppy disk" -e “[netID]” 
		-E “[collection title]” -f "encase6" -m "removable" -M "logical" -N "Migration from img" 
		-c "deflate" -o 0 -S "1.4 GiB" -P 512 -g 64 -t ./$i/$i
		
		ewfverify $i/$i.E01 >$i/verify$i.txt
		
		done

3. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to migrate. 

*For example*: 

::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/Mackey_diskImages/
	
	for i in 123_{01..06}
		do 
		
		md5sum $i/$i.img >$i/imgMD5.txt
		
		ewfacquire ./$i/$i.img -C "$i" -D "3.5 inch floppy disk" -e "bedwa24" 
		-E "Nathaniel Mackey papers" -f "encase6" -m "removable" -M "logical" 
		-N "Migration from img" -c "deflate" -o 0 -S "1.4 GiB" -P 512 -g 64 -t ./$i/$i
		
		ewfverify $i/$i.E01 >$i/verify$i.txt
		
		done

*This will run the MD5 checksum, the migration to E01 format, and verify the checksum for img folders/files 01 through 06 in one command.* 

4. **SAVE** the file and close it. 

	*If you do not save the file, the script will not run correctly*

5. In the terminal, navigate to the Desktop using

    ```cd Desktop```

6. Type **bash migration.bash**
7. Hold down **enter** until you are back to the original prompt ($). 

## Review MD5 checksum and verify checksum files

Using the **MD5.bash** file, the MD5 file and verify files created during the migration process can be compared against one another to make sure they are the same values.

**NOTE:** The *.bash* file and the Python file of the same name must be in the same directory. One does not work without the other.

1. Open the **MD5.bash** file. 
2. Edit the file path to direct to the collection folder, similar to how you did above. 
	* If you type an invalid file path and run the file, an error message will appear.
3. **SAVE** the file. 
4. Open a terminal window but right-clicking anywhere on the Desktop and selecting **Open Terminal**.
5. In the terminal, navigate to the Desktop using

    ```cd Desktop``` 

6. Type **bash MD5.bash** and hit **enter**
7. The results of the scan will appear in the terminal window, either "Success!" or "Fail!" next to the folder number. 
	* **NOTE:** This script will run on the entire folder as a whole, so if you're doing a collection in stages, you'll see previous results as well. It's best to wait to run it all at once.
  
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
	b. The ``imgMD5.txt`` file created during migration from a ``.img`` file to a ``.E01`` file
	c. The ``verify[MSSnumber_ID].txt`` file also created during migration from a ``.img`` file to a ``.E01`` file (e.g., ``verify1297_24.txt``)
	d. The ``fiwalk.xml`` file
	
### Copy files:
	
7. On the desktop, look for **copy.bash** and click on it to open. 

The file should look like this:
	
::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/
	
	for i in [MSSnumber]_{[ID]..[ID]}
		do
		cp ./$i/*.E01 ./$i/*.txt ./$i/*.xml 
		./[new netID folder]/$i
		done
		
8. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to copy. 
		
*For example*::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/
	
	for i in 123_{01..05}
		do
		cp ./$i/*.E01 ./$i/*.xml ./$i/*.txt ./bedwa/$i
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
	* **Creating Application:** From the drop-down menu, select the application used to create the disk image. For all of our Mackey floppy disks, this will be **ewfacquire 20140608**.
	* **Original Environment Software:** Type *none* in all three **Original * Environment Software** fields.
	* **Hardware - Name:** Type *3.5" floppy disk*.
	* **Hardware - Type:** Select **removable media** from drop-down menu.
	* **Other information:** Type *Data originally transferred using KryoFlux. Raw disk image file migrated to Expert Witness Format using ewfacquire*.
		   
21. Complete **Rights Metadata**:
	
	The following field should be completed:
		
	* **Access Status:** Select **13: Metadata only** from the drop-down menu.
		
22. Hit **Save**.

### Repeat for remaining Bags:

23. For each remaining Bag, repeat from step 14.

[Back to top](#table-of-contents)
