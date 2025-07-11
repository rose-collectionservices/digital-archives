# Web Archiving

## Program Goals
The goal of web archiving is to capture a web-based resource so that it behaves and looks the same way as on the live web. The process begins using a web crawler, which captures all the source material from the web page as it exists on the live web including images, text, and any supplemental programs or stylesheets. These files are wrapped into a WARC file (a web archive file).

## Collection Development Policy
Written January 2019, revised January 2022

The Rose Library collects, preserves, and provides access to websites and web-based material in two distinct areas: the Emory University web archives and the Rose Manuscript Collections web archives. The web archives collections reflect and complement the mission and priorities of other collecting areas within the Rose Library, and collecting decisions should be content-centered and format-agnostic to the greatest extent possible. As Rose Library’s collecting areas shift and grow, the Rose Library web archives will evolve as well.

The selection of web content for archiving is an extension of selection performed for materials in other formats and is thus led by the University Archivist or Collection Development team members. The Digital Archives unit is responsible for initiating web captures upon request, selecting and maintaining appropriate tools for use in the web archives program, and preserving the collected web archives. The Digital Archives unit may also advise on and participate in accessioning, describing, and providing access to collected web content alongside the Accessioning Archivist, Collection Processing unit, and Research Services unit.

### Emory University Archives Priorities 
The Emory University Archives seeks to preserve collections of websites produced by Emory’s administrative offices, schools, departments, institutes, centers, and programs, as well as its faculty, student, and alumni organizations, with a particular focus on websites containing content that falls within the Emory University Archives collecting scope regardless of format. Decisions about which websites and pages are in scope for the Emory University web archives are primarily the responsibility of the University Archivist. The Digital Archives unit is also authorized to carry out appraisal and selection decisions in consultation with the Emory University Archivist and following the selection criteria outlined below.
* The website complements or has related material amongst the University Archives’ manuscript and archival collections.
* The website documents significant administrative, instructional, research, creative, ceremonial, or social functions and activities of Emory University; its components units, employees, or students; and affiliated organizations.
* The website reflects significantly on alumni, organizations, individuals, or events associated with, but not officially part of, Emory University.

### Rose Library Manuscript Collections Priorities
The web archives support the broader analog and digital collecting efforts of the Rose Library and thus mirror the collecting scope and priorities for the Rose Library’s manuscript collections in general.  Curators are responsible for suggesting websites or pages for inclusion in the Rose Library’s web archives based on their collecting goals and knowledge of specific collections. The Digital Archives unit, in consultation with curatorial staff, may also choose to initiate captures of web content that align with the following criteria: 
* The website or its content was created or maintained by a person or organization whose records the Rose Library holds.
* The website contains unique content that documents the work and/or thought of a person or organization represented in the Rose Library’s collections.
* The website includes unique content that is not duplicated in paper records already held by Emory.
Websites that are indirectly related to a person or organization represented in Rose Library collections are generally out of scope, but some third-party websites may be captured if they offer significant unique perspective or essential context that may not be documented elsewhere.

### Technical Requirements
Websites must be capturable by current technology employed by the Rose Library. The following types of web content can typically be captured:
* Static websites
* Social media accounts, pages, feeds, or hashtags
* Downloadable files in common formats hosted on web pages

The following content will be captured only with permission from the creator or owner:
* Social media pages or posts visible only to certain viewers 
* Content designated as off-limits by a webmaster via exclusions in robots.txt files
(except in the case of emory.edu sites that require ignoring robots.txt to crawl effectively)

The following types of content typically cannot be captured or require special intervention:
* Dynamic content 
* Database-generated or server-side content
* Streaming media
* POST requests
* Content unavailable on the live web
* Most content that cannot be made publicly available
* Most content that requires login credentials to access
* Sites with specialty certificates or two-factor authentication

