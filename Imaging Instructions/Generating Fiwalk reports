# Generating Fiwalk reports, with virus checking

### Before you begin:

* This workflow uses tools stored as part of the BitCurator suite. If necessary, restart the Digital Archives Lab workstation and boot to the BitCurator hard drive. You can find instructions on how to do this [here](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) (Right click to open in a new tab).
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
