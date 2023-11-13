Collection
==========

**Collection** means the aggregated content to be preserved under the banner of one metadata record in the Conspectus database.

The scope and boundaries of collections are determined by the member. Typically, collections correspond to either an archival collection, bibliographic collection, or artificial collections around a particular subject.

LOCKSS 1.x does not include the concept of collections in its data model. In LOCKSS 1.x, all [archival units](/public-documentation/MetaArchive Cooperative/Knowledge Base/Archival Units (AUs)) ([object](/public-documentation/MetaArchive Cooperative/Knowledge Base/Object)) are organized by the plugin used to ingest them into the network. Plugins may or may not align with a collection.

LOCKSS 1.x data model:

* Plugin
	+ Archival Unit

LOCKSS 2.x does introduce the concept of collections, but how it aligns with MetaArchive's conceptualization is unclear.

MetaArchive has incorporated the concept of collections into our use of LOCKSS, but this level of administrative metadata exists only in Conspectus. Content managers create new collections in Conspectus and each collection uses a plugin. The same plugin can be used for multiple collections, so there is not necessarily a 1:1 ratio between plugins and collections. 

MetaArchive data model:

* Collection
	+ Plugin
		- Archival unit
