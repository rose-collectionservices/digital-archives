# Tier 2b - Full Processing without Restrictions
To process at the Tier 2b level, typically when extracted content requires normalization or arrangement beyond original groupings, begin after deduplication in Tier 2 and follow the additional steps below. When finished, return to the [Tier 2 instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/03-tier_2.md) for the final workflow steps, which are identical for Tiers 2, 2b, and 3.

Record Tier 2b actions and observations in a .txt readme file, digital processing plan, or media log spreadsheet (recommended for large, complex collections). 

---

## Content Review and Weeding (if needed)

If needed, use one or more of the methods described below. For small or homogeneous collections, a visual review without software tooling might be sufficient.

### Deduplication with FSLint
*This step should take place in the BitCurator/Ubuntu environment.*

1. On the desktop, click the Forensics and Reporting folder.
2. Double click FSLint to launch it.
3. Once open, click the “+Add” button at the top left and navigate to the hard drive and WorkingFiles folder. 
4. Double click the first folder in WorkingFiles.
5. Remove the “/” from the top box using the “X Remove” button under the “+Add” button.
6. Make sure the tab on the left is set to “Duplicates.”
7. Click the “Find” button on the bottom left of the screen to start finding duplicates within the one folder.
8. In the results screen, right click and choose "within groups," then “select all but newest” then click “Delete” in the bottom right corner.
9. Click “Find” again to make sure everything else got deleted.
10. On the left, choose the “Empty Directories” tab and click “Find.”
11. Delete all the empty directories which appear.
12. Do the same for the “Temp Files” tab.
13. Repeat this process for other folders in the collection, removing and adding each one every time.
14. Once done with the individual folders, add the WorkingFiles folder as a whole and run the “Duplicates,” “Empty Directories,” and “Temp Files” options against everything at once. This is to triple-check there are no more lingering duplicate files or empty directories in the collection. 

### Size and format analysis with TreeSize Pro
*This step should take place in Windows.*

1. Open TreeSize Pro and scan the WorkingFiles folder.
2. In the results, look for files or folders that are particularly large, possibly duplicative, in problematic formats, etc. At this stage, do not assess or make decisions about individual files, but look for patterns and problem areas.
3. If you find folders that are clearly out of scope, delete them from WorkingFiles.
4. If you notice anything that requires more careful review or intervention, flag it and consider taking the collection to Tier 3.
5. Record any relevant information that will help with writing more accurate description later.

---

## Normalization (if needed)
*This step may take place in either BitCurator/Ubuntu or Windows, depending on the material being normalized and the method chosen. See [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*

The instructions below work best for text and image files. They may be applied to all files in a collection or a subset. 

This step is no longer required in all cases, as most text and image files can be used in their original formats. It is still recommended when files are in uncommon formats and will not be usable by researchers using standard reading room access tools. If the files of concern are not text or image files that can be converted to PDF or JPG using the scripts, a digital archivist will identify alternative tools or suitable manual processes.

### In BitCurator/Ubuntu
1. Locate the *convertFINAL.bash* file on the desktop. Double-click to open the file in the text editor. 
2. In the text editor, select all of the text and right-click to copy (or do ```Ctrl+C```)
3. In the collection folder, navigate to the WorkingFiles folder. Right-click and select "Open in Terminal"</br>
a. You can also choose each individual folder inside WorkingFiles, if that's what you prefer. </br>
4. In the terminal, double-check the file path to make sure the right folder is open in the terminal. 
5. In the terminal, right-click and select *Paste* to paste the previously copied text into the terminal window.
6. Hit *Enter* on the keyboard. 
7. Keep an eye on the terminal window as the script runs, to make sure it doesn't get stuck on anything. If it does, consult the Digital Archivist. 

### In Windows
*[Switch back to Windows](#switching-to-bitcuratorubuntu-from-windows) to normalize the files using Adobe PDF/Paint/GIMP/Excel/Word*</br>
1. For Word and Excel files, select multiple (around 10) files at once, right click and select “Convert to Adobe PDF”</br>
a. To select multiple files at once, select the first one, then hold down the "Shift" key and click the last one you want to select in the group. All the files selected should appear blue. </br>
2. Navigate to the correct folder the PDF should save in, and hit “Save” in the first dialogue box; do the same for the second dialogue box. 
3. For TIFF/BMP/PNG files, right click and choose “Open With...” and choose Paint. Do these one at a time. In Paint, choose “Save As…” and choose JPG. Navigate to the proper folder and hit “Save”
4. For Photoshop/Illustrator files, right click and choose “Open With...” and choose GIMP. Click “Ok” when GIMP asks how to read the file (so, going with normal initial settings). Go to “File” at the top and choose “Export As” and choose JPG as the file type in the pop-up box in the bottom scroll list. Slide the resolution up to 10 and hit “Export” and navigate to proper folder for it to export to. 
5. If you run into an odd or unfamiliar file type, contact the digital archivist for assistance.

---

## Arrangement (if needed)
*This step should take place in the Windows environment.*

### If you are maintaining the original groupings of the content by carrier or batch 
This is the most common approach except in situations where the original groupings are not meaningful and may in fact impede access. Even entire hard drives can often be handled this way, provided robust scope notes and detailed directory lists are made available to help researchers locate content.

1. Within each disk-level subfolder of WorkingFiles, move any folders and files past the root folder up to the disk-level directory to reduce the number of unnecessary nested folders.
2. Rename WorkingFiles to MSS/EUA###_ProcessedFiles.

### If you are instead arranging files (a) by material type (floppy disks and optical discs, hard drive model, etc.) or (b) to match series arrangement 
This used to be our standard practice but is now uncommon because it takes more time and obscures provenance.

1. Create a complete copy of WorkingFiles, ideally using TeraCopy, and name it MSS/EUA###_ProcessedFiles.
2. Create folders within the ProcessedFiles folder based on the planned arrangement.
3. Copy the content of each disk-level folder under WorkingFiles into the appropriate new location. 
4. If there are any files noted by Windows as duplicates as you copy and paste, select **See details for all files** in the pop-up window. Select **BOTH** checkboxes at the top of the list to select both copies of the materials. Windows will automatically append a "(1)" to the end of the original file title.
5. Once you are satisfied with the folder structure and everything has been sorted, delete WorkingFiles, retaining only the finished ProcessedFiles (in addition to Originals and ExtractedFiles).

At the end of this stage, all processed files intended to be made available to researchers should be in subfolders within the ProcessedFiles directory. This directory is the final version of the content and will live as two copies in our systems: one packaged for preservation and ingested alongside the Tier 1/original versions, and one uploaded to an access system for researcher use.

---

## Tier 2b Examples

* Thomas Kinsella papers
* Constance W. Curry papers
* Henry H. and Ella Pearson Mitchell papers
* AID Atlanta records
* Teri Darnell photographs
