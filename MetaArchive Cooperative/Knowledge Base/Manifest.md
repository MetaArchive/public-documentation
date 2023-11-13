Manifest
========


* 1 [Manifest Page](#Manifest-ManifestPage)
* 2 [Manifest File](#Manifest-ManifestFile)
* 3 [Generating Manifests & Checksums without Bagging](#Manifest-GeneratingManifests&ChecksumswithoutBagging)




### Manifest Page

A [Manifest Page](/public-documentation/MetaArchive Cooperative/Knowledge Base/HTML Manifest Page) is an HTML page that lists enough top-level web addresses for the LOCKSS harvesters to discover the entirety of content to be preserved for a given AU.  They are **required** when creating [AUs](/public-documentation/MetaArchive Cooperative/Knowledge Base/Archival Units (AUs)).

### Manifest File

A **manifest file** in computing is a file containing metadata for a group of accompanying files that are part of a set or coherent unit. For example, the files of a computer program may have a manifest describing the name, version number, license and the constituent files of the program.  The term is borrowed from a cargo shipping procedure, where a ship manifest would list the crew and/or cargo of a vessel. ([from Wikipedia](https://en.wikipedia.org/wiki/Manifest_file))

In MetaArchive & LOCKSS, manifest files are used to help describe the files gathered together in an [Archival Unit](/public-documentation/MetaArchive Cooperative/Knowledge Base/Archival Units (AUs)).

Manifest files are easily created using [bagging](/public-documentation/MetaArchive Cooperative/Knowledge Base/Bags and Bagging) software.

However, manifest files are ***not* required** for the LOCKSS software to work, but they help make it clear what is in an AU.

### Generating Manifests & Checksums without Bagging

* [Bash AVpres](https://avpres.net/Bash_AVpres/) - Developed by audiovisual archivist/preservationist Reto Kromer
