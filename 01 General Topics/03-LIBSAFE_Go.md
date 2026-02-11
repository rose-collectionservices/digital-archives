# LIBSAFE Go
[This page is under construction.]

LIBSAFE Go (LSG) is the preservation repository for most born-digital material—disk images, logical transfers, and processed files. A separate node within LIBSAFE Go is also used to make processed, unrestricted access copies of born-digital material available in the reading room. Legacy born-digital material (primarily disk images with some tar files of processed material) is stored in The Keep, but we have plans to migrate this content to LIBSAFE Go in 2026.

As much as possible, Rose Library's LIBSAFE Go workflows and policies should align with general Collection Services procedures and with the information contained in the TDS-managed [LIBSAFE Go Confluence wiki](https://emorylib.atlassian.net/wiki/spaces/LG/overview?homepageId=160465038). This page is used to add Rose-specific details that are difficult to outline within the processing workflow document and to clarify how Rose Library is interpreting and applying broader data models and policies within our LIBSAFE Go content nodes.

# LIBSAFE Go content structure
* Preservation copies live in the permanent MSS or EUA node within LIBSAFE Go. Each collection has a single container.
* Within each collection container should be two to four directories (all four are part of the template copied automatically when you create a new container):
  * Required: MSS####_PreservationDescriptionInfo (for logs, manifests, and other documentation generated during transfer and processing and not bagged with a specific disk image or batch of files).
  * Required: MSS####_Originals (for disk images or packaged logical transfers ingested during the Tier 1 workflow). Each original media carrier or batch will typically have a folder within this directory.
  * Used when applicable: MSS####_ProcessedFiles (for extracted and processed files produced during a Tier 2b/3 workflow)
  * Used when applicable: MSS####_RestrictedFiles (for files that are restricted for a period of time, files that have been extracted from a disk image but require further processing prior to access, such as .pst files, etc.)
* The content of MSS####_ProcessedFiles is also ingested to the appropriate collection folder within the RRR - Rose Reading Room node. This is considered a convenience copy for end-user access. The copy stored in EUA - Emory University Archives Node or EUA - Emory University Archives Node is the copy of record. Archivists should take care to make any changes in both places.
* Containers for some legacy collections or collections with unique acquisition and processing workflows, such as EUA 177 (Department of Music collection), may employ a different structure.

# Restricted content in LSG
* All disk images and other unprocessed original copies should be tagged as restricted. Accompanying reports and logs need not be.
* Content extracted from originals that is embargoed or otherwise restricted per Rose Library policy or donor agreement should also be tagged as restricted. Typically such items will be placed in the container's MSS####_RestrictedFiles folder, provided their original locations are not essential or we can easily restore original order when they are opened in the future. In some cases, restriction management and future reversal might be more straightforward if the restricted files remain in their original locations within MSS####_ProcessedFiles but are removed from the corresponding folder in the user-accessible RRR - Rose Reading Room node; in this situation, however, it is extremely important to accurately tag the files and keep careful records in the collection file and in the MSS####_PreservationDescriptionInfo folder explaining the circumstances.

# Accessioning and processing "workflows"
These terms as used for LSG workflows do not map perfectly onto other Rose Library uses. For LSG purposes, the Archival Accessioning Workflow outlines the steps involved in preliminary review, logging, and stabilization of content submitted by donors/creators and is used only in the Accessioning Node, where containers are generated through submission area uploads. The Archival Processing Workflow, applied to containers in the EUA and MSS nodes where permanent collection containers live, outlines the steps for more complete physical and intellectual control. 

Some steps, such as recording object metadata or reviewing content analysis, might be relatively minimal for content processed at Tier 1 and more extensive at Tiers 2-3. See the processing tier workflows for guidance. 

## Rose accessioning workflow 
Any content uploaded the Rose Accessioning Node either directly or via submission areas should go through this workflow. It includes the minimum required steps to gain basic control of the content. If staff upload content directly into a collection container (for example, after processing files received on physical media) they should ensure equivalent steps are taken prior to entering the processing workflow. 
1. Save submission form and agreement
   * This step is for content uploaded by external contributors through a submission area.
   * Save a generic copy of the submission form and agreement, merged with a screenshot of the submission container metadata, in SharePoint in place of a transfer form/deed and link to this file from the accession record.
2. Rename container with accession number
   * Enter the accession number for the content in place of the automatically generated alphanumeric title. 
3. Review submission
   * Check to make sure all expected content is present and matches any submitted metadata.
   * Weed files that should not be preserved.
4. Create accession record
   * This step is performed in ArchivesSpace but is used in LSG to flag content that is not yet officially documented in an accession record.
   * Any important information received as part of the submission container metadata should be added to the ArchivesSpace accession record, as this information won’t transfer with the files to their permanent containers.
