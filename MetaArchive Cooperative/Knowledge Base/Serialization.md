Serialization
=============

In computer science, [serialization](https://en.wikipedia.org/wiki/Serialization) is when data is translated to a format that can be stored or transmitted, and reconstructed later.  

In MetaArchive, this often happens when [preparing content for ingest](/public-documentation/MetaArchive-Cooperative/Technical-Workflows/Prepare-Content-for-Ingest) .  Examples include:

1. [bagging](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Bags-and-Bagging) a group of files using tools like DART or Bagger, or
2. zipping a group of files using a [file archiver](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/File-archivers-and-zipping) like WinZip or 7-Zip.

Serialization can be useful when preparing content for ingest into the  [LOCKSS](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/LOCKSS) network, since a single  [checksum](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Checksum) for the group of bagged/zipped files can be created and checked, reducing the servers' work during [polling and voting](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Polling-and-Voting).

