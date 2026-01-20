# Packaging disk images and supplemental files using BagIt

### Before you begin:

* This workflow uses tools stored in BitCurator. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) (Right click to open in a new tab).
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

### Alternative method (Windows):
If you cannot access the content in BitCurator or if you prefer a manual approach for a very small number of disk images, you may use the Bagger GUI tool in Windows. Click "Create New Bag" and select "<no profile>." In the Bag Info frame, add contact name as a field and fill in your Emory ID as the value. Add the folder containing the disk image and manifest files to the payload. When saving the bag, make sure the boxes for md5 bag and tag manifests are checked and "holey bag" is NOT checked. You may choose to bag in place or save as depending on the drive holding the content and the expected bag size. Validate the bag after creating it. This method may also be used when bagging processed files prior to LIBSAFE Go ingest, as the bagging script above is specific to disk images.
