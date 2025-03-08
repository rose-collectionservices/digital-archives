# Tier 1 - Accessioning and Imaging

Tier 1 is imaging or transfer of content and ingest into a preservation repository during the accessioning process. The goal is basic control and stability. All digital content selected for preservation after preliminary appraisal by a curator, processing archivist, or digital archivist will be minimally processed at Tier 1.

These steps apply when accessioning a new born-digital collection or digital media from a previously accessioned hybrid collection. If the collection as a whole has not yet been accessioned, be sure to also complete the general accessioning steps described in the [Rose Library Collection Services manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/03-ACCESSIONING).

Tier 1 process:
1. Create a digital processing plan and/or media log spreadsheet. A log is often more efficient for accessioning content from large numbers of carriers.
2. Label physical media with disk numbers.
3. Image media or complete logical transfer of files. See the [Imaging](https://github.com/rose-collectionservices/digital-archives/tree/master/Imaging%20Instructions) folder for more information on how to image different types of media upon accessioning.
4. Generate manifest and scan for viruses. To complete this step for content destined for The Keep, see [Fiwalk instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Generating_Fiwalk_reports.md). For content destined for LIBSAFE Go, use the platform's built-in virus scan and md5 checksum functions. 
5. Assemble disk images/logically transferred content and supplemental files. If uploading to The Keep, bag using BagIt. See [BagIt packaging instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Packaging_with_BagIt.md).
6. Ingest packaged content and supplemental files to a preservation repository (The Keep or LIBSAFE Go). See the [Keep upload instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md) for instructions on how to upload bagged materials to the Keep. See the Emory Libraries [LIBSAFE Go wiki](https://emorylib.atlassian.net/wiki/spaces/LG/pages/405995521/Using+LIBSAFE+Go+Non-Admin+Users) on Confluence or Libnova's [product documentation](https://docs.libnova.com/libsafe-go) for instructions on how to ingest to LISBAFE Go. Content ingested to LIBSAFE Go should go through the complete accessioning workflow in the platform and will typically go through the processing workflow as well, although the latter might be abbreviated for Tier 1 (e.g., no weeding or arrangement, minimal object metadata).
7. Enter the metadata required by the preservation repository. See links in the previous step for detailed instructions.
8. Add basic descriptive information to the finding aid. Collection-level description should follow the requirements outlined in the [Collection Services Manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/05-DESCRIPTION), including at minimum a collection-level processing note about the transfer of data and a collection-level access note ("Researchers must contact the Rose Library in advance for access to unprocessed born digital materials in this collection. Collection restrictions, copyright limitations, or technical complications may hinder the Rose Library's ability to provide access to unprocessed born digital materials.").
9. Add an archival object for each physical carrier or batch of transferred files. Archival objects may be placed at the top level of the hierarchy, grouped intellectually with other materials into preliminary series, or gathered in a "born-digital materials" series as appropriate. See the [quick guide to processing digital media](https://github.com/rose-collectionservices/collection-services-manual/blob/master/10-PHYSICAL%20PROCESSING/readme.md#1074-processing-digital-media) for guidance on titling AOs if placeholders were not already created during accessioning of physical media.
10. Create a corresponding digital object record as an instance of each AO describing digital content. Every DO record should have a one-to-one relationship with an AO record, description following [Emory's metadata guidelines for digital archival objects](https://emory.sharepoint.com/:w:/r/sites/EmoryUniversityLibraries/Shared%20Documents/Staff/Committees%20%26%20Working%20Groups/Metadata%20Policy%20Committee/Archival%20Description%20Sub-Committee/Policy%20Documentation/Metadata%20Guidelines%20for%20Digital%20Archival%20Objects%20in%20ArchivesSpace%20at%20Emory.docx?d=w25158557429b4a4a867cf6fe6fd0946d&csf=1&web=1&e=5tb8UU), and a file version linking to the relevant disk image or batch of files in the preservation repository.
11. If the AO is not a file transfer and is associated with physical media, add the container housing the media as an instance.
12. If the collection includes web content, set up seed(s) in Archive-It, create another accession record, and add an AO and DO for each one in the finding aid. For more detailed instructions, see [accessioning and description guidelines for web archives](https://github.com/rose-collectionservices/collection-services-manual/tree/master/11-FORMAT%20SPECIFIC%20PROCEDURES#114-web-archives).
13. Add the completed digital processing plan and/or media log to the collection file.

---

Checklist for accessioning born-digital content, including both digital-specific steps and general accessioning steps (not all steps will apply in every situation):
1. Create processing plan document and/or media log
2. Label disks with numbers
3. Image or transfer content
5. Create manifests/checksums
6. Scan for viruses
7. Collect/bag content and supplemental files
8. Ingest to preservation repository
9. Record metadata in preservation repository
10. Create CL-2 file (physical and electronic)
    *  Write accession number on acquisitions paperwork
    *  File acquisitions paperwork in CL-2
11. Update accession record
    * Link to acquisitions paperwork in SharePoint
12. Archive web content
    *  Add seeds to Archive-It and start test crawl
    *  QA and save
    *  Create additional accession record
13. Create or update finding aid with digital-specific information in the following fields:
    * Extent
    * Abstract
    * Scope and content note
    * Processing note
    * Conditions governing access note
14. Add AO for each piece of media or batch of files
15. Add DO for each AO describing digital content
16. Create or update catalog record 
17. Gather physical media into BD box(es)
    * Label and barcode boxes
    * Create top container(s) for boxes and link to AOs in ASpace
    * Add box(es) to Alma holdings
    * Move box(es) to permanent location
18. Update shelf list (main entry and digital archives tab)
19. Update records in Acquisitions & Accessioning table
20. Update processing stats spreadsheet
21. Announce to #collections Slack channel (if new or significant)

---
Standard disk sizes (to help fill out the [processing plan] size estimate):

| Media               | Size    |
|---------------------|---------|
| 5.25" floppy disk   | 1.2 MB  |
| 3.5" floppy disk    | 1.4 MB  |
| ZIP 100 disk        | 100 MB  |
| ZIP 250 disk        | 250 MB  |
| Optical disc        | 700 MB  |