Websites that do not fit the technical parameters outlined above may be considered for archiving on a case-by-case basis. The Digital Archives unit reserves the right to deem a website ineligible. Although the Rose Library makes every effort to produce exact capture of websites that are in scope and eligible for capture, technological limitations may still result in incomplete preservation of website content, appearance, and/or functionality. Partial crawls of a selected seed, capture of content using non-WARC formats, or other alternative approaches may be appropriate depending on size restrictions, technical limitations, or collecting scope. 

### Reappraisal
The Rose Library reserves the right to reappraise material that no longer aligns with its mission or fits its collection scope as well as material that cannot be adequately preserved by Emory. 

An archived website may be removed from Rose Library collections if:
* The site no longer reflects the mission or the collecting priorities of the Rose.
* There are legal or ethical concerns about maintaining the website or its content as part of the collection.
* Another institution or consortial project has committed to preserving and providing ongoing access to the content.
* The archived website no longer retains its integrity, identity, or authenticity.
* The archived versions of the website have technical issues to the extent that patrons will not be able to use them for research.

Crawls may be discontinued but previously archived versions of a website retained if:
* The value of the site is limited to a specific time period and does not necessitate ongoing capture.
* The website has had no significant changes for at least 3 years or more.
* The architecture or design of the site no longer allows successful capture. 

Although the Rose Library will not monitor the live versions of already captured websites for subsequent deletions or permission changes, we will evaluate requests for removal of this content in accordance with the Emory Libraries takedown policy and relevant Rose Library policies governing deaccessioning.

## Content Selection

### Seed Requests & Changes
Because of their collection development duties, curators and the university archivist are primarily responsible for identifying web content that should be archived; however, processing archivists, digital archivists, and others who encounter eligible content in the course of their work may also submit requests.

Web content to be captured at the time a collection is acquired should be reported by the curator in the Potential Acquisitions Report Form. Once aware of the web content, the accessioning archivist will ensure it is covered in the acquisition paperwork and create a stub accession record for the web content (this should be a separate record from the non-web contents of the collection). The accessioning archivist will then assign the web-based accession to a member of the Digital Archives unit for configuration, capture, accessioning, and description per the guidelines below. Web-only collections will follow a similar workflow, with specific procedures determined case by case.

