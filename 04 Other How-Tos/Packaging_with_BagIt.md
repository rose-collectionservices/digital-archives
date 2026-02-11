# Packaging disk images and supplemental files using BagIt

1. Boot the computer into BitCurator. Ensure that the hard drive dock is powered on and the drive is mounted.
2. If needed: Set up a folder for each disk image. See step 4 of [Setting Up Folders](https://github.com/rose-collectionservices/digital-archives/blob/master/04%20Other%20How-Tos/Setting_Up_Folders.md).
3. Ensure each folder named with an original carrier/batch identifier (MSS###_##; e.g., 1297_01) contains the following:
	* Forensically packaged disk image, tar file, or batch of logically transferred files
 	* Any log files or manifests generated during imaging or transfer
 	* A fiwalk.xml file, if applicable
4. On the Desktop, locate the file **bagger.bash** and click to open it.
		The file should look like this: 
	
   		cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/[collectionName]_diskImages/[netID]
	
		for i in [MSSnumber]_{[ID]..[ID]}
			do
		
			bagit.py --md5 --sha1 --contact-name=[netID] ./$i
			bagit.py --validate ./$i
			echo
		
			done
5. Edit the information located in the brackets [] to match your collection information. The ID numbers should equal the folder numbers you are wanting to bag. For example:

   		cd /media/bcadmin/New\ Volume1/digitalArchives/diskImages/test_diskImages/bedwa
	
		for i in 123_{01..05}
			do
		
			bagit.py --md5 --sha1 --contact-name=bedwa24 ./$i
			bagit.py --validate ./$i
			echo
		
			done
		
6. **SAVE** the file and close it.
	*If you do not save the file, it will not run correctly.* 
	
7. In the terminal window, navigate to the desktop using 

    ```cd Desktop```
	
8. Type in **bash bagger.bash** and hit **enter**.

### Alternative method (Windows):
If you cannot access the content in BitCurator or if you prefer a manual approach for a very small number of disk images, you may use the Bagger GUI tool in Windows. Click "Create New Bag" and select "<no profile>." In the Bag Info frame, add contact name as a field and fill in your Emory ID as the value. Add the folder containing the disk image and manifest files to the payload. When saving the bag, make sure the boxes for md5 bag and tag manifests are checked and "holey bag" is NOT checked. You may choose to bag in place or save as depending on the drive holding the content and the expected bag size. Validate the bag after creating it. This method may also be used when bagging processed files prior to LIBSAFE Go ingest, as the bagging script above is specific to disk images.
