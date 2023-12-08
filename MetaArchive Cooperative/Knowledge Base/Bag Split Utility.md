# Bag Split Utility

**NOTE: This tool is deprecated and no longer functioning.**

**The [BagIt-Python](https://github.com/LibraryOfCongress/bagit-python/) library deprecated a function that the Bag Split Utility used, so the utility is [no longer able to update bag manifests](https://github.com/LibraryOfCongress/bagit-python/issues/61).** 

**Additionally, the tool was originally designed to help split bags into 30GB chunks. Since network speed and storage are no longer as limited as they once were, the need for the tool is also deprecated. MetaArchive now accepts [AUs up to 300GB](/public-documentation/MetaArchive Cooperative/Technical Workflows/2 - Ingest Content-index.md).**

Please see below for historical documentation, and/or the code repo at **<https://github.com/MetaArchive/bagit-split>.**

**\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_**

MetaArchive's use of LOCKSS means that large collections need to be aggregated into smaller units for the purposes of optimal fixity checking across multiple replications in the preservation network. These smaller units are known as Archival Units (or AUs). The current upper limit size of AUs is 30GB.

When a MetaArchive member chooses to use BagIt for their collections prior to an ingest, the [Java BagIt Library](https://github.com/LibraryOfCongress/bagit-java) has an in-built mechanism for splitting a large Bag into smaller sub-Bag AUs conformant to our 30GB upper limit (bag splitbagbysize <BAG> --maxbagsize 30). To facilitate proper handling of AU formation the MetaArchive has developed a custom script that can work in conjunction with use of the Java BagIt Library. This script validates that a split did not result in any loss of files and produces a new metadata folder to retain the original Bag files in order to facilitate a reconstruction of the original Bag upon a future export/recovery from MetaArchive.

Making use of the Bag Split Utility occurs during Step 9 in [Getting Started with BagIt for MetaArchive](https://wiki.metaarchive.org/metawiki/index.php/Getting_Started_with_BagIt_for_MetaArchive "Getting Started with BagIt for MetaArchive").

The Bag Split Utility can be obtained from our MetaArchive GitHub repository here: <https://github.com/MetaArchive/bagit-split>. Usage is documented in the README, which is also provided below. The "unsplitting" function mentioned can be ignored during the process of preparing collections for a BagIt ingest into MetaArchive.

##Bag Split Utility Usage

### Overview

This tool provides functionality for splitting BagIt bags into a collection of smaller bags, and for "unsplitting" these bags back into a single bag mostly identical to the original. Usage

To see the full command-line help text, do:

```
  $ python bagit-split.py --help

```
### Splitting a Bag

```
  $ bag splitbagbysize <BAG> --maxbagsize 30

```

```
  $ python bag-split.py splitcheck <BAG>

```
The first command above uses the official BagIt command-line utility (bag) to split the original , in this example using 30GB as the per-bag limit. You can also use --maxbagsize values like .001 to indicate 1 MB (for example). You must be in the /bin directory of the BagIt utility to execute the command (if you use BitCurator, the BagIt Library (BIL) tool launches the terminal in the /bin directory). See the Library of Congress's [README file](https://github.com/LibraryOfCongress/bagit-java/blob/master/README.txt) and [an issue on GitHub](https://github.com/LibraryOfCongress/bagit-java/issues/9) for more information on building and running the utility.

The second command uses this tool to verify the split bags against the original bag for integrity and completeness, as well as to create an additional "metadata" bag among the split bags; the /data directory of the metadata bag will contain the original bag's manifests and bag-info.txt file.

### Unsplitting a Bag

```
  $ python bag-split.py unsplit <DIRECTORY CONTAINING BAGS>

```
This command creates a new directory called MERGED\_BAG by merging the bags found inside into a single reconstructed bag. The tool will check that the reconstructed bag is a faithful reconstruction of the original. If the input directory's name ended in "\_split" (this is added by the LoC tool when it splits a bag), the resulting directory will have the same name with "\_split" removed; if the input directory name did not end in "\_split", "\_merged" will be added to the name of the input directory.