Web content discovered after the point of acquisition—during accessioning, processing, or use of the collection—should be reported by archivists using the Submit Web Archives Capture form (https://airtable.com/shrihCiXDQ2GL8k52). After receiving the form, the accessioning archivist will create a stub accession record associated with the existing resource record and assign accessioning duties to a member of the Digital Archives unit. Digital Archives will configure, capture, accession, and describe the content. For these captures, a deed is typically not required but Digital Archives may choose to notify website owners as appropriate.

The Digital Archives unit will review web content proposed for acquisition, determine the appropriate tier (see below) and crawl scope based on the collection development policy for web archives and the nature of the content, initiate or revise crawls, and conduct QA checks. 

After web content has been captured, an archived website or active seed may require updates for a variety of reasons (i.e., the seed URL has changed and should be updated in Archive-It, the crawl tier should be adjusted to change the capture frequency or QA level, the website is now inactive or out of scope and future crawls should be canceled, we need to consider deaccessioning, the information in the finding aid is incorrect). Rose staff members may suggest changes to the by submitting the Web Archives Change Request form (https://airtable.com/shr0cho8ZEhZASD81). Required information includes the URL of the website in question and a description of what needs to be reviewed or changed. 

### Crawl Tiers
When initiating new captures or reviewing recurring crawls, the Digital Archives unit will follow the frequency and QA guidelines for the most appropriate tier.

| **Tier** 	| **Frequency**               	| **QA Level**                                                                                                                                                       	| **Use Cases**                                                                                            	|
|----------	|-----------------------------	|--------------------------------------------------------------------------------------------------------------------------------------------------------------------	|----------------------------------------------------------------------------------------------------------	|
| **1**    	|     One-time                	|     Thorough QA of main page(s) upon capture, cursory review of subpages.                                                                                          	|     Static, infrequently updated sites. Content that is in scope only at a particular moment in time.    	|
| **2**    	|     Annual                  	|     Thorough QA of initial capture. For subsequent captures, QA based on Archive-It crawl reports and spot checks.                                                 	|     Infrequently updated sites.                                                                          	|
| **3**    	|     Quarterly or monthly    	|     Thorough QA of top-level pages and cursory review of other pages in initial capture. For subsequent captures, minimal QA based on Archive-It crawl reports.    	|     Frequently updated content, such as news sites, blogs, and social media feeds.                       	|

### Permission
The Digital Archives unit aims to strike a balance between, on the one hand, respecting the intellectual property and privacy rights of content owners and, on the other, the need to capture ever-growing volumes of critical online content and manage web archives at scale.

Archived web content is subject to Emory Libraries policies regarding takedown and deletion. Requests for removal of previously captured content will be referred for consideration under Emory Libraries’ and the Rose Library’s takedown and deaccessioning policies.

#### Emory University Domains 
For content hosted on Emory University domains, which the Rose Library collects as part of the Emory University Archives’ preservation remit, we do not notify or seek permission from website creators and managers. We will ignore robots.txt prohibitions when necessary to troubleshoot crawls and ensure more complete capture. For web content in this category, there is no opt-out option except by request of the Office of Information Technology or Office of the General Counsel. 

#### Emory University Content on Other Domains
If digital archivists and the university archivist reasonably believe the content in question to be Emory property or covered by an existing deed of gift or transfer agreement, and if the site terms and conditions do not prohibit archiving, we will crawl such content without notification or permission. However, we will respect robots.txt and ensure the crawl scope is defined as narrowly as possible to obtain the content. For web content in this category, site owners or content managers may opt out of web archiving. We will cease crawling if requested by content owners.

#### Non-Emory Content
For content not associated with Emory University (e.g., most web content crawled in connection with Rose Library manuscript collections), we will make best efforts to notify and obtain permission from the rightsholder, ideally in a deed of gift or born-digital addendum. When the content is of critical importance and obtaining written permission is not feasible, we will proceed with capture. We will honor requests from copyright owners to cease crawling their content. 

#### Private Content
Content from any of the above categories that is password protected or otherwise not visible on the open web will be crawled only with the permission and cooperation of its owner or manager. 

## High-Level Workflows

Web content as part of initial acquisition
1. Curator determines that a prospective acquisition includes online content.
2. Curator includes description of web content on Potential Acquisitions Report Form.
3. Accessioning archivist notifies head of digital archives about incoming web content.
4. Curator and head of digital archives meet to discuss web content and how it fits into collection.
5. Curator and accessioning archivist ensure Deed of Gift or Sale mentions “web content” and born-digital addendum is attached.
6. Accessioning archivist creates stub accession record for web content (separate record from record for any non-web collection material) and assigns accessioning to Digital Archives. 
7. In consultation with curator, Digital Archives locates all prospective web content and selects appropriate capture method.
8. Digital Archives captures content or configures recurring crawls.
9. Expands stub accession record, adds metadata to Archive-It (if applicable), and adds archival objects and metadata to resource record.

Web content discovered during accessioning or processing:
1. Archivist identifies online content related to donor/collection and in scope for capture.
2. Archivist reports content via the Submit Web Archives Capture form (https://airtable.com/shrihCiXDQ2GL8k52).
3. Accessioning archivist creates stub accession record (without Deed of Gift or Sale) and assigns accessioning to Digital Archives.
4. Digital Archives consults processing archivist or curator to gather more information and determine how content fits in collection.
5. Digital Archives captures content or configures recurring crawls.
6. Digital Archives expands stub accession record (including rationale for capture after initial acquisition), adds metadata to Archive-It (if applicable), and adds archival objects and metadata to resource record.
7. Digital Archives sends notification to site owner if appropriate.

Recurring crawls that need changes:
1. Curator or archivist determines that an existing seed should be changed.
2. Curator or archivist fills out the Web Archives Change Request form (https://airtable.com/shr0cho8ZEhZASD81).
3. Digital Archives reviews change request, gather additional information as needed, and decides whether to proceed. 
4. If change requires external review (e.g., request for deaccessioning and deletion), Digital Archives routes appropriately.
5. Digital Archives updates the seed settings, descriptive metadata, or other elements as needed. 

## Using Archive-It
Archive-It is the Rose Library’s primary tool for capturing archived websites; it also indirectly supports collection management and access functions. Other tools are used as needed for atypical use cases or difficult content, but our default procedures are based on Archive-It’s terminology and interface. 

Staff may access Emory Libraries' Archive-It dashboard at https://partner.archive-it.org/1017. Archive-It does not use SSO; log-in credentials are managed by the Emory University Archivist and the Rose Library digital archivists.

Currently the Rose Library maintains two public collections organized by administrative unit: 
* Emory University Archives web archives: contains web assets on the Emory domain OR  produced by Emory University faculty, staff, or students
* Emory Manuscript Collections web archives: contains web assets related to collections held by the Rose Library; generally these have been created or maintained by a person or organization whose records the library holds.  
New collections may be added in consultation with the Digital Archives unit.

For definitions of web archiving terms, explanations of the Archive-It interface and features, instructions for routine tasks (such as adding new seed URLs to a collection or verifying the completeness and accuracy of a crawl), and troubleshooting, visit the <a href="https://support.archive-it.org/hc/en-us/categories/201179946-Archive-It-User-Guide">Archive-It support pages</a>. 

## Accessioning and Describing Web Archives
See the <a href="https://github.com/rose-collectionservices/collection-services-manual/blob/master/11-FORMAT%20SPECIFIC%20PROCEDURES/readme.md#114-web-archives">Format-Specific Procedures</a> section of the Collection Services manual.

## Access
Most researchers will access websites captured with Archive-It through one of two methods:
1. Following a pointer from an ArchivesSpace resource record to the Wayback interface for a specific seed. (See <a href="https://github.com/rose-collectionservices/collection-services-manual/tree/master/11-FORMAT%20SPECIFIC%20PROCEDURES#114-web-archives">web archives description guidelines</a> for creating AOs in finding aids.)
2. Searching or browsing in the Rose Library’s Archive-It collection page. 
Other methods may be used when needed, but Digital Archives will not actively support them unless adopted as preferred approaches.

For content captured using another tool and not available through an online WARC viewer, researchers’ access will be mediated using one of the following methods:
1. When appropriate based on the nature and format of the content (e.g., basic HTML pages, individually saved files, static PDF or JPG renderings of page content), we will make it available through our normal workflow for reading room or remote access to born-digital material.
2. For more complex captures saved as WARC files, we will temporarily upload the packaged content to a web-based WARC viewer such as Conifer and share a link with the researcher. Like other temporary access to online content, such as through Aviary or The Keep, access will remain valid for 30 days, after which we will take down the uploaded content to save space and avoid the need to maintain the access copy indefinitely. 

## Preservation
At present, content captured through Archive-It is stored and preserved solely by the Internet Archive. A future goal is to develop a workflow using the Archive-It API to download copies of WARC for preservation in an Emory Libraries preservation system; these local copies would be maintained for preservation only and access still provided through Archive-It unless or until the Internet Archive ceases to maintain Archive-It or Emory’s digital repository includes a WARC viewer we prefer to the Internet Archive’s.

Content captured using tools and methods other than Archive-It is treated like other born-digital collection material for the purposes of preservation. WARCs or sets of files in other formats are packaged and uploaded to a designated system, such as The Keep or LIBSAFE Go, for storage and monitoring. 

Any web content stored within Emory Libraries’ centrally managed preservation ecosystem is subject to the Libraries’ policies about preservation, retention, and deletion. Decisions about long-term management of the content should align with those policies. Regardless of the system used to store and manage the content, Rose Library staff should follow established Rose and Emory Libraries processes for appraisal, deaccessioning, and takedown requests.
