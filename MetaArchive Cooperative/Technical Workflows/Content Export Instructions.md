# Content Export Instructions
{:.no_toc}

1. ordered toc
{:toc}

Overview
========

The following instructions are for MetaArchive Members who are conducting content checks as part of a [quality assurance strategy](/public-documentation/MetaArchive Cooperative/Technical Workflows/MetaArchive Quality Assurance Strategy) or who have experienced local loss of collections that are being preserved in the MetaArchive preservation network. Following these instructions and working with the MetaArchive Central Staff it will be possible to recover a preserved copy of collection content to replace all locally lost copies. It is recommended that Members read these instructions from top to bottom before proceeding with the first steps.

Content Export Instructions
---------------------------

### Step 1: Identify a Valid Preservation Copy

1. Go to the Conspectus and login: <http://conspectus.metaarchive.org/archives>
	1. Visit your Collections and identify the collection that you wish to export
		1. Click on “Preserved” status for each Archival Unit in the collection and verify:
			1. that the Last Poll occurred some time within the last 6 months; and
			2. that its Agreement is at 100%
	2. Select a member and a cache that is successfully preserving each of the Archival Units for the collection

### Step 2: Identify a Proper Download Destination

1. Now select a local workstation with network connectivity and note its unique public IP address
	1. Then choose a designated output directory on this workstation for downloading the collection
		1. Note: You may want to make the workstation a web server and the output directory the final destination for the restored files.

### Step 3: Exchange Connectivity Information

1. Contact the MetaArchive central staff Project Manager through [support@metaarchive.org](mailto:support@metaarchive.org) and:
	1. provide her/him with a brief description of your disaster recovery scenario
	2. provide her/him with the Collection name and/or desired Archival Units;
	3. provide her/him with the chosen member and cache; and
	4. provide her/him with the IP address of the workstation (she/he will make sure it is added to the Allow List in the Content Access Control of the chosen member’s LOCKSS UI)
		1. You will then be provided with a temporary login for the designated member’s LOCKSS UI and will be asked to confirm a general start date for triggering the export process.

### Step 4: Connect to a Recovery Cache

1. Login to a recovery cache using the provided information
2. Navigate to Content Access Options in the right-hand sidebar menu

### Step 5: Prepare an Export Package

1. Click on Export Content and:
	1. Select AU (currently must be done on a per AU basis)
	2. Choose ZIP from the Export file type dropdown (if earlier versions of files are desired, WARC or ARC will be more appropriate - see below)
	3. De-select the "Compressed" checkbox
	4. Select the "Exclude Directories" checkbox
	5. Choose how filenames should be translated for the destination platform
	6. Define a helpful filename prefix (e.g., export1)
	7. Choose the maximum file size batch per export request or leave blank for one full size package (total AU size will be distributed in batches observing the provided upper limit)
	8. If choosing ARC or WARC, choose the number of archived versions you would like to request (not available for ZIP)
2. Click “Create Export File(s)” (note below that several small interface bugs exist)
	1. May return a blank page. If so:
		1. Navigate back to Export Content page with your Browser Back button (you may still not see any download links)
		2. Navigate away from the Export Content page by clicking on one of the LOCKSS UI menu items and then return to Export Content and you should see one or more download links forming near the bottom of the page – you may have to do this several times to retrieve all the requested links (pay attention to time stamps to verify that the links have indeed stopped generating)
		3. DO NOT REFRESH BROWSER in order to update progress (this will clear the export process)
		4. May need to wait 30 minutes or more for a complete list of links to form

### Step 6: Retrieve Export Package

1. Click on each link to retrieve the prepared export package
2. Repeat for each desired AU
3. It may be helpful to have your System Administrator keep running system logs of the process to diagnose any network problems that may occur and to verify completion of the downloads.

### Step 7: Clean-Up

1. Once you have verified the successful download of each of the export packages, please click Delete Export Files and notify [support@metaarchive.org](mailto:support@metaarchive.org).

  
Retrieved from "<https://wiki.metaarchive.org/metawiki/index.php?title=Content_Export_Instructions&oldid=9086>"

* This page was last modified on 24 April 2015, at 14:10.
