# Generating Fiwalk reports

* This workflow uses tools stored as part of the BitCurator suite. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive.
* Before you begin, ensure that the Digital Archives Lab workstation is not connected to the Internet by unplugging the ethernet cable.

### Current instructions: Run Fiwalk

1. Ensure that the Digital Archives hard drive dock is powered on.
2. Locate **fiwalk.bash** on the desktop and double-click. 
3. The file should look like this: 

::

	for i in [MSSnumber]_{ID..ID} 
		do
		fiwalk -f -X /media/bcadmin/[HDD name]/[path to Originals]/$i/fiwalk.xml /media/bcadmin/[HDD name]/[path to Originals]/$i/$i.[E01]
		done
	
4. Edit the information in brackets [ ] above to match your collection information. The ID numbers should equal
the folder numbers you are wanting to scan. The disk image extension will most often be E01 but might in some cases be dd or something else. If a file path contains spaces, either insert a forward slash before each space or put quotation marks around the entire path. 

*For example*

::

	cd /home/bcadmin/.fiwalk

	for i in 123_{01..06}
		do
		fiwalk -f -X /media/bcadmin/New\ Volume/digitalArchives/1297_Originals/$i/fiwalk.xml /media/bcadmin/New\ Volume/digitalArchives/
		1297_Originals/$i/$i.iso
		done
		
5. Save the file and close it. *If you do not save the file, the script will not run correctly*
6. Open a terminal window but right-clicking anywhere on the Desktop and selecting **Open Terminal**.
7. In the terminal, navigate to the Desktop using

    ```cd Desktop```

8. Type **bash fiwalk.bash** and hit **enter**
	
### Legacy instructions: Run Fiwalk with the ClamAV plugin (do not use anything after this heading)

#### Fiwalk script:

Previous version of the fiwalk.bash file:

::

  	cd /home/bcadmin/.fiwalk

	for i in [MSSnumber]_{ID..ID} 
		do
		fiwalk -c clamconfig.txt -X /media/bcadmin/New\ Volume1/digitalArchives/diskImages/
		[collectionName]_diskImages/$i/fiwalk.xml /media/bcadmin/New\ Volume1/digitalArchives/
		diskImages/[collectionName]_diskImages/$i/$i.img *enter*
		done
	
*For example*

::

	cd /home/bcadmin/.fiwalk

	for i in 123_{01..06}
		do
		fiwalk -c clamconfig.txt -X /media/bcadmin/New\ Volume/digitalArchives/diskImages/
		Mackey_diskImages/$i/fiwalk.xml /media/bcadmin/New\ Volume/digitalArchives/
		diskImages/Mackey_diskImages/$i/$i.E01
		done

#### fiwalk.xml review:
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
