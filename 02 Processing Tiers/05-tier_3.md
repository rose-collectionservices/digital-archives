# Tier 3 - Full Processing with Restrictions
The Tier 3 workflow is identical to Tier 2b except for the addition of steps to implement content review and restriction. To process at the Tier 3 level, begin after deduplication in the [Tier 2 instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Processing%20Tiers/Tier%202.md). Follow the instructions below for PII review and implementation of restrictions before any normalization or arrangement work. Then return to complete the remaining steps as described for [Tier 2b](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/04-tier_2b.md), noting that the arrangement and description steps will likely involve a higher degree of complexity and level of intervention for collections at Tier 3. Record Tier 3 actions and observations in a .txt readme file, digital processing plan, or media log spreadsheet (recommended for large, complex collections). 

A note on restrictions: Restrictions set by the donor and outlined in the Deed for physical material should be carried over to born digital materials, unless explicitly stated otherwise. There may also be cases where there are additional restrictions on born digital material, separate from physical material. Record observations, decisions, and actions in 

---

## Bulk Reviewer/BulkExtractor
*This step should take place in the BitCurator/Ubuntu environment. Please see [Switching from BitCurator to Windows](#switching-to-bitcuratorubuntu-from-windows) for instructions to switch.*</br>
1. [Official Bulk Reviewer documentation](https://bulk-reviewer.readthedocs.io/en/latest/) (Right-click to open in new tab) 
2. [Bulk Reviewer GitHub page](https://github.com/bulk-reviewer/bulk-reviewer) (Right-click to open in new tab)

*Notes:* 
* Bulk Reviewer is already downloaded on the lab computer. The application is in the Forensics and Reporting folder on the desktop. Bulk Extractor is located in the same folder, and comes pre-installed in BitCurator. 
* Following the official documentation is the easiest way to use Bullk Reviewer. 
* If using a regular expressions text file to search for specific terms or topics that are restricted, make sure it is placed on the Desktop and then copied to the hard drive once the scan is complete. 
* For the regular expressions file, use only one word per line. Phrases or names like "Billy Bob Joe" will need to be on a single line each. There will also need to be a capital version and a lower-case version (ex. "Bob" and "bob"). There is no need for quotation marks within the text file itself. </br>
*Example:* </br> ```Billy```</br> ```billy``` </br> ```Bob``` </br> ```bob``` </br> ```Joe``` </br> ```joe``` </br>
*Note:* This will often bring up other content, but Bulk Reviewer has a preview function which shows in-context placement, so you can quickly identify if it needs to be restricted or not. </br>
* Save any reports to a folder on the Desktop (ex. BurkeBR), since it doesn't like to save to the hard drive due to the naming convention of the hard drive. 
* Sometimes there will be an error code, but it will still show the results. Sometimes it's really an error code, so keep an eye on it. 

---

## Examples
* [Alice Walker papers](https://findingaids.library.emory.edu/documents/walker1061/)
* [Rita Ann Higgins papers](https://findingaids.library.emory.edu/documents/higgins1194/)
* [Southern Christian Leadership Conference records](https://findingaids.library.emory.edu/documents/sclc1083/)
* [Eamon Grennan papers](https://findingaids.library.emory.edu/documents/grennan1150/)
* [Tracy K. Smith papers](https://findingaids.library.emory.edu/documents/smith1468/)
* [Alli Royce Soble papers](https://findingaids.library.emory.edu/documents/soble1315/)

[Back to top](#table-of-contents)
