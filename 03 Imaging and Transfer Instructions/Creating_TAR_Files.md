## Creating TAR Files

These instructions explain how to create and extract a TAR file in cases where a complete disk image is not warranted or possible. Examples: media with multiple failed attempts to image, large hard drives, CD-RW (read-write) optical discs, disks with notable privacy concerns or containing significant amounts of out-of-scope content. In some of these cases, it may also be appropriate to extract logical copies using FTK Imager and then bag or tar the extracted files for preservation.

### Using the Windows machine in the lab:
*This should take place in the Windows environment. Please see [Switching from BitCurator to Windows](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions to switch. Right click to open in a new tab.*
1. Connect the collection hard drive to the DA lab machine using a write blocker.
2. Launch Cygwin Terminal.
3. Navigate to the collection hard drive using: ``$ cd [drive letter]``:
  * For example: ``$ cd J:``
4. Use the following command to create your TAR file:
`` $ tar -cvpf [path/to/tar-file-name-with-extension] [directory-of-collection-files``
  * For example: ``$ tar -cvpf '/cygdrive/c/Users/Digital Archives/Desktop/868_01.tar'donor-files``

**NOTE:** If you wish to wrap multiple directories/files into a single TAR file, they can be listed at the end of the command.
   * For example: ``$ tar -cvpf '/cygdrive/c/Users/Digital Archives/Desktop/868_01.tar'donor-files1 donor-files2 donor-files3``

5. Extract the TAR file using the following command (you will need to either navigate to the location of the TAR file or 
include the path): ``$ tar -xvpf [TAR-file-name-with-extension]``
  * For example: ``$ tar -xvpf 868_01.tar``
  
### Using Mac OS or Linux:
*This should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions to switch. Right click to open in a new tab.*
1. Connect the collection hard drive to the DA lab machine using a write blocker.
2. Navigate to the collection hard drive using: ``$ cd [drive letter]:``
  * For example: ``$ cd J:``  
3. Use the following command to create your TAR file: ``$ tar -cvpf [path/to/tar-file-name-with-extension] 
[directory-of-collection-files]``
  * For example: ``$ tar -cvpf /c/Users/Digital Archives/Desktop/868_01.tar donor-files``

**NOTE:** If you wish to wrap multiple directories/files into a single TAR file, they can be listed at the end of the command.
  * For example: ``$ tar -cvpf /c/Users/Digital Archives/Desktop/868_01.tar donor-files1 donor-files2 donor-files3``
4. Extract the TAR file using the following command (you will need to either navigate to the location of the TAR file or 
include the path): ``$ tar -xvpf [TAR-file-name-with-extension]``
  * For example: ``$ tar -xvpf 868_01.tar``

