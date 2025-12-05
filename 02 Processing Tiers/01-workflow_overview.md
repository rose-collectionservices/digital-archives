# Rose Library Digital Archives Processing Tiers

This document outlines a tiered approach to processing born-digital material for the Digital Archives program at the Stuart A. Rose Manuscripts, Archives, and Rare Books Library at Emory University in Atlanta, GA.

* [An overview of processing workflows for born-digital materials](#an-overview-of-processing-workflows-for-born-digital-materials)
* [Processing tier criteria](#processing-tier-criteria)
* [Tier 1 (Standard)](#tier-1-standard)
* [Tier 2 (Enhanced)](#tier-2-enhanced)
* [Tier 2b (Enahanced+)](#tier-2b-enhanced)
* [Tier 3 (Full)](#tier-3-full)

## An overview of processing workflows for born-digital materials

All incoming born-digital materials undergo the same stages of work following arrival at Emory:

1.	The digital media is received or files are transferred.
2.	Born-digital materials are accessioned.
3.	Born-digital materials are inventoried.
4.	Born-digital materials are stabilized and prepared for ingest. This process will vary depending on the original format of the materials:
	a.	*Digital media* will be imaged.
	b.	*Transferred files* will be quarantined for thirty days and scanned for viruses. If not completed during transfer, checksums will be created for all files.
5.	Content is analyzed and reports created. Often this involves using Fiwalk to producing a DFXML report with metadata and provenance information, but it might instead mean creating a directory list, a checksum manifest, or other outputs from similar tools.
6.	At this point, the archivist will determine and document the appropriate tier of processing for the collection.

## Levels of processing
Born-digital materials are processed at one of four tiers:

* [**Tier 1:** Standard](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/02-tier_1_(accessioning).md)
	* Basic descriptive metadata added to finding aid
 	* Content transferred and ingested, along with metadata, into preservation repository
  	* Processing documentation added to collection file
* [**Tier 2:** Enhanced](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/03-tier_2.md) 
	* All Tier 1 steps 
 	* Files extracted from preservation copy
  	* Files scanned for viruses and malware
  	* Checksums created for extracted files
  	* Optional:
  		* Duplicate files identified and deleted
  		* File formats identified
 	* Enhanced descriptive metadata added to finding aid
	* Additional reports and metadata added to preservation repository and/or collection file
* [**Tier 2b:** Enhanced+](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/04-tier_2b.md)
	* All Tier 1 and 2 steps
 	* Extracted files normalized if needed
  	* Files added to access system
* [**Tier 3:** Full](#tier-3-full)
	* All Tier 1 and 2 steps
 	* Extracted files scanned for PII and other restricted information
  	* Restricted information redacted or restricted documents moved into a restricted folder in preservation repository
  	* Files normalized if needed
  	* Files arranged if needed
  	* Files added to access system

There is no hard and fast formula for determining the appropriate tier of processing. Archivists should refer to the following criteria and use their best judgement, recognizing that this decision can be revisited later should additional processing become warranted. Once a decision has been made, it should be documented in the digital archives processing plan.

Generally, though, the following guidelines apply: All materials should receive Tier 1 processing at or near the time of accessioning to establish basic intellectual and physical control and ensure researchers know the content exists. At Tier 1, born-digital materials are still considered unprocessed. Processing to Tier 2, 2b, or 3 typically occurs when a researcher requests access, when a collection is selected for priority processing, or when processing additions to a collection that already has digital content processed to Tier 2b or 3. Tier 2b is the most common level for content available to researchers. Tier 2 is the stopping point when processing step yield no usable content' when usable content is recovered, the archivist either completes the few additional steps from Tier 2b to facilitate access or proceeds to Tier 3, which includes more extensive review, restriction, and possibly rearrangement prior to access. 

While the born-digital processing tiers do not map perfectly to the (traditional levels and arrangement and description)[https://github.com/rose-collectionservices/collection-services-manual/tree/master/05-LEVELS%20OF%20ARRANGEMENT%20AND%20DESCRIPTION#51-levels-of-arrangement-and-description], it might be helpful to think of Tier 1 are corresponding roughly with collection-level processing. Tiers 2, 2b, and 3 can be considered variations on file-level processing. 

## Processing tier criteria

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
