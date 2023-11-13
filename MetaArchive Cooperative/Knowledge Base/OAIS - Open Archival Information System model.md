OAIS - Open Archival Information System model
=============================================

MetaArchive's use of  [LOCKSS](/public-documentation/MetaArchive Cooperative/Knowledge Base/LOCKSS) can help member institutions enact [**The Reference Model for an Open Archival Information System (OAIS)**](http://www.oais.info/).

**MetaArchive and Submission Information Package (SIP)**

A MetaArchive Submission Information Package (SIP) consists of an HTML Manifest Page; an XML structured file known as a  [Plugin](/public-documentation/MetaArchive Cooperative/Knowledge Base/Plugin) that conforms to the organization of content into [Archival Units](/public-documentation/MetaArchive Cooperative/Knowledge Base/Archival Units (AUs)) on a web server; the individual content objects within each Archival Unit, and metadata supplied through the  [Conspectus](/public-documentation/MetaArchive Cooperative/Knowledge Base/Conspectus) database.

The Plugin and its parameters are given a unique name and are stored in a versioning repository. The name of the Plugin is then entered into the Conspectus database along with the base\_URL of the collection that has been prepared for harvest. The base\_URL, the Plugin name, and the collection’s Archival Unit parameters form a unique set of [Archival Unit IDs (AUIDs)](/public-documentation/MetaArchive Cooperative/Knowledge Base/AUID - Archival Unit ID).

These AUIDs are identified at the collection level in a separate XML file that constitutes a LOCKSS-specific [Title Database](/public-documentation/MetaArchive Cooperative/Knowledge Base/titledb - Title Database). The Title Database entry for a collection is finalized upon completion of the collection’s Conspectus database entry, which also serves to tie the Description Information directly to the collection for which it was created.

The base\_URL and the Plugin are then made available via the Title Database so that a designated MetaArchive-LOCKSS cache can retrieve the Plugin XML, point a browser at the collection on the web server, and make use of the parameters to crawl and harvest all of the content.

**MetaArchive and Archival Information Package (AIP)**

Once harvested, the LOCKSS software records the instances of, and communicates the outcomes of the initial ingest and polling/auditing process (including status of the AUs, and any errors concerning fixity) via a status log in the LOCKSS software and through the software’s user interface. This information coupled with the AUID (Archival Unit ID) information that comprises the SIPs represent the Preservation Description Information.

Throughout this ingest transfer process into the cache storage environment, the LOCKSS software maintains the file structure of the web server upon which content was originally organized for harvesting purposes. This harvested content is then registered in a  [POSIX](https://en.wikipedia.org/wiki/POSIX) or  [WARC](https://www.loc.gov/preservation/digital/formats/fdd/fdd000236.shtml) specification on the cache’s own file storage directory. The original Package Information is thus maintained during the transfer and throughout subsequent repair and refreshment of content.

In addition, if content is modified on a web server, the scheduled re-crawls of content will acknowledge the change and archive a new version of the individual content that was modified. 

**MetaArchive and Dissemination Information Package (DIP)**

Because the formation of an AIP preserves content in a POSIX or WARC format specification, the relationship of a file, a group of files, or the collection as a whole can be reconstituted in the same relationship to the organization of files as existing on the Content Contributor’s web server prior to content loss. This content undergoes no special transformations prior to being restored to a Content Contributor’s desired recovery location.

A Dissemination Information Package can then be fully reconstituted through reference to any previously compiled documentation about the collection's original repository structure, and through a retrieval of the Description Information supplied to the Conspectus, as well as the XML plugin and any of its special parameters. 

 (adapted from the MetaArchive wiki <https://wiki.metaarchive.org/metawiki/index.php/MetaArchive_OAIS_Definitions>)

