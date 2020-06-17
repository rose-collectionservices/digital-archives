## Creating TAR Files

These instructions explain how to create and extract a TAR file in cases where a complete disk image is not warranted. An example of this is an overly large hard drive or a CD-RW (read-write) optical disc. 

### Using the Windows machine in the lab:
*This should take place in the Windows environment. Please see [Switching from BitCurator to Windows](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions to switch.*
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
*This should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Switching_BitCurator_Windows.md) for instructions to switch.*
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

