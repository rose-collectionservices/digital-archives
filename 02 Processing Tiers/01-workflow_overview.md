# Rose Library Digital Archives Processing Tiers

This document outlines a tiered approach to processing born-digital material for the Digital Archives program at the Stuart A. Rose Manuscripts, Archives, and Rare Books Library at Emory University in Atlanta, GA.

---
## Born-digital processing overview

All incoming born-digital materials undergo the same stages of work following arrival at Emory:

1.	The digital media is received or files are transferred.
2.	Born-digital materials are accessioned.
3.	Born-digital materials are inventoried.
4.	Born-digital materials are stabilized and prepared for ingest. This process will vary depending on the original format of the materials:
	a.	*Digital media* will be imaged.
	b.	*Transferred files* will be quarantined for thirty days and scanned for viruses. If not completed during transfer, checksums will be created for all files.
5.	Content is analyzed and reports created. Often this involves using Fiwalk to producing a DFXML report with metadata and provenance information, but it might instead mean creating a directory list, a checksum manifest, or other outputs from similar tools.
6.	At this point, the archivist will determine and document the appropriate tier of processing for the collection.

Archivists may use the [digital media log template](https://emory.sharepoint.com/:x:/r/sites/EUVRoseLibrary/_layouts/15/Doc.aspx?sourcedoc=%7BDF9842DA-4BCB-4997-B1DA-1899AB188D4E%7D&file=DigitalArchives_MediaLog.xlsx&action=default&mobileredirect=true) to inventory materials and record actions taken during processing.

---
## Levels of processing
Born-digital materials are processed at one of four tiers:

### [**Tier 1:** Standard](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/02-tier_1_(accessioning).md)
	* Basic descriptive metadata added to finding aid
 	* Content transferred and ingested, along with metadata, into preservation repository
  	* Processing documentation added to collection file

Tier 1 is imaging or transfer of content and ingest into a preservation repository during the accessioning process. The goal is basic control and stability. All digital content selected for preservation after preliminary appraisal by a curator, processing archivist, or digital archivist will be minimally processed at Tier 1. Tier 1 is the digital equivalent of the baseline collection-level processing done for paper materials at the point of accessioning.

### [**Tier 2:** Enhanced](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/03-tier_2.md) 
	* All Tier 1 steps 
 	* Files extracted from preservation copy
  	* Files scanned for viruses and malware
  	* Checksums created for extracted files
  	* Optional:
  		* Duplicate files identified and deleted
  		* File formats identified
 	* Enhanced descriptive metadata added to finding aid
	* Additional reports and metadata added to preservation repository and/or collection file

Tier 2 processing is done by staff, students, and interns as deemed appropriate. Tier 2 includes the extraction of the materials from disk images, tar files, or other submission or preservation packages, along with a virus and deduplication scan, to make the contents of disk images accessible to researchers. Tier 2 processing may be done immediately following Tier 1, if the collection is a known priority or there are preservation-related reasons for timely intervention. In many cases, however, materials processed at Tier 1 will not proceed to Tier 2 until one of the following conditions applies: 1) The collection as a whole is chosen for granular processing. 2) A researcher requests access to the unprocessed (Tier 1) born-digital content.

### [**Tier 2b:** Enhanced+](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/04-tier_2b.md)
	* All Tier 1 and 2 steps
 	* Extracted files normalized if needed
  	* Extracted files arranged if needed
  	* Final files added to access system
	
Tier 2b processing is done by staff, students, and interns as deemed appropriate. Tier 2b builds upon what was started with Tier 2. Tier 2b collections are those that contain relevant collection material and do not have any restrictions put on them as determined in the Deed. These can be large or small, depending on the collection. 

### [**Tier 3:** Full](#tier-3-full)
	* All Tier 1, 2, and 2b steps
 	* Extracted files scanned for PII and other restricted information
  	* Restricted information redacted or restricted documents moved into a restricted folder in preservation repository

Tier 3 processing is done by digital archives staff **only**, as these collections are normally very large or complex, are expected to be heavily used, or have unique restrictions that require more attention. The decision to process collections at Tier 3 is generally made based on information gleaned during Tier 1 and plans for the collection as a whole. In most cases, hybrid collections prioritized for granular processing should have their born-digital components processed at Tier 3 and integrated into the overall intellectual arrangement. If a granularly processed hybrid collection has only a small amount of born-digital content, or that content is relatively homogeneous, it might be appropriate to process the digital content at Tier 2/2b instead of Tier 3.

---

While the born-digital processing tiers do not map perfectly to [traditional levels and arrangement and description](https://github.com/rose-collectionservices/collection-services-manual/tree/master/05-LEVELS%20OF%20ARRANGEMENT%20AND%20DESCRIPTION#51-levels-of-arrangement-and-description), it can be helpful to think of Tier 1 as corresponding roughly with collection-level processing. Tiers 2, 2b, and 3 can be considered variations on file-level processing. 

There is no hard and fast formula for determining the appropriate tier of processing. Archivists should refer to the following criteria and use their best judgement, recognizing that this decision can be revisited later should additional processing become warranted. Once a decision has been made, it should be documented in the digital archives processing plan.

Generally, though, the following guidelines apply: All materials should receive Tier 1 processing at or near the time of accessioning to establish basic intellectual and physical control and ensure researchers know the content exists. At Tier 1, born-digital materials are still considered unprocessed. Processing to Tier 2, 2b, or 3 typically occurs when a researcher requests access, when a collection is selected for priority processing, or when processing additions to a collection that already has digital content processed to Tier 2b or 3. Tier 2b is the most common level for content available to researchers. Tier 2 is the stopping point when processing step yield no usable content or when content can be used as is after extraction. When recovered content requires additional work to facilitate access, the archivist either completes the additional steps from Tier 2b (which involves possible rearrangement and normalizations) and, in some cases, Tier 3 (which includes more extensive review and restriction). 

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