5. Create md5 manifest
   * Click “Explore Content,” select all folders/files within the viewer, and click “create-md5-manifest” in the “Functions” menu on the right side.
   * Enter a file name for the manifest using the accession number or batch identifier (ex. “2020-08-08_manifest”).
   * After the process finishes running, refresh the container to make sure the manifest has appeared.  
6. Create permanent collection container (if applicable)
   * Check the appropriate node or subnode to see if a container for the collection already exists.
7. Create folder in collection container for each disk/accession/batch
   * See [content structure instructions](#LIBSAFE-Go-content-structure) above for guidelines on grouping and naming.
8. Copy files to collection container
   * Select all content and use the Functions pane to copy it to the permanent collection container in the appropriate node.
   * Do not do anything else in either the source or destination container until the job is complete. 
9. Update accession record
   * Add any essential notes based on further content review or preservation steps taken during accessioning.
   * Include in the record a list of any original carrier/batch identifiers associated with the content.
10. Delete submission/accessioning container
    * Do this only after the move is complete, you’ve verified the md5 manifest, and the content in the permanent container has gone through the processing workflow.
   
## Rose processing workflow 
Any time new content is added to a permanent collection container, the archivist should restart the Archival Processing Workflow and go through each applicable step.  

1. Assign/update container metadata 
2. Validate bags (if applicable)
    * If any content was bagged prior to submission/ingest, use the validation function to ensure it is complete and correct. 
3. Dedupe/weed/arrange files (if applicable)
   * Note that for large or complex collections, it might be best to complete this step outside LSG on a processing workstation and ingest the content already arranged. This is because 1) the move and copy functions in LSG can be slow, 2) it is easy to cause discrepancies or lose information by changing container content while previous processes are running, 3) LSG lacks tools that might be useful in processing (e.g., for normalization or PII detection).
4. Create md5 manifest
   * Content moved from the Accessioning Node will already have a manifest, but creating a second one is recommended to ensure it reflects any deletions or changes made during processing and contains all files, including those that might have already been in the collection container.
   * Submission-level manifests and all previous validation results should be moved to the PDI folder, but the latest manifest for the entire container should remain at the top level to enable periodic fixity checking. 
5. Review content analysis
   * Generating the content analysis may take a day or two after upload, so be prepare to pause and wait at this step.
   * Check for viruses, duplicate files, at-risk file formats, etc.
   * Document any important findings in the collection file and/or accession record.
   * Consult a digital archivist before altering or removing files based on the results of the content analysis.
7. Upload documentation
    * Gather any manifests, logs, submission agreements, metadata spreadsheets, etc. and place it in the PDI folder.
8. Assign object metadata
   * See the Creating Object Metadata and Using Excel Metadata Import sections of this guide. 
9. Tag restricted objects (if applicable) 
10. Create DOs
   * Follow digital content description guidelines for ArchivesSpace to create digital object records and record LSG links.
   * Your collection might have a single DO for all content in LSG or more granular DOs. See the Container Organization section for more guidance.
   * Any DO record, regardless of level of description, must correspond 1:1 with a folder (top level or subfolder) or item within the collection container. 
11. Update resource record
   * This step takes place in ArchivesSpace but must be completed as part of the process to ensure all content stored permanently in LSG is described in a resource record (aggregate representation is fine).
   * Follow ArchivesSpace field usage guidelines and local practice to decide which notes and other fields should be updated. 











## Notes on using workflows
* Content uploaded by an archivist after disk imaging or other accessioning and processing steps outside the LSG platform can go directly into the permanent collection node and follow the Archival Processing Workflow. (It is assumed steps equivalent to those in the Archival Accessioning Workflow will have already been completed.)
* For EUA acquisitions only: Some collections do not yet have finding aids, and creating resource records at the point of accessioning is not always feasible (or necessary, especially if the materials will be closed for a period of time). When moving EUA records through the LSG processing workflow, pause at the resource record step if a finding aid has not been created. A digital archivist will revisit and complete the workflow when a finding aid is needed.

* 

# Metadata 
* Files in MSS####_ProcessedFiles (and equivalent folders in RRR Rose Reading Room) should have object-level metadata assigned, with required fields completed at minimum.
* Files in MSS####_Originals and MSS####_RestrictedFiles are not intended for end-user access, so object-level metadata is a lower priority and a reduced number of completed fields may be appropriate. Administrative metadata fields (ArchivesSpace ID, original object/batch ID, accession number, and PID) are still required when applicable.
* Files in MSS####_PreservationDescriptionInfo do not need object metadata assigned. 

* For unprocessed material (preservation copies transferred as Tier 1) ingested into LIBSAFE Go, only the administrative metadata fields are required. Fill these out for the disk image file itself. (If the material is later processed to a higher level, the processed copies will have more extensive metadata assigned.)

