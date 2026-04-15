# Tier 1 - Accessioning and Imaging

## Workflow overview

All incoming born-digital materials go through the same basic process, although the order and depth of the stages might vary. This work ideally occurs as soon as possible after the materials' arrival at Emory.

1.	Digital media is received or files are transferred.
2.	Collection or addition is inventoried and accessioned. (This includes format-agnostic accessioning steps that are done for both hybrid and digital-only collections and maybe be completed by a digital archivist or a processing archivist, depending on the collection. See the [Collection Services manual's instructions](https://github.com/rose-collectionservices/collection-services-manual/tree/master/10-PHYSICAL%20PROCESSING#1074-processing-digital-media) for physical processing of digital media that takes place at this stage.) 
3.	Content is stabilized and prepared for ingest. 
4.	Content is analyzed and reports created. 
5.	Archivist determines and documents whether Tier 1 treatment is sufficient or the collection should undergo a higher level of processing.

## Detailed workflow
These steps apply when accessioning a new born-digital collection or digital media within a previously accessioned hybrid collection. If the collection as a whole has not yet been accessioned, be sure to also complete the general accessioning steps described in the [Rose Library Collection Services manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/03-ACCESSIONING).

This section describes accessioning steps in detail. If you need a simpler version for quick reference, see the checklist linked below. Trained students may assist with the steps in bold type.

1. Document processing steps and collection needs
   * Review deed terms and check if there is a born digital addendum.
   * **Create a <a href="https://emory.sharepoint.com/:x:/r/sites/EUVRoseLibrary/Shared%20Documents/Digital%20Collections/Transfer%20and%20processing/DigitalArchives_MediaLog_Tier1Processing.xlsx?d=wdf9842da4bcb4997b1da1899ab188d4e&csf=1&web=1&e=AQ67Fv">media log</a> with one row for each carrier or file transfer/batch.** If the accession or collection contains only a few carriers/batches, you can record equivalent information in a .txt readme file or the accession record instead of a log spreadsheet. High-level or summary information about Tier 1 work that can't be captured in the accession log can also be recorded in the accession record. 
   * After accessioning is complete, upload the completed log or .txt readme, along with other relevant records, to the electronic CL-2 or CL-11 collection file on SharePoint and the PreservationDescriptionInfo folder in the collection's LIBSAFE Go container.

2. Extended physical processing (if the collection is hybrid, some of these preliminary steps might have already been completed during initial accessioning)
   * Remove any out-of-scope computer equipment and blank or nonfunctional media. Talk to a digital archivist about how to discard these items.
   * **Put loose CDs and DVDs in cases or sleeves.**
   * **Put internal hard drives in padded antistatic bags.***
   * **Label physical media.**
     * Write the disk number (the collection identifier followed by a sequential number; for example, 1315_05 or EUA283_100) on a small white sticker and apply it in a discreet location that will not harm the media (ideally on a case or enclosure, or directly on the media if no case is present or the media might become separated from the case).
     * Optical discs should be labeled on the clear plastic center ring, preferably with an optical media pen.
     * This number is used in the media log to identify the disk or transfer, in ArchivesSpace as the Component Unique Identifier for the Archival Object, and in the object metadata in LIBSAFE Go.
   
3. Transfer and ingest content
   * **[Set up folder structure](https://github.com/rose-collectionservices/digital-archives/blob/master/04%20Other%20How-Tos/Setting_Up_Folders.md) on working drive.**
   * **Image media or complete logical transfer of files.**
     * We don't have hard and fast rules about when to image vs. logically copy, so consulting a digital archivist is recommended. Decisions may be made at the level of the collection, media type, or individual carrier and involve considerations like the age and fragility of the media, PII and sensitivity concerns, content volume, and preservation intent.
     * See the [transfer and imaging instructions](https://github.com/rose-collectionservices/digital-archives/tree/master/03%20Imaging%20and%20Transfer%20Instructions) for more information on how to separate content from different types of media upon accessioning.
     * If the material arrived via any form of remote transfer other than direct submission to LIBSAFE Go (e.g., email, FTP, Dropbox, network drive) rather than on physical media, quarantine for 30 days on a working drive before proceeding.
     * If the material arrived via a LIBSAFE Go submission area, follow the [LSG accessioning workflow](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/03-LIBSAFE_Go_Documentation.md#rose-accessioning-workflow) for this and subsequent steps, referring back to this page to ensure all requirements outlined here are met.
   * Generate manifest with metadata and provenance information and scan for viruses.
     * For content submitted directly to LIBSAFE Go, use the platform's built-in virus scan and md5 checksum functions.
     * For content going into LIBSAFE Go via the Digital Archives lab, use any appropriate combination of tools prior to ingest.
       * For larger collections, [Fiwalk](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Generating_Fiwalk_reports.md) is most efficient.
       * For smaller collections or when Fiwalk can't generate a complete manifest, use FTK Imager to produce a directory list and hash list for each carrier/batch.
       * As of 2026, Microsoft Defender is the preferred virus scan tool. Talk to a digital archivist about other options if needed; available alternatives include ClamTk, Avast, and Crowdstrike.
       * After uploading content to LIBSAFE Go, repeat the virus scan and checksum calculation steps with the platform's built-in functions to check for accuracy and confirm successful ingest. To facilitate this, it's ideal when possible to either format the pre-ingest md5 manifest in a compatible manner so it can be verified by LIBSAFE Go or plan to package the content with Bagger (see next step). 
   * Assemble disk images/logically transferred content and supplemental files, including imaging or transfer logs, checksum manifests, DFXML files, and readmes.
     * [Bagging with Bagger](https://github.com/rose-collectionservices/digital-archives/blob/master/Imaging%20Instructions/Packaging_with_BagIt.md) is recommended for preservation copies of content prepared by an archivist outside LIBSAFE Go (vs. files transferred directly through submission areas).
   * Ingest packaged content and supplemental files into the LIBSAFE Go preservation repository (or prepare and move content already in LIBSAFE Go via a submission area).  
     * See the Emory Libraries [LIBSAFE Go wiki](https://emorylib.atlassian.net/wiki/spaces/LG/pages/405995521/Using+LIBSAFE+Go+Non-Admin+Users) on Confluence or Libnova's [product documentation](https://docs.libnova.com/libsafe-go) for detailed instructions on how to ingest into LISBAFE Go.
     * If content is ingested to LIBSAFE Go as a bag, verify using the built-in function.
     * Complete the LIBSAFE Go [accessioning workflow](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/03-LIBSAFE_Go_Documentation.md#rose-accessioning-workflow). Review the steps in the [processing workflow](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/03-LIBSAFE_Go_Documentation.md#rose-processing-workflow) as well and complete any that are appropriate; this workflow may be abbreviated for Tier 1 (e.g., no weeding or arrangement, minimal object metadata).
     * Upload log files, manifests, or similar information not contained in batch/disk-level bags (including the completed media log spreadsheet or .txt readme) to the PDI folder within the collection container.
   * If the collection includes web content, set up seed(s) in Archive-It, run a test crawl, QA the crawl, and configure recurring crawls if applicable. A digital archivist will usually handle web capture, but other accessioning or processing archivists may flag content for inclusion and support appraisal and description per [web archiving program guidelines](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/01-web_archives.md).

4. Describe content
   * Enter the metadata required by the preservation repository. See [schema and field usage guidelines in Confluence](https://emorylib.atlassian.net/wiki/spaces/LG/pages/210075651/Metadata) and [local practice notes](https://github.com/rose-collectionservices/digital-archives/blob/master/01%20General%20Topics/03-LIBSAFE_Go_Documentation.md#metadata) for details. (As of April 2026, these steps are optional. Full implementation is on hold pending further work on system integration and digital content modeling.)
     * For unprocessed material (preservation copies transferred as Tier 1) ingested into LIBSAFE Go, only the administrative metadata fields are required. Fill these out for the disk image file, not manifests and other supplemental files (if the material is later processed to a higher level, the processed copies will be assigned more extensive metadata).
   * Add basic descriptive information to the finding aid. Collection-level description should follow the requirements outlined in the [Collection Services Manual](https://github.com/rose-collectionservices/collection-services-manual/tree/master/05-DESCRIPTION) and include the following at minimum:
     * Collection-level access note: "Researchers must contact the Rose Library in advance for access to unprocessed born-digital materials in this collection. Collection restrictions, copyright limitations, or technical complications may hinder the Rose Library's ability to provide access to unprocessed born-digital materials."
   * Create an archival object for each physical carrier or batch of transferred files. Archival objects may be placed at the top level of the hierarchy, grouped intellectually with other materials into preliminary series, or gathered in a "born-digital materials" series as appropriate. See the [quick guide to processing digital media](https://github.com/rose-collectionservices/collection-services-manual/blob/master/10-PHYSICAL%20PROCESSING/readme.md#1074-processing-digital-media) for guidance on titling AOs if an accessioning archivist didn't already create titles.
     * For each AO that corresponds 1:1 with a specific carrier or transfer (they will in most cases, but large file transfers or complex collections might occasionally be different—consult a digital archivist), record the original carrier/batch identifier (the same number used to label disks, name disk image files, and record entries in the accession log—for example, 1309_51) in the AO's component unique identifier field.
     * File-level access note recommended for all born-digital AOs: "This born-digital material is unprocessed. Researchers must contact the Rose Library in advance for access. Use of the original digital media is restricted."
     * File-level access note recommended for all media that couldn't be imaged: "Due to technical complications, the Rose Library is currently unable to provide access to this unprocessed born-digital material."
   * Create a corresponding digital object record for every AO that represents the content of an original carrier/batch. Give the DO the same title as the AO. Following [Emory's metadata guidelines for digital archival objects](https://emory.sharepoint.com/:w:/r/sites/EmoryUniversityLibraries/Shared%20Documents/Staff/Committees%20%26%20Working%20Groups/Metadata%20Policy%20Committee/Archival%20Description%20Sub-Committee/Policy%20Documentation/Metadata%20Guidelines%20for%20Digital%20Archival%20Objects%20in%20ArchivesSpace%20at%20Emory.docx?d=w25158557429b4a4a867cf6fe6fd0946d&csf=1&web=1&e=5tb8UU), each DO record should have 1) a one-to-one relationship with an AO record and 2) a file version that links to the relevant disk image or batch of files in LIBSAFE Go. A DO might have multiple file versions if separate preservation and access copies exist.
   * If the AO is not a file transfer and is associated with physical media, also create an instance for the physical container housing the media (usually Box: BD1).
   * If the collection includes archived websites captured with Archive-It, create another accession record and add an AO and DO for each one in the finding aid. For more detailed instructions, see [accessioning and description guidelines for web archives](https://github.com/rose-collectionservices/collection-services-manual/tree/master/11-FORMAT%20SPECIFIC%20PROCEDURES#114-web-archives).

5. Log your work in [Airtable](https://airtable.com/invite/l?inviteId=inv3FmWzGzi5XrWvO&inviteToken=089e7964d2803ca1f3de9f9b867eb008531dfac68765d7556314eb61f9969e88&utm_medium=email&utm_source=product_team&utm_content=transactional-alerts) (if applicable), the Digital Archives tab of the [shelf list](https://emory.sharepoint.com/:x:/r/sites/BoxDeletedUsers14/Shared%20Documents/aczebla_emory_edu/MARBL_Master%20SHELF%20LIST/Shelf%20List.xlsx?d=wf0968fe689044379898108b0228a3a62&csf=1&web=1&e=Ln9kIl), and the [annual processing stats spreadsheet](https://emory.sharepoint.com/:x:/r/sites/EUVRoseLibrary/Shared%20Documents/Reports%20and%20Statistics/Collection%20Services/Manuscript%20Processing%20Statistics/Annual%20Processing%20Reports.xlsx?d=we8382d29282646d8a17b240c1a701e96&csf=1&web=1&e=fchlSs&nav=MTVfezMxMEVCMDA1LTdFQzMtNDIyQS04NjIzLUI2MTJGQ0VERTg0Qn0).

## Accessioning Checklist for Born-Digital Content
There are [two versions of the checklist](https://emory.sharepoint.com/:w:/r/sites/EUVRoseLibrary/Shared%20Documents/Digital%20Collections/Transfer%20and%20processing/Templates/Accessioning%20Checklist%20for%20Born-Digital%20Content.docx?d=w58343e7735794a51a6ed9fac99aa61a0&csf=1&web=1&e=CkChHx): one for digital-only accessions and the other for accessioning digital content from hybrid accessions or otherwise processed collections. The checklist is not required and does not become part of the collection file, but it can be a useful tool. Note that not all steps will apply in every situation, so the archivist should adapt as needed.

## Size Estimates

Standard disk sizes (to help fill out the [processing plan] size estimate):

| Media               | Size    |
|---------------------|---------|
| 5.25" floppy disk   | 1.2 MB  |
| 3.5" floppy disk    | 1.4 MB  |
| ZIP 100 disk        | 100 MB  |
| ZIP 250 disk        | 250 MB  |
| Optical disc        | 700 MB  |
