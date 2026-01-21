# LIBSAFE Go
[This page is under construction.]

LIBSAFE Go (LSG) is the preservation repository for most born-digital material—disk images, logical transfers, and processed files. A separate node within LIBSAFE Go is also used to make processed, unrestricted access copies of born-digital material available in the reading room. Legacy born-digital material (primarily disk images with some tar files of processed material) is stored in The Keep, but we have plans to migrate this content to LIBSAFE Go in 2026.

As much as possible, Rose Library's LIBSAFE Go workflows and policies should align with general Collection Services procedures and with the information contained in the TDS-managed [LIBSAFE Go Confluence wiki](https://emorylib.atlassian.net/wiki/spaces/LG/overview?homepageId=160465038). This page is used to add Rose-specific details that are difficult to outline within the processing workflow document and to clarify how Rose Library is interpreting and applying broader data models and policies within our LIBSAFE Go content nodes.

Some notes on LIBSAFE Go content structure:
* Preservation copies live in the permanent MSS or EUA node within LIBSAFE Go. Each collection has a single container.
* Within each collection container should be two to four directories (all four are part of the template copied automatically when you create a new container):
  * Required: MSS####_PreservationDescriptionInfo (for logs, manifests, and other documentation generated during transfer and processing and not bagged with a specific disk image or batch of files).
  * Required: MSS####_Originals (for disk images or packaged logical transfers ingested during the Tier 1 workflow).
  * Used when applicable: MSS####_ProcessedFiles (for extracted and processed files produced during a Tier 2b/3 workflow)
  * Used when applicable: MSS####_RestrictedFiles (for files that are restricted for a period of time, files that have been extracted from a disk image but require further processing prior to access, such as .pst files, etc.)
* The content of MSS####_ProcessedFiles is also ingested to the appropriate collection folder within the RRR - Rose Reading Room node. This is considered a convenience copy for end-user access. The copy stored in EUA - Emory University Archives Node or EUA - Emory University Archives Node is the copy of record. Archivists should take care to make any changes in both places.
* Containers for some legacy collections or collections with unique acquisition and processing workflows, such as EUA 177 (Department of Music collection), may employ a different structure.

Restricted content in LSG:
* All disk images and other unprocessed original copies should be tagged as restricted. Accompanying reports and logs need not be.
* Content extracted from originals that is embargoed or otherwise restricted per Rose Library policy or donor agreement should also be tagged as restricted. Typically such items will be placed in the container's MSS####_RestrictedFiles folder, provided their original locations are not essential or we can easily restore original order when they are opened in the future. In some cases, restriction management and future reversal might be more straightforward if the restricted files remain in their original locations within MSS####_ProcessedFiles but are removed from the corresponding folder in the user-accessible RRR - Rose Reading Room node; in this situation, however, it is extremely important to accurately tag the files and keep careful records in the collection file and in the MSS####_PreservationDescriptionInfo folder explaining the circumstances.

Accessioning vs. processing "workflows":
* These terms as used for LSG workflows do not map perfectly onto other Rose Library uses. For LSG purposes, the Archival Accessioning Workflow outlines the steps involved in preliminary review, logging, and stabilization of content submitted by donors/creators and is used only in the Accessioning Node, where containers are generated through submission area uploads. The Archival Processing Workflow, applied to containers in the EUA and MSS nodes where permanent collection containers live, outlines the steps for more complete physical and intellectual control. Some steps, such as recording object metadata or reviewing content analysis, might be relatively minimal for content processed at Tier 1 and more extensive Tiers 2-3. See the processing tier workflows for guidance. 
* Content uploaded by an archivist after disk imaging or other accessioning and processing steps outside the LSG platform can go directly into the permanent collection node and follow the Archival Processing Workflow. (It is assumed steps equivalent to those in the Archival Accessioning Workflow will have already been completed.)
* For EUA acquisitions only: Some collections do not yet have finding aids, and creating resource records at the point of accessioning is not always feasible (or necessary, especially if the materials will be closed for a period of time). When moving EUA records through the LSG processing workflow, pause at the resource record step if a finding aid has not been created. A digital archivist will revisit and complete the workflow when a finding aid is needed.

Metadata for files other than those in MSS####_ProcessedFiles (and equivalent folders in RRR Rose Reading Room):

