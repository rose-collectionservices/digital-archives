# Packaging disk images and supplemental files using BagIt

### Before you begin:

* This workflow uses tools stored in BitCurator. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) (Right click to open in a new tab).
* Ensure that the Digital Archives Lab workstation is not connected to the Internet by unplugging the ethernet cable.

### Set up folders:

1. Ensure that the hard drive dock is powered on and the drive is mounted in BitCurator.
2. Open the directory for the collection you're working on and create a new folder inside the [EUA/MSS]###_Originals folder. Name the folder using your netID or name.
3. Before beginning the process of creating bags, each forensically packaged disk image (.E01) must be placed with any supplemental files inside a folder named using the MSSnumber_ID (e.g., 1297_01). Each folder needs to contain the following files:
	a. The forensically packaged disk image (e.g., .E01)
	b. Any log files or manifests generated during imaging or transfer
	c. The ``fiwalk.xml``
4. If folders for each disk already exist in the Originals folder, you can simply highlight them and move them into the netID folder you just created in step 2. If these folders do not yet exist, here is the quickest way to create them:

In the netID folder you just created, right click and select **Open in Terminal**
	
a. Type the following command to create all folders at once and hit **enter**

    mkdir 1297_{[ID]..[ID]}
    
*For example*

    mkdir 1297_{150..170}
	
 file, if applicable
	
### Copy files:
**Skip if your disk images and supplemental files are already located in the appropriate subfolders.**
	
5.  On the desktop, look for **copy.bash** and click on it to open. 

The file should look like this:
	
::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/
	
	for i in [MSSnumber]_{[ID]..[ID]}
		do
		cp ./$i/*.E01 ./$i/*.xml 
		./[new netID folder]/$i
		done
		
6. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to copy. Add any other relevant file extensions to those listed in the script.
		
*For example*::

	cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/
	
	for i in 123_{01..05}
		do
		cp ./$i/*.E01 ./$i/*.xml ./bedwa/$i
		done
		
7. In the terminal window, navigate to the desktop using 

    ```cd Desktop```

8. Type in **bash copy.bash** and hit **enter**

### Create and Validate a Bag:

9. On the Desktop, locate the file **bagger.bash** and click to open it.

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

10. Edit the information located in the brackets [] to match your collection information. The ID numbers should equal the folder numbers you are wanting to bag. 
		
11. **SAVE** the file and close it.
	*If you do not save the file, it will not run correctly.* 
	
12. In the terminal window, navigate to the desktop using 

    ```cd Desktop```
	
13. Type in **bash bagger.bash** and hit **enter**

### Alternative method (Windows):
If you cannot access the content in BitCurator or if you prefer a manual approach for a very small number of disk images, you may use the Bagger GUI tool in Windows. Click "Create New Bag" and select "<no profile>." In the Bag Info frame, add contact name as a field and fill in your Emory ID as the value. Add the folder containing the disk image and manifest files to the payload. When saving the bag, make sure the boxes for md5 bag and tag manifests are checked and "holey bag" is NOT checked. You may choose to bag in place or save as depending on the drive holding the content and the expected bag size. Validate the bag after creating it. This method may also be used when bagging processed files prior to LIBSAFE Go ingest, as the bagging script above is specific to disk images.
