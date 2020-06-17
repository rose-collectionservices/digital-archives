# Optical Disc Policy

This document outlines policy for handling optical discs acquired by the Rose Library as part of manuscript collections. 
This will help guide decisions as to if and how digital archivists at the Rose capture data from CDs and DVDs.

Upon receiving an optical disc, an archivist reviews its content using [IsoBuster](http://www.isobuster.com), located on the Windows side of the machine. 

A disc’s contents will fall into one of four categories:
1. A commercially-produced disc
2. A recordable disc containing only audiovisual data
3. A recordable disc with a single session and a single track containing many filesystems (a typical data CD)
4. A recordable mixed-mode CD, containing both audio and filesystem data

**If the disc in question is a COMMERCIALLY-PRODUCED DISC...**
- No data is captured. Due to copyright concerns, access is restricted.

**If the disc in question is contains ONLY AUDIOVISUAL DATA...**
- The disc enters the AV workflow, managed by Laura and Trey.

**If the disc in question is a DATA CD...**
- A raw disk image is created using Guymager.
- The resulting ISO file is bagged and ingested into the Keep using our normal workflows.

**NOTE:** Check to see if the CD is a *CD-R* or a *CD-RW*. If the CD is a **CD-RW**, you will need to create a TAR file, using [these instructions](https://github.com/bedwards254/DAprocessingTiers/blob/master/Tier%201/Imaging/TAR_Files.md). 

**If the disc in question is a recordable mixed-mode CD...**
- A disk image is created using the BIN/CUE file format, using either FTK Imager or IsoBuster.
- *WHY IS THE BIN/CUE FORMAT REQUIRED FOR MIXED-MODE DISCS?*
1. Unlike single session CDS, mixed-mode CDs store data in multiple sessions and multiple tracks. 
One session will contain audio tracks, the other will contain filesystem data. 
A BIN/CUE file is a multi-part object: the BIN file contains the raw data from the disc, while the CUE file 
contains metadata thatrecordshow the raw file should be broken into sessions and tracks. 
The CUE file is required in order to properly render data from mixed-mode discs.
2. The BIN/CUE format also capturesthe full sector width, unlike an ISO file. This is essential forany discs 
containing audiotracks, as audio dispenses with one layer of error correction and uses the full 2352 bytes for data.

- Current repository infrastructure does not support BIN/CUE files (or any other single multi-part objects). 
As a result, these files should be bagged and stored on Digital Archives Lab storage until ingest becomes possible.
