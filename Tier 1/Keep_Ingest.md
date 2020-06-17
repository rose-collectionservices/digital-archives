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
