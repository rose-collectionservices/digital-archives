# LIBSAFE Go
[This page is under construction.]

LIBSAFE Go (LSG) is the preservation repository for most born-digital material—disk images, logical transfers, and processed files. A separate node within LIBSAFE Go is also used to make processed, unrestricted access copies of born-digital material available in the reading room. Legacy born-digital material (primarily disk images with some tar files of processed material) is stored in The Keep, but we have plans to migrate this content to LIBSAFE Go in 2026.

As much as possible, Rose Library's LIBSAFE Go workflows and policies should align with general Collection Services procedures and with the information contained in the TDS-managed [LIBSAFE Go Confluence wiki](https://emorylib.atlassian.net/wiki/spaces/LG/overview?homepageId=160465038). This page is used to add Rose-specific details that are difficult to outline within the processing workflow document and to clarify how Rose Library is interpreting and applying broader data models and policies within our LIBSAFE Go content nodes.

Some notes on LIBSAFE Go content structure:
* Preservation copies live in the permanent MSS or EUA node within LIBSAFE Go. Each collection has a single container.
* Within each collection container should be two to four directories:
  * Required: MSS####_PreservationDescriptionInfo (for logs, manifests, and other documentation generated during transfer and processing.
  * Required: MSS####_Originals (for disk images or packaged logical transfers ingested during the Tier 1 workflow).
  * Used when applicable: MSS####_ProcessedFiles (for extracted and processed files produced during a Tier 2b/3 workflow)
  * Used when applicable: MSS####_RestrictedFiles (for files that are restricted for a period of time, files that have been extracted from a disk image but require further processing prior to access, such as .pst files, etc.)
* The content of MSS####_ProcessedFiles is also ingested to the appropriate collection folder within the RRR - Rose Reading Room node. This is considered a convenience copy for end-user access. The copy stored in EUA - Emory University Archives Node or EUA - Emory University Archives Node is the copy of record. Archivists should take care to make any changes in both places.

Restricted content in LSG:
* All disk images and other unprocessed original copies should be tagged as restricted. Accompanying reports and logs need not be.
* Content extracted from originals that is embargoed or otherwise restricted per Rose Library policy or donor agreement should also be tagged as restricted. Typically such items will be placed in the container's MSS####_RestrictedFiles folder, provided their original locations are not essential or we can easily restore original order when they are opened in the future. In some cases, restriction management and future reversal might be more straightforward if the restricted files remain in their original locations within MSS####_ProcessedFiles but are removed from the corresponding folder in the user-accessible RRR - Rose Reading Room node; in this situation, however, it is extremely important to accurately tag the files and keep careful records in the collection file and in the MSS####_PreservationDescriptionInfo folder explaining the circumstances.

Accessioning vs. processing "workflows":

Metadata for files other than those in MSS####_ProcessedFiles (and equivalent folders in RRR Rose Reading Room):

