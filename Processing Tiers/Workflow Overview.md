# Rose Library Digital Archives Processing Tiers

This document outlines a tiered approach to processing born-digital material for the Digital Archives program at the Stuart A. Rose Manuscripts, Archives, and Rare Books Library at Emory University in Atlanta, GA.

* [An overview of processing workflows for born-digital materials](#an-overview-of-processing-workflows-for-born-digital-materials)
* [Processing tier criteria](#processing-tier-criteria)
* [Tier 1 (Standard)](#tier-1-standard)
* [Tier 2 (Enhanced)](#tier-2-enhanced)
* [Tier 2b (Enahanced+)](#tier-2b-enhanced)
* [Tier 3 (Full)](#tier-3-full)
* [Tracking time using Toggl](#tracking-time-using-toggl)
	* [How to Use Toggl](#how-to-use-toggl)
* [Time analysis](#time-analysis)
	* [Tier 1 (Standard)](#tier-1-standard-1)
	* [Tier 2 (Enhanced)](#tier-2-enhanced-1)
	* [Tier 2b (Enhanced+)](#tier-2b-enhanced-1)
	* [Tier 3 (Full)](#tier-3-full-1)

## An overview of processing workflows for born-digital materials

All incoming born-digital materials undergo the same stages of work following arrival at Emory:

1.	The digital media is received or files are transferred.
2.	Born-digital materials are accessioned.
3.	Born-digital materials are inventoried.
4.	Born-digital materials are stabilized and prepared for ingest. This process will vary depending on the original format of the materials:
	a.	*Digital media* will be imaged.
	b.	*Transferred files* will be quarantined for thirty days and scanned for viruses. If not completed during transfer, checksums will be created for all files.
5.	Using Fiwalk, a DFXML report is created.
6.	At this point, the archivist will determine and document the appropriate tier of processing for the collection.

Born-digital materials are then processed at one of four tiers of processing:

* [**Tier 1:** Standard](#tier-1-standard)
* [**Tier 2:** Enhanced](#tier-2-enhanced)
* [**Tier 2b:** Enhanced+](#tier-2b-enhanced)
* [**Tier 3:** Full](#tier-3-full)

There is no hard and fast formula for determining the appropriate tier of processing. Archivists should refer to the following criteria and use their best judgement, recognizing that this decision can be revisited later should additional processing become warranted. Once a decision has been made, it should be documented in the digital archives processing plan.

[Back to top](#digital-archives-processing-tiers)

---

## Processing Tier Criteria

| ﻿Criteria                            | Considerations                                                                                                                                                                                                                                           |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Collection use                      | Do we have reason to anticipate high levels of use for this collection? Are there existing parts of this collection that see high levels of use?                                                                                                         |
| Teaching potential                  | Is there faculty interest in this collection or other collections that are similar to this one? Would this collection be particularly well-suited to classes focused on teaching with born-digital materials using digital humanities tools and methods? |
| Research potential                  | Is this collection considered to have particular research value? Is this collection especially relevant to our collecting areas or the interests emphasized in our research fellowship positions?                                                        |
| Requests/mandates                   | Have we been asked (or required) to fully process the collection either by donors or researchers?                                                                                                                                                        |
| Related exhibits or outreach        | Does this collection support upcoming exhibits or programming?                                                                                                                                                                                           |
| Relationship to paper component     | How much overlap exists between the born-digital materials and any paper component of the collection?                                                                                                                                                    |
| Digital Archives research potential | Is the collection stored on media or in formats that would allow digital archives to test new methods or tools, or refine workflows and processes?                                                                                                       |
| Technical feasibility               | What types of media and files have we received, and how well-equipped are we to process and render them? How much staff time would need to be devoted to this project?                                                                                   |

Depending on the selected tier, processing will continue as follows:

## Tier 1 (Standard)
**[Link to full instructions](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%201)**

1.	Basic descriptive metadata is added to the finding aid.
2.	Disk image or tar file, plus metadata, is bagged and ingested into the Keep.
3.	A copy of a completed processing plan is added to the collection file.

## Tier 2 (Enhanced)
**[Link to full instructions](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202)**

1.	Files are extracted from the disk image or tar file.
2.	Files are scanned for viruses and malware, and the results of the scan documented.
3.	Duplicate files are identified and deleted.
4.	Checksums are created for extracted files.
5.	File formats are identified.
6.	Extracted files are wrapped into a tar file.
7.	Enhanced descriptive metadata is added to the finding aid.
8.	Disk image, tar file, metadata, and virus scan report are bagged and ingested into the Keep.
9.	A copy of a completed processing plan is added to the collection file.

## Tier 2b (Enhanced+)
**[Link to full instructions](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%202b)**

In cases where a collection's content is low-risk and stored using a very limited number of standard file formats, files undergo all steps listed under **Tier 2**, plus:

1. Files are normalized.
2. Access copies of files are moved to the secure server.

## Tier 3 (Full)
**[Link to full instructions](https://github.com/rose-collectionservices/digital-archives/tree/master/Tier%203)**

1. Files are extracted from the disk image or tar file(s).
2. Files are scanned for viruses and malware, and the results of the scan documented.
3. Duplicate files are identified and deleted.
4. Using bulk_extractor (and other methods where necessary), files are scanned for PII and other restricted information.
5. Restricted information is redacted or restricted documents are moved into a restricted folder.
6. Checksums are created for extracted files.
7. File formats are identified.
8. Files are normalized.
9. Files are 'arranged.'
10. Full descriptive metadata is added to the finding aid.
11. Access copies of files are moved to the secure server.
12. Folder containing extracted files, restricted files, and access copies of files are wrapped into a tar file.
13. Disk image, tar files, metadata, and virus scan report are bagged and ingested into the repository.
14. A copy of a completed processing plan is added to the collection file.

[Back to top](#digital-archives-processing-tiers)

---

## Tracking Time using [Toggl](https://toggl.com)

All time spent processing born-digital collections should be tracked using the Rose Library Digital Archives [Toggl](https://toggl.com) account. Contact the account administrator to be added.

All time tracked in Toggl should be associated with a project. The Rose Library Digital Archives Toggl account has five projects. Use the descriptions below to determine which project should be used to track your time:

1 | **ACCESSIONING/TIER 1 PROCESSING**

	* Used to track any activity that falls under the scope of accessioning born-
	digital materials.
	* This includes:
		* Any review of media (for example, using ISOBuster to review optical
			discs);
		* Disk Imaging;
		* The creation of TAR files;
		* Any reporting activity associated with accessioning and tier 1
		  processing (for example, FiWalk, ClamAV, etc.);
		* Packaging the SIP (using BagIt);
		* Ingest into the Keep and completion of Keep metadata;
		* Any necessary updates to the collection finding aids.

2 | **TIER 2A PROCESSING**

	* If a collection is selected for tier 2 processing, all post-accessioning
	activity should be tracked within Toggl's Tier 2a processing project.
	* This includes:
		* The extraction of files from the disk image or TAR file;
		* Virus scanning;
		* De-duplication of files;
		* The creation of file-level checksums;
		* The identification of file formats;
		* The packaging of files and associated metadata using TAR and BagIt;
		* Ingest into the Keep and completion of Keep metadata;
		* Any necessary updates to the collection finding aids.

3 | **TIER 2B PROCESSING**

	* If a collection is selected for tier 2b processing, all post-accessioning
	activity should be tracked within Toggl's Tier 2b processing project.
	* This includes:
		* The extraction of files from the disk image or TAR file;
		* Virus scanning;
		* De-duplication of files;
		* The creation of file-level checksums;
		* The identification of file formats;
		* File format normalization and the creation of access copies;
		* The packaging of files and associated metadata using TAR and BagIt;
		* Ingest into the Keep and completion of Keep metadata;
		* Any necessary updates to the collection finding aids.

4 | **TIER 3 PROCESSING**

	* If a collection is selected for tier 3 processing, all post-accessioning
	activity should be tracked within Toggl's Tier 3 processing project.
	* This includes:
		* The extraction of files from the disk image or TAR file;
		* Virus scanning;
		* De-duplication of files;
		* The creation of file-level checksums;
		* The identification of file formats;
		* Scans for PII and other restricted information;
		* Any necessary redaction work;
		* File format normalization;
		* Any necessary arrangement and the creation of access copies;
		* The packaging of files and associated metadata using TAR and BagIt;
		* Ingest into the Keep and completion of Keep metadata;
		* Any necessary updates to the collection finding aids.

4 | **TROUBLESHOOTING**

	* Any significant problem-solving or research conducted in response to
	  issues identified during the accessioning or processing of a collection
	  should be tracked within Toggl's Troubleshooting project.
	* This would not include known issues or problem areas (for example,
	  repeated attempts to image a damaged floppy disk).
	* This would also not include collection-specific tasks (for example,
    establishing how to migrate a particular file format to PDF. This would be
    considered part of normalization and tracked either under Tier 2b
    processing or Tier 3 processing.)
	* This would include new or unresolved issues (for example, establishing
    workflows for imaging new media formats, time spect researching how a tool
    works, etc.).

In addition to tracking your time within the relevant project, you should use tags to identify the category of work underway. Pre-populated tags include:

| Tags                          | Use for:                                                                                                                                                                                                                             |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arrangement                   | Any tasks associated with arranging files for access.                                                                                                                                                                                 |
| Deduplication                 | Any tasks associated with the deduplication of files.                                                                                                                                                                                 |
| Description                   | Includes any updates to the finding aids and/or the creation of any supplementary files used to support access (file inventories, for example).                                                                                       |
| File extraction and reporting | Includes the extraction of files from disk images or TAR files, the creation of file-level checksums, the identification of file formats, virus scanning, and use of any additional reporting tools (for example, Brunhilde, FiWalk). |
| Imaging                       | Includes any pre-imaging review of media (for example, using ISObuster to review optical discs), and the initial creation of disk images and TAR files.                                                                               |
| Ingest                        | Includes any taska associated with packaging and ingesting files into the Keep, and the creation of Keep metadata.                                                                                                                    |
| Normalization or migration    | Includes any tasks associated with the normalization or migration of files, including any work required to establish methods and tools.                                                                                               |
| Restrictions and PII          | Includes any tasks associated with identifying PII and other restricted content, and redacting or removing restricted content from the collection.                                                                                    |

### How to Use Toggl

1. Log into your [Toggl](https/toggl.com) account.
2. From the **Timer**, enter the collection name in the space marked **What are you working on?**
3. Click the **Project** icon (which looks like a small folder) and select the relevant project.
4. Click the **Tags** icon (to the right of the **Project** icon) and select the relevant tags.
5. Hit the green **Play** button to start the timer.
6. When work is complete, hit the red **Stop** button to stop the timer.
7. Don't forget to stop and restart the timer as you complete one category of work and move into another. This will let you change the tags associated with your work.

[Back to top](#digital-archives-processing-tiers)

---

## Time Analysis

The following time analysis is intended to guide decisions and inform planning around the processing of born-digital archival material.

Disk imaging occurs at every tier of processing. When working with large storage media, imaging can be a time-consuming process and, where possible, large media should be imaged overnight so as to avoid monopolizing digital archives workstations during the workday. On average:

* Imaging a 250GB hard drive will take 3-4 hours
* Imaging a 500GB hard drive will take 6-7 hours
* Imaging a 1TB hard drive will take 20 hours

### Tier 1 (Standard)

The following estimates are based on metrics gathered between July 2018 and January 2019. During that time, born-digital materials from 50 collections were processed at tier 1. Collections included 1,379 individual pieces of media (including floppy disks, optical discs, hard drives, zip disks, and flash drives), totaling 426.5 GB of data.

Based on these numbers and for the purposes of high-level planning, archivists should anticipate tier 1 processing times of **54 minutes per gigabyte**.

With that being said, processing times vary depending on format. When planning resources for processing projects at tier 1, the following should be taken into consideration:

| Type of media      | Time per 10 disks |
|--------------------|-------------------|
| 3.5" floppy disks  | 1.5 hours         |
| 5.25" floppy disks | 1.5-2 hours       |
| Optical discs      | 2 hours           |
| ZIP 100 disks      | 2.5 hours         |
| ZIP 250 disks      | 1-1.5 hours       |


### Tier 2 (Enhanced)

The following estimates are based on metrics gathered between September 2019 and April 2020. During that time, born-digital materials from 6 collections were processed at tier 2. Collections included 18 individual pieces of media (including floppy disks and hard drives), totaling 102 MB. 

Based on these numbers and for the purposes of high-level planning, archivists should anticipate tier 2 processing times of **4 minutes per 25 MB**. 

With that being said, processing times vary depending on format and task. When planning resources for processing projects at tier 2, the following should be taken into consideration: 

| Task                               | Time per collection |
|------------------------------------|---------------------|
| File extraction and identification | 2.4 minutes         |
| Deduplication                      | 30 seconds          |
| Description                        | 3.5 minutes         |


### Tier 2b (Enhanced+)

The following estimates are based on metrics gathered between September 2019 and April 2020. During that time, born-digital materials from 59 collections were processed at tier 2b. Collections included 1,956 individual pieces of media (including floppy disks, optical discs, hard drives, zip disks, flash drives, and file transfers), totaling 794.5 GB. 

Based on these numbers and for the purposes of high-level planning, archivists should anticipate tier 2b processing times of **6 minutes per 1 GB**. 

With that being said, processing times vary depending on format and task. When planning resources for processing projects at tier 2b, the following should be taken into consideration: 

| Task                               | Time per collection |
|------------------------------------|---------------------|
| File extraction and identification | 25 minutes          |
| Deduplication                      | 3 minutes           |
| Normalization                      | 1.3 hours           |
| Arrangement                        | 12 minutes          |
| Ingest                             | 10 minutes          |
| Description                        | 12 minutes          |

### Tier 3 (Full)

The following estimates are based on metrics gathered between September 2019 and April 2020. During that time, born-digital materials from 13 collections were processed at tier 3. Collections included 488 individual pieces of media (including floppy disks, optical discs, hard drives, zip disks, flash drives, and file transfers), totaling 167.5 GB. 

Based on these numbers and for the purposes of high-level planning, archivists should anticipate tier 3 processing times of **7 minutes per 1 GB**. 

With that being said, processing times vary depending on format and task. When planning resources for processing projects at tier 3, the following should be taken into consideration: 

| Task                               | Time per collection |
|------------------------------------|---------------------|
| File extraction and identification | 4.5 hours           |
| Deduplication                      | 1.5 hours           |
| Normalization                      | 12.7 hours          |
| Arrangement                        | 1.5 hours           |
| Ingest*                            | 11 minutes          |
| Description                        | 30 minutes          |

* Ingest started to be counted into the Description timing starting in 2020, so this reflection is off, but still important to note. 


[Back to top](#digital-archives-processing-tiers)
