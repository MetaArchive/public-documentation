
* 1
* 2 [Individual](#RecoverContent-Individual)
	+ 2.1 [Access to cache](#RecoverContent-Accesstocache)
	+ 2.2 [No access to cache (support request)](#RecoverContent-Noaccesstocache(supportrequest))
* 3 [Bulk (support request)](#RecoverContent-Bulk(supportrequest))
	+ 3.1 [Content Export & Restoration](#RecoverContent-ContentExport&Restoration)
		- 3.1.1 [Identify a Valid Preservation Copy](#RecoverContent-IdentifyaValidPreservationCopy)
		- 3.1.2 [Identify a Proper Download Destination](#RecoverContent-IdentifyaProperDownloadDestination)
		- 3.1.3 [Exchange Connectivity Information](#RecoverContent-ExchangeConnectivityInformation)
		- 3.1.4 [Prepare an Export Package](#RecoverContent-PrepareanExportPackage)
		- 3.1.5 [Retrieve Export Package](#RecoverContent-RetrieveExportPackage)
		- 3.1.6 [Clean-Up](#RecoverContent-Clean-Up)
=========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

Individual
==========

Access to cache
---------------

No access to cache (support request)
------------------------------------

Bulk (support request)
======================

**Content Export & Restoration**
--------------------------------

### **Identify a Valid Preservation Copy**

1. Navigate to the MetaArchive Conspectus site, <http://conspectus.metaarchive.org/archives>.
2. Locate your institutions sub-page and identify a specific AU Collection that requires restoration via data export.
3. Ensure that the AU selected had a Poll event occurred within 6 months, and that the agreement rate from this was at 100%.

### **Identify a Proper Download Destination**

1. Select a computer workstation with network connectivity and securely determine its unique IP address. For reasons of practicality this may be carried out via a staging server as necessary.

### **Exchange Connectivity Information**

1. Contact MetaArchive central staff at [support@metaarchive.org](mailto:support@metaarchive.org), provide the AU file string name and MetaArchive member identification.
2. Send the MetaArchive staff the IP address of the designated work station (or staging server) that will be used for data recovery.
3. Following this exchange of technical information the user wishing for AU recovery will be provided temporary login for the MetaArchive LOCKSS UI system and will be asked to begin a data export on the desired AU within a specified time window.

### **Prepare an Export Package**

1. Click on Export Content and:
	* Select AU (currently must be done on a per-AU basis)
	* Choose ZIP from the Export file type dropdown (if earlier versions of files are desired, WARC or ARC will be more appropriate - see below)
	* De-select the "Compressed" checkbox
	* Select the "Exclude Directories" checkbox
	* Choose how filenames should be translated for the destination platform
	* Define a helpful filename prefix (e.g., export1)
	* Choose the maximum file size batch per export request or leave blank for one full size package (total AU size will be distributed in batches observing the provided upper limit)
	* If choosing ARC or WARC, choose the number of archived versions you would like to request (not available for ZIP)
2. Click “Create Export File(s)” (note below that several small interface bugs exist)
	1. May return a blank page. If so:
		* Navigate back to Export Content page with your Browser Back button (you may still not see any download links)
		* Navigate away from the Export Content page by clicking on one of the LOCKSS UI menu items and then return to Export Content and you should see one or more download links forming near the bottom of the page – you may have to do this several times to retrieve all the requested links (pay attention to time stamps to verify that the links have indeed stopped generating)
		* DO NOT REFRESH BROWSER in order to update progress (this will clear the export process)
		* May need to wait 30 minutes or more for a complete list of links to form

### **Retrieve Export Package**

1. Click on each link to retrieve the prepared export package
2. Repeat for each desired AU
3. It may be helpful to have your System Administrator keep running system logs of the process to diagnose any network problems that may occur and to verify completion of the downloads.

### **Clean-Up**

1. Once you have verified the successful download of each of the export packages, please click Delete Export Files and notify [support@metaarchive.org](mailto:support@metaarchive.org).

For Further Clarification of the steps for collection Recovery visit that MetaArchive Content Export Instructions page; <https://wiki.metaarchive.org/metawiki/index.php/Content_Export_Instructions>, **<!-- RH: Won't this go away? Should we copy it to here?>** or contact MetaArchive directly via their website, <https://metaarchive.org/contact/>.

  


  


  


  


