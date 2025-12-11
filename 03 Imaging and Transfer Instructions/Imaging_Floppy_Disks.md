This page focuses on how to image floppy disks using the KryoFlux. For floppy disks in good condition and with common file systems, it is also acceptable (and often faster) to image using a USB floppy drive and FTK Imager or Guymager in BitCurator (see [instructions for imaging external drives]([digital-archives/Imaging_Instructions/Imaging_External_Drives](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Imaging_External_Drives.md))).

Quick steps for imaging with FTK Imager (to be revised and expanded):
1. Connect floppy drive to host computer, ensure disk's write-protect tab is open, and insert disk.
2. In FTK Imager, click the button with two green pluses ("add all available evidence items").
3. When the list of disks appear, right click on "A:\" and select "Export disk image."
4. Click the "Add" button, select E01, fill in case and evidence numbers with the media identifier (e.g., 1000_01), enter your Emory ID as examiner, and record a description if desired.
5. On the following screen, browse to and select the folder you prepared for the disk image to be stored.
6. Ensure all verification and reporting boxes are checked, then click "Finish."

Before imaging a floppy disk using any method, check for physical damage and make sure the write-protect tab is open.

# Transferring data from floppy disks using the KryoFlux

### Before you begin:

* This workflow uses tools  in Windows. If necessary, restart the Digital Archives Lab workstation and boot to the Windows hard drive. You can find instructions on how to do this [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md). Right click to open in a new tab. 
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

* This workflow uses tools stored as part of the BitCurator suite. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md). Right click to open in a new tab. 
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
