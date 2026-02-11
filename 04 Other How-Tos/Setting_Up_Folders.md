# Setting Up Folders

Before starting work on any collection:
1. Find a working drive with sufficient space.
2. Create a top-level folder called [MSS/EUA]###_ShortName.
3. Create three subfolders:
   * [MSS/EUA]###_Originals will hold the disk images or bagged/tarred logical transfers that will be ingested as preservation copies. This is the only subfolder that will be used for Tier 1.
   * [MSS/EUA]###_ExtractedFiles will hold extracted or unpackaged files left untouched during processing in case of problems and stored afterward on the working drive.
   * [MSS/EUA]###_WorkingFiles will hold a second copy of those files available for weeding, arrangement, normalization, etc.; after processing, this subfolder will be renamed as [MSS/EUA]###_ProcessedFiles and ingested to two locations, one for preservation and one for access.
 4. Within the Originals folder, create a subfolder for each disk image/batch.
    * In BitCurator: While in the Originals folder, right click and choose "Open in Terminal." (If you need a command to batch create folders in Windows, ask a digital archivist.)
    * In the command line window that opens, type the following, replacing the second number in curly brackets with an estimated final number based on the number of media: 

      ```mkdir ###_{[ID]..[ID]}```
    
      *For example*
      
      ```mkdir 1297_{01..45}```   
