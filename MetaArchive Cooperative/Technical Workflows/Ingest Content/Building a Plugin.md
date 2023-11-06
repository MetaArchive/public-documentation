Ingest Content — Building a Plugin
==================================


* 1 [Creating, Testing, & Implementing a Plugin](#BuildingaPlugin-trueCreating,Testing,&ImplementingaPlugin)
	+ 1.1 [Create the plugin, collection, and AUs](#BuildingaPlugin-Createtheplugin,collection,andAUs)
	+ 1.2 [Test the plugin and AUs](#BuildingaPlugin-TestthepluginandAUs)
	+ 1.3 [Implement the plugin in the production network](#BuildingaPlugin-Implementthepluginintheproductionnetwork)
* 2 [External Links](#BuildingaPlugin-ExternalLinks)


Creating, Testing, & Implementing a Plugin
=============================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

1. Create the plugin, collection, and AUs
--------------------------------------


	1. Upload plugin XML or generate a plugin in Conspectus.
	2. Configure a collection that uses the plugin. (If performed by central staff, be sure to consult with the member on collection properties, especially the name–avoid changing collection names.)
		1. Do not include a trailing slash in the Base URL
		2. Use the same plugin prefix as listed on the [Content Provider list](https://conspectus.metaarchive.org/content_providers)
	3. Create AUs in the collection. (The members should complete this step.)
2. Test the plugin and AUs
-----------------------


	1. Upload the plugin XML to the admin server (`/home/metaarchive/admin/lockss-plugin-xml/test`) and run the update script (`/home/metaarchive/admin/lockss_test/plugins/update`) to sign and compile the XML into a JAR file. The plugin XML compiled must exactly match the plugin XML in Conspectus.
		1. Run `ls -ls | head -10` in the plugin directory to verify that the first file is the new plugin JAR and that the file name matches the plugin name in the XML.
		2. Run the verify script to validate the plugin. (This may take a while as it checks every plugin.)
	2. Update AU status to Test. The test network title database is automatically generated every fifteen minutes starting on the hour.
	3. Log into a test cache.
	4. Force a recrawl of the MetaArchive plugin repository AU on the test cache to be sure LOCKSS will see the new plugin.
	5. Force an update on the title database on the test cache by going to the Debug Panel and clicking "Reload Config".
	6. Add the test AU(s) to the test cache and monitor crawling for issues.
3. Implement the plugin in the production network
----------------------------------------------


	1. Copy the plugin XML from `/home/metaarchive/admin/lockss-plugin-xml/test` to `/home/metaarchive/admin/lockss-plugin-xml/production` (using the appropriate subdirectories).
	2. Run the update script (`/home/metaarchive/admin/lockss/plugins/update`) to sign and compile the XML into a JAR file. The plugin XML compiled must exactly match the plugin XML in Conspectus.
		1. ```
		Run ls -ls | head -10 (or ls -ltr)in the plugin directory to verify that the first file is the new plugin JAR and that the file name matches the plugin name in the XML.
		```
		2. Run the verify script to validate the plugin. (This may take a while as it checks every plugin.)
	3. Update the AU status to Preserved.
	4. Manually update the production title database by running the update script (`/home/metaarchive/admin/lockss/config/update`).
	5. At this point, the AU(s) should be available and the call for ingest message can be sent.

Any changes to plugin XML on the admin server should include an increment to the plugin version number.

External Links
==============

* [ADPNet Wiki: LOCKSS Plugin](https://adpn.org/wiki/LOCKSS_Plugin)
* [ADPNet Annotation: Example Plugin formatting (PDF)](https://adpn.org/docs/pdf/ADPNAnnotation.pdf)
* [ma\_plugins](https://docs.google.com/document/d/1WhJVdCs7jbvycEMuELvanMnHQOmn7stXxhIijrXnlK4/edit)
* [2008-10: MetaArchive Plugin Lifecycle](https://docs.google.com/document/d/14-_YSh79ahuaZ1s0Ma5Q8IdKRrLHmYfu/edit)
