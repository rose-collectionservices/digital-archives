# Tier 1 - Accessioning and Imaging

## General workflow
These steps apply when accessioning a new born-digital collection or digital media from a previously accessioned hybrid collection. If the collection as a whole has not yet been accessioned, be sure to also complete the general accessioning steps described in the [Rose Library Collection Services manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/03-ACCESSIONING).

1. Document processing steps and collection needs
   * Review deed terms and check for born digital addendum.
   * Create <a href="https://emory.sharepoint.com/:x:/r/sites/EUVRoseLibrary/Shared%20Documents/Digital%20Collections/Transfer%20and%20processing/DigitalArchives_MediaLog_Tier1Processing.xlsx?d=wdf9842da4bcb4997b1da1899ab188d4e&csf=1&web=1&e=AQ67Fv">media log</a> with one row for each carrier or file transfer/batch. If the accession or collection contains very few carriers/batches, a .txt readme or additional notes in the accession record may be sufficient. High-level or summary information about Tier 1 work that can't be captured in the accession log can be recorded in the ArchivesSpace accession record. 
   * After accessioning is complete, be sure to add the completed log, along with any addenda and other relevant records, to the collection file.
2. Extended physical processing (some preliminary steps might have been completed during initial accessioning if the collection is hybrid)
   * Remove any out-of-scope computer equipment or nonfunctional media.
   * Label physical media. Write the disk number (the collection identifier followed by a sequential number: 1315_05 or EUA283_100, for example) on a small white sticker and apply it in a discreet location that will not harm the media. This number will be entered in the media log to identify the disk or transfer, in ArchivesSpace as the Component Unique Identifier for the AO describing the content, and in the object metadata in LIBSAFE Go.
