# Tier 3 - Full Processing with Restrictions
The Tier 3 workflow further extends Tiers 2 and 2b with steps to implement content review and restriction when needed based on the deed, born-digital addendum, and/or archivists' observations about the content during the Tier 1 and 2 steps. Note that restrictions set by the donor and outlined in the deed for physical material should be carried over to born-digital materials, unless explicitly stated otherwise. There may also be cases where there are additional restrictions on born digital material, separate from physical material. 

To process at the Tier 3 level, begin after deduplication in the [Tier 2 instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/Processing%20Tiers/Tier%202.md) or after normalization and arrangement in the [Tier 2b instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/04-tier_2b.md) as appropriate. When finished, return to the [Tier 2 instructions](https://github.com/rose-collectionservices/digital-archives/blob/master/02%20Processing%20Tiers/03-tier_2.md) for the final workflow steps, which are identical for Tiers 2, 2b, and 3. Note that after PII review and implementation of restrictions, you might need to revisit some arrangement decisions and other work completed earlier in the process. Record Tier 3 actions and observations in a .txt readme file, digital processing plan, or media log spreadsheet (recommended for large, complex collections). 

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

## Implementing Restrictions

[To be added.]

---

## Examples
Alice Walker papers
Rita Ann Higgins papers
Southern Christian Leadership Conference records
Eamon Grennan papers
Tracy K. Smith papers
