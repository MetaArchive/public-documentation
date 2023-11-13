Conspectus
==========


* 1 [Conspectus Overview](#Conspectus-ConspectusOverview)
	+ 1.1 [Content Providers](#Conspectus-ContentProviders)
	+ 1.2 [Archives](#Conspectus-Archives)
	+ 1.3 [Collections](#Conspectus-Collections)
	+ 1.4 [Plugins](#Conspectus-Plugins)
	+ 1.5 [Archival Units](#Conspectus-ArchivalUnits)
	+ 1.6 [Archival Unit Status](#Conspectus-ArchivalUnitStatus)
		- 1.6.1 [Draft](#Conspectus-Draft)
		- 1.6.2 [Test](#Conspectus-Test)
		- 1.6.3 [Preserved](#Conspectus-Preserved)
		- 1.6.4 [Retest](#Conspectus-Retest)
		- 1.6.5 [Retired](#Conspectus-Retired)
	+ 1.7 [Site Up/Site Down](#Conspectus-SiteUp/SiteDown)
		- 1.7.1 [Site Up](#Conspectus-SiteUp)
		- 1.7.2 [Site Down](#Conspectus-SiteDown)


The Conspectus is the MetaArchive's collection management tool.  The Conspectus tool is accessible at **[http://conspectus.metaarchive.org](http://conspectus.metaarchive.org/)**.

* It maintains the metadata and preservation status information of preserved (or to be preserved) collections that are relevant to the library (or any partner institution), as well as LOCKSS-specific metadata (managing the [LOCKSS Title database "titledb"](/public-documentation/MetaArchive Cooperative/Knowledge Base/titledb - Title Database)).
* The Conspectus offers a Graphical User Interface so Members can create, update, and maintain their collections and their collection descriptions.
* The Conspectus generates LOCKSS-specific configuration data which is used by system scripts to configure the MetaArchive LOCKSS production and test networks.

The MetaArchive Cooperative already has many Conspectus entries. Please review some of the existing entries before making your own first entry.

Conspectus Overview
-------------------

This page provides an overview of how the Conspectus organizes its data. The Conspectus supports multiple Archives. Each Archive holds Collections, which contain Archival Units, that are created via a Plugin. Content Providers (MetaArchive Members) use the Conspectus to create Collections and assign them to various Archives.

All of the various Conspectus elements can be accessed via the sidebar menu.

### Content Providers

Each MetaArchive Member is considered a Content Provider and is listed in the Conspectus by emblem, acronym, name and Plugin prefix string. The number of Plugins and Collections is also listed for each Content Provider. Members who have left the Cooperative will be listed as (Retired). When a Member logs into the Conspectus they will see their Content Provider Details, which includes a list of all of their own Collections and Plugins, and a Retired status of 'True' or 'False'. If the Member is in good standing and has not left the Cooperative, that status will be 'False'.

A list of all Content Providers is available here: <http://conspectus.metaarchive.org/content_providers>.

### Archives

Collections are grouped together within Archives. Each Archive is identified by a title and each has a description. Archives are defined by the MetaArchive Content Committee and are used to designate collections of similar type (e.g., genre or subject) from across the entire MetaArchive membership. Archives do not functionally control or govern preservation operations in the network. You can think of Archives rather as a cataloging feature that helps to display collections with affinity in the Conspectus.

A list of all Archives is available here: <http://conspectus.metaarchive.org/archives>

### Collections

Collections are associated with various Archives.

As described above, a Member's Collections are listed on their Content Provider Details page. Clicking on any Collection in the list brings the Member to a Collection Details page. This page provides information about the Collection's Title, Archive, Plugin, Base URL, Description, and Repository Type.

All of the above information is provided to the Conspectus by clicking on the 'New Collection' link in the sidebar. The Member is presented with a form to supply the relevant entries for the information. Once created Members can edit certain Collection information by visiting the 'Edit Collection' button at the top of the Collection Details page.

Once a Plugin is added to a Collection, Archival Units can be defined from the Collection Details page. This is available via the 'Manage Archival Units' button at the bottom of the page (more on Archival Units below).

The Plugin XML can also be viewed on the Collection Details page by visiting the appropriate tab.

Metadata that has been supplied via the forthcoming 'Metadata Editor' (Late 2015) is also able to be viewed on the Collection Details page.

A Member can view all of their Collections by clicking on 'My Collections' in the left sidebar.

A list of all Collections defined in the Conspectus is available here: <http://conspectus.metaarchive.org/collections>.

### Plugins

The instructions to harvest Collections, or Archival Units of Collections, are contained in a Plugin. A Plugin defines the start URL of a web crawl and the crawl's filter rules in terms of parameter values, such as base\_url, volume\_name, year, etc. Each collection has only one Plugin but a Plugin can be re-used for multiple different collections. In other words, a Plugin's crawl rules can be helpful for harvesting different collections if they are organized and hosted the same way (e.g., in DSpace or Fedora, etc.).

Plugins are used to define Archival Units in Collections via the 'Manage AUs' action provided for individual Collections. If a plugin requires parameters beyond **base\_url** users are prompted to provide values. If a Plugin does not require any additional parameter values, 'Manage AUs' simply creates an Archival Unit without prompting for any values. Collections that use such Plugins will contain only a single Archival Unit.

Content Providers can upload a Plugin or create a new Plugin from a template under the 'New Plugin' link in the sidebar menu. Content Providers can view their created plugins by visiting the 'My Plugins' link in the sidebar menu.

All Plugins are associated with a Content Provider (e.g., a university) when they are created. The Conspectus requires that Plugin names begin with the plugin\_prefix of its Content Provider. For example, all Plugins from Auburn University have the Plugin prefix *edu.auburn*. All universities begin with "edu". All non-universities begin with "org".

Users can modify and re-upload Plugins as many times as needed so long as no Collection uses the given Plugin to define Archival Units. All Plugins know which Collections they support.

A list of all Plugins is available here: <http://conspectus.metaarchive.org/plugins>

### Archival Units

Collections that are comprised of more than one part are described in LOCKSS jargon as having multiple Archival Units. They are managed, that is created and deleted, in the context of their Collection. All of a Collection's Archival Units are defined with their Collection's Plugin - specifically the Collection's base\_url, and the parameters that define the units (e.g., year or folder name).

For each Archival Unit, the Conspectus prompts the user to enter values for all additional parameters beyond the base\_url parameter that the Collection's Plugin requires.

Archival Units for a Collection are managed by navigating to the Collection, choosing the Archival Units tab, and then choosing the 'Manage Archival Units' button at the bottom of the page.

### Archival Unit Status

The status of an Archival Unit (AU) indicates whether it is ready to be tested or preserved. Updating the the status of an AU results in changes to the LOCKSS title database.

#### Draft

* *What this means:* The AU is not yet ready to be tested. An AU always starts with a status of 'Draft.'
* *Permitted status changes by user group:* 
	+ Editor: 'Draft' to 'Test.' Can delete.
	+ Superuser: Same permissions as Editor.
* *Interaction with LOCKSS:*AUs with a 'Draft' status have no impact on LOCKSS and there are no changes made to either LOCKSS title database.

#### Test

* *What this means:* The AU is ready to be tested in the MetaArchive test network.
* *Permitted status changes by user group:*
	+ Editor: 'Test' to 'Draft.' Can delete.
	+ Superuser: Same permissions as Editor PLUS 'Test' to 'Preserved'
* *Interaction with LOCKSS:* When an AU's status is changed to 'Test' and Central Staff run the update script on the admin server, the AU definition is added to the LOCKSS title database for the test network.

#### Preserved

* *What this means:* The AU is ready to be preserved in the MetaArchive production network, ***or*** it is already preserved in the MetaArchive production network. In Conspectus, viewing the [preservation status records (PSRs)](/public-documentation/MetaArchive Cooperative/Knowledge Base/PSR - Preservation Status Record) will show how many copies are in the network, indicating whether it was recently set to "Preserved" or whether it has already replicated across the network and is fully preserved. This is generally the final state of an AU. 'Preserved' AUs cannot be deleted, and once an AU status has been changed to 'Preserved' it can never be deleted in Conspectus.
* *Permitted status changes by user group:* 
	+ Editor: None.
	+ Superuser: 'Preserved' to 'Retired.' 'Preserved' to 'Retest.'
* *Interaction with LOCKSS:* When an AU's status is changed to 'Preserved' and Central Staff run the update script on the admin server, the AU definition is added to the LOCKSS title database for the production network.

#### Retest

* *What this means:*The plugin for this AU has been modified and the AU should be retested in the test network. 'Retest' AUs cannot be deleted.
* *Permitted status changes by user group:*
	+ Editor: None.
	+ Superuser: 'Retest' to 'Preserved.' 'Retest' to 'Retired.'
* *Interaction with LOCKSS:* When an AU's status is changed to 'Retest' and Central Staff run the update script on the admin server, the AU definition is added to the LOCKSS title database for the test network.

#### Retired

* *What this means:*The AU will no longer be preserved in the MetaArchive production network. 'Retired' AUs cannot be deleted.
* *Permitted status changes by user group:*
	+ Editor: None.
	+ Superuser: None.
* *Interaction with LOCKSS:*When an AU's status is changed to 'Retired' it is removed from the LOCKSS title database for the production network. This does not, however, remove the AU from any of the caches in the network.

### Site Up/Site Down

Sometimes content becomes unavailable at the originating base\_url after Archival Unit content has been ingested in a LOCKSS network. In these cases the 'Up/Down' property of Archival Units should be set to 'Site Down'. This setting should only be used after an Archival Unit is fully preserved and can only be done by a superuser. If a member removes content from staging, they should first inform Central Staff so that they can change the property to 'Site Down.'

#### Site Up

* *What this means:*The AU is still crawlable at the same location. If any updates are made to the AU, LOCKSS will crawl the new content.
* *Interaction with* *LOCKSS:* LOCKSS will continue to try to crawl the content as long as it is marked as 'Site Up.' If an AU is marked as 'Site Up' and it is no longer in the same location, the Last Crawl Result will be a Fetch Error in the LOCKSS GUI every time it tries to recrawl the content.

#### Site Down

* *What this means:* The AU is no longer crawlable at the same location (often because it has been removed to free up storage space on the staging server).
* *Interaction with LOCKSS:* LOCKSS will no longer try to crawl the content. In the LOCKSS GUI, the Last Crawl Result will be 'No longer crawled.'  The following property will be added to the AU definition in the LOCKSS title database:



```
<property name="param.999">
  <property value="pub_down" name="key"/>
  <property value="true" name="value"/>
</property>
```

This answers the AirTable Question "[What does "Site Up" mean in Conspectus?](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/rec9s3rGvaXjOTccS)" and provides some context for the AirTable Question "[Do any of our members have active AUs that are being added to?](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/recA1xrOHQRyjHt5c)"  


This page provides an overview of how the Conspectus organizes its data. The Conspectus supports multiple Archives. Each Archive holds Collections, which contain Archival Units, that are created via a Plugin. Content Providers (MetaArchive Members) use the Conspectus to create Collections and assign them to various Archives.

All of the various Conspectus elements can be accessed via the sidebar menu.

You can read this page and then follow our [Conspectus How-To](https://wiki.metaarchive.org/metawiki/index.php/ConspectusHowTo "ConspectusHowTo") to get started using the Conspectus for your collections.

