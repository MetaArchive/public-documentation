# Archival Units (AUs)
{:.no_toc}

1. ordered toc
{:toc}

Archival units (AUs) are containers for files preserved in LOCKSS. Each AU has an [AUID](/public-documentation/MetaArchive Cooperative/Knowledge Base/AUID - Archival Unit ID), associated administrative metadata, and member URLs or files. Each LOCKSS cache stores AUs in opaque directories on the server filesystem, each AU is self-contained and self-describing. AU directories can be mapped to AUIDs. 

AUs are a meaningful aggregation of content (e.g., a discrete subset of a digital collection, a volume of a journal, etc.) and are closely related to the concept of an [object](/public-documentation/MetaArchive Cooperative/Knowledge Base/Object). At MetaArchive, AU's are organized into  [collections](/public-documentation/MetaArchive Cooperative/Knowledge Base/Collection) via Conspectus. Each AU must be ingested via a [plugin](/public-documentation/MetaArchive Cooperative/Knowledge Base/Plugin).

## AU Size

* AUs should typically be between 1GB - 100GB.
* AUs larger than 100GB can take days or weeks to propagate across the network.  However, it should be noted that there are not technical limitations to AUs larger than 100GB.

This answers the AirTable Question: "[Is there a recommended limit to the bag size? If so, what is it?](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/recOBiEALRczpNTEc)"

## Tarring / Zipping / Compressing AUs

Zipping or tarring (uncompressed) AUs makes recovery/movement a little easier technically, if there aren't thousands of files. But it's not the best thing for every scenario. If you're using temporary staging, it might make sense to zip/tar your AUs. If you're using permanent staging (e.g. a publicly crawlable site of journals) it doesn't make as much sense to zip/tar.

Many preservationists avoid compression, particularly lossy compression. It introduces risk by making files more fragile and susceptible to catastrophic damage in the event of a bit flip. Lossy compression results in permanent loss of the original data, i.e. it's non-reversible. However, use and implementation of lossless compression (which is reversible) can be a valid decision if it suits institutional needs and constraints, just be warned and have good documentation of your workflow choices.

If you are using Amazon Web Services (AWS) for staging, AUs need to be serialized.