3. Transfer and ingest content
   * Image media or complete logical transfer of files. See the [Imaging](https://github.com/rose-collectionservices/digital-archives/tree/master/Imaging%20Instructions) folder for more information on how to image different types of media upon accessioning.
   * Determine which preservation repository will house the content. As of 2025, most newly accessioned content will go into LIBSAFE Go. Content from collections that already have born-digital material in The Keep should go into The Keep so the collections are split; however, it is likely all Keep disk images will migrate to LIBSAFE Go in 2026, so new ingest to The Keep will stop at that point.
   * Generate manifest and scan for viruses.
     * To complete this step for content destined for The Keep, see [Fiwalk instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Generating_Fiwalk_reports.md).
     * For content submitted directly to LIBSAFE Go, use the platform's built-in virus scan and md5 checksum functions.
     * For content an archivist is uploading to LIBSAFE Go, use any appropriate combination of tools prior to ingest (recommendation as of 2025: Crowdstrike virus scan, FTK Imager directory list and hash list) then repeat with LIBSAFE Go's built-in functions after uploading. If possible, either format the pre-ingest md5 manifest in a compatible manner so it can be verified by LIBSAFE Go or plan to package the content with Bagger so it can be verified as a bag. 
   * Assemble disk images/logically transferred content and supplemental files, including imaging or transfer logs, checksum manifests, DFXML files, and readmes.
     * If uploading to The Keep, bag using Bagger. See [BagIt packaging instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Packaging_with_BagIt.md).
     * For LIBSAFE Go, bagging is recommended for preservation copies of content processed by an archivist outside the platform (vs. files transferred directly through submission areas).
   * Ingest packaged content and supplemental files to a preservation repository (The Keep or LIBSAFE Go).
     * See the [Keep upload instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Tier%201/Keep_Ingest.md) for instructions on how to upload bagged materials to the Keep.
     * See the Emory Libraries [LIBSAFE Go wiki](https://emorylib.atlassian.net/wiki/spaces/LG/pages/405995521/Using+LIBSAFE+Go+Non-Admin+Users) on Confluence or Libnova's [product documentation](https://docs.libnova.com/libsafe-go) for instructions on how to ingest to LISBAFE Go. If content is ingested to LIBSAFE Go as a bag, verify using the built-in function. Content ingested to LIBSAFE Go should go through the complete accessioning workflow in the platform and will typically go through the processing workflow as well, although the latter might be abbreviated for Tier 1 (e.g., no weeding or arrangement, minimal object metadata).
   * If the collection includes web content, set up seed(s) in Archive-It, run a test crawl, QA the crawl, and configure recurring crawls if applicable.
4. Describe content
   * Enter the metadata required by the preservation repository. See links in the previous step for detailed instructions.
     * For unprocessed disk images ingested into LIBSAFE Go, only the administrative metadata fields are required. Fill these out for the disk image file itself.
   * Add basic descriptive information to the finding aid. Collection-level description should follow the requirements outlined in the [Collection Services Manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/05-DESCRIPTION) and include the following at minimum:
     * Collection-level access note ("Researchers must contact the Rose Library in advance for access to unprocessed born digital materials in this collection. Collection restrictions, copyright limitations, or technical complications may hinder the Rose Library's ability to provide access to unprocessed born digital materials").
     * Recommended at the file level: "This born-digital material is unprocessed. Researchers must contact the Rose Library in advance for access. Use of the original digital media is restricted." Remember to select the "Restricted" local access restriction type and publish the note. 
   * Add an archival object for each physical carrier or batch of transferred files. Archival objects may be placed at the top level of the hierarchy, grouped intellectually with other materials into preliminary series, or gathered in a "born-digital materials" series as appropriate. See the [quick guide to processing digital media](https://github.com/rose-collectionservices/collection-services-manual/blob/master/10-PHYSICAL%20PROCESSING/readme.md#1074-processing-digital-media) for guidance on titling AOs if placeholders were not already created during accessioning of physical media.
   * For each AO that corresponds 1:1 with a specific carrier or transfer, record the original carrier/batch identifier (the same number used to label disks, name disk image files, and record entries in the accession log—for example, 1309_51) in the AO's component unique identifier field.
   * Create a corresponding digital object record as an instance of each AO describing digital content. Every DO record should have a one-to-one relationship with an AO record, description following [Emory's metadata guidelines for digital archival objects](https://emory.sharepoint.com/:w:/r/sites/EmoryUniversityLibraries/Shared%20Documents/Staff/Committees%20%26%20Working%20Groups/Metadata%20Policy%20Committee/Archival%20Description%20Sub-Committee/Policy%20Documentation/Metadata%20Guidelines%20for%20Digital%20Archival%20Objects%20in%20ArchivesSpace%20at%20Emory.docx?d=w25158557429b4a4a867cf6fe6fd0946d&csf=1&web=1&e=5tb8UU), and a file version linking to the relevant disk image or batch of files in the preservation repository. (A DO might have multiple file versions if there are separate preservation and access copies in the same or different systems.)
   * If the AO is not a file transfer and is associated with physical media, add the container housing the media as an instance.
   * If the collection includes archived websites, create another accession record and add an AO and DO for each one in the finding aid. For more detailed instructions, see [accessioning and description guidelines for web archives](https://github.com/rose-collectionservices/collection-services-manual/tree/master/11-FORMAT%20SPECIFIC%20PROCEDURES#114-web-archives).

## Accessioning Checklist for Born-Digital Content
There are [two versions of the checklist](https://emory.sharepoint.com/:w:/r/sites/EUVRoseLibrary/Shared%20Documents/Digital%20Collections/Transfer%20and%20processing/Templates/Accessioning%20Checklist%20for%20Born-Digital%20Content.docx?d=w58343e7735794a51a6ed9fac99aa61a0&csf=1&web=1&e=CkChHx): one outlining the required steps when handling a digital-only accession and the other outlining the required steps when accessioning digital content from a hybrid accession or otherwise processed collection. The checklist is not required and does not become part of the collection file, but it can be a useful tool. Note that not all steps will apply in every situation—adapt as needed.

## Size Estimates

Standard disk sizes (to help fill out the [processing plan] size estimate):

| Media               | Size    |
|---------------------|---------|
| 5.25" floppy disk   | 1.2 MB  |
| 3.5" floppy disk    | 1.4 MB  |
| ZIP 100 disk        | 100 MB  |
| ZIP 250 disk        | 250 MB  |
| Optical disc        | 700 MB  |
