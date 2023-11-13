Ingest
======

**Ingest(ing) content** is done using MetaArchive's  [Conspectus](/public-documentation/MetaArchive Cooperative/Knowledge Base/Conspectus) tool. 

* Content is packaged into [Archival Units (AUs)](/public-documentation/MetaArchive Cooperative/Knowledge Base/Archival Units (AUs)) and put on a [staging server](/public-documentation/MetaArchive Cooperative/Knowledge Base/Staging Server).
* A  [plugin](/public-documentation/MetaArchive Cooperative/Knowledge Base/Plugin) is written to point the LOCKSS network to the location of the content on the staging server.
* The [LOCKSS daemon](https://confluence.educopia.org/display/MET/LOCKSS#LOCKSS-LOCKSSDaemon) copies (ingests) content from the staging server via [the HTTP GET method](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET).
* LOCKSS daemons do not encrypt or compress copied content.
* AUs are copied across the network.

For more, see the technical workflow: [Ingest Content](/public-documentation/MetaArchive Cooperative/Technical Workflows/Ingest Content).

For other ingest methods, see [LOCKSS documentation Ingest Content](https://www.lockss.org/use-lockss/how-lockss-works#ingest-content).

