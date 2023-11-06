Using the BagIt find-bad-files.py Script
========================================

Using the BagIt find-bad-files.py Script
========================================

  
From <http://wiki.metaarchive.org>



<table class="confluenceTable">
 <tbody>
  <tr>
   <td>
    <h2 id="UsingtheBagItfindbadfiles.pyScript-Contents">
     Contents
    </h2>
    <ul>
     <li>
      <a href="https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&amp;printable=yes#Overview" rel="nofollow" style="text-decoration: underline;">
       <span>
        1
       </span>
       <span>
       </span>
       <span>
        Overview
       </span>
      </a>
     </li>
     <li>
      <a href="https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&amp;printable=yes#Find_Bad_Files_Script_Usage" rel="nofollow" style="text-decoration: underline;">
       <span>
        2
       </span>
       <span>
       </span>
       <span>
        Find Bad Files Script Usage
       </span>
      </a>
      <ul>
       <li>
        <a href="https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&amp;printable=yes#Overview_2" rel="nofollow" style="text-decoration: underline;">
         <span>
          2.1
         </span>
         <span>
         </span>
         <span>
          Overview
         </span>
        </a>
       </li>
       <li>
        <a href="https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&amp;printable=yes#Usage" rel="nofollow" style="text-decoration: underline;">
         <span>
          2.2
         </span>
         <span>
         </span>
         <span>
          Usage
         </span>
        </a>
       </li>
       <li>
        <a href="https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&amp;printable=yes#Rules_enforced" rel="nofollow" style="text-decoration: underline;">
         <span>
          2.3
         </span>
         <span>
         </span>
         <span>
          Rules enforced
         </span>
        </a>
       </li>
      </ul>
     </li>
    </ul>
   </td>
  </tr>
 </tbody>
</table>


Overview
========

Prior to creating a Bag of collection data it is important to isolate any hidden files, config files, .DS\_store, tilde-prefixed backups, and other likely-undesired files that often have their contents modified on endpoints during a transfer or ingest. Inclusion of these files and their checksums in a BagIt manifest file will result in a failed validation of the Bag at some future point. This is because each endpoint will modify such files for its own localized management purposes. When the contents change the checksums will change. The BagIt Library will flag these mismatches during a future export/recovery.

Of special significance, because LOCKSS makes use of http to retrieve Bagged collection files at a URL, any empty spaces in file names will be URL encoded and result in a file stored with inserted characters that were not present in the file name at the source URL. Upon an export of Bagged collections these encodings will be present and differ from what was recorded in the original BagIt manifest. In addition to isolating problematic system files the find-bad-files.py script alerts to file names that contain empty spaces so that these can be remedied with underscores in accordance with best practices for file naming conventions.

Making use of the find-bad-files.py script occurs during Phase 2, Step 2 in [Getting Started with BagIt for MetaArchive](https://wiki.metaarchive.org/metawiki/index.php/Getting_Started_with_BagIt_for_MetaArchive "Getting Started with BagIt for MetaArchive").

The find-bad-files.py script can be obtained from our MetaArchive GitHub repository here: <https://github.com/MetaArchive/metaarchive-qa-tools>. Usage is documented in the README, which is also provided below.

Find Bad Files Script Usage
===========================

### Overview

This tool will recursively scan a directory for filenames that violate a set of naming standards meant to prevent problems when ingesting collections into LOCKSS over HTTP. The relative paths will be printed to standard output; No files are moved or modified by this tool.

If -v or --verbose is provided, the reasons for the results being matched will be printed with the output.

### Usage


```
  find-bad-files.py [-h|--help] [-v|--verbose] <directory>

```
### Rules enforced

* Characters must be URL-safe. For our purposes, we strictly limit the characters present in filenames to letters, numbers, dots (.), hyphens (-), and underscores (\_).
* Filenames must start with a letter or number. This prevents inclusion of various hidden files, config files, .DS\_store, tilde-prefixed backups, and other likely-undesired files.
* Filenames must not equal "Thumbs.db".

  
[<< Back to Getting Started with BagIt for MetaArchive](https://wiki.metaarchive.org/metawiki/index.php/Getting_Started_with_BagIt_for_MetaArchive#Phase_2:_Obtaining_.26_Using_BagIt_Tools_for_MetaArchive "Getting Started with BagIt for MetaArchive")  
Retrieved from "<https://wiki.metaarchive.org/metawiki/index.php?title=Using_the_BagIt_find-bad-files.py_Script&oldid=7831>"

* This page was last modified on 11 October 2013, at 18:34.
