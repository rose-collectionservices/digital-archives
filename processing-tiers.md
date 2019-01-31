# Digital Archives Processing Tiers

* [An overview of processing workflows for born-digital materials](#an-overview-of-processing-workflows-for-born-digital-materials)
* [Processing tier criteria](#processing-tier-criteria)
* [Tier 1 (Standard)](#tier-1-standard)
* [Tier 2 (Enhanced)](#tier-2-enhanced)
* [Tier 2b (Enahanced+)](#tier-2b-enhanced)
* [Tier 3 (Full)](#tier-3-full)
* [Time analysis](#time-analysis)
	* [Tier 1 (Standard)](#tier-1-standard)

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
* [**Tier 2b:** Enhanced+](#tier-2b-enhanced+)
* [**Tier 3:** Full](#tier-3-full)

There is no hard and fast formula for determining the appropriate tier of processing. Archivists should refer to the following criteria and use their best judgement, recognizing that this decision can be revisited later should additional processing become warranted. Once a decision has been made, it should be documented in the digital archives processing plan.

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

1.	Basic descriptive metadata is added to the finding aid.
2.	Disk image or tar file, plus metadata, is bagged and ingested into the Keep.
3.	A copy of a completed processing plan is added to the collection file.

## Tier 2 (Enhanced)

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

In cases where a collection's content is low-risk and stored using a very limited number of standard file formats, files undergo all steps listed under **Tier 2**, plus:

1. Files are normalized.
2. Access copies of files are moved to the secure server.

## Tier 3 (Full)

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

### Tier 2b (Enhanced+)

### Tier 3 (Full)

Data collection underway