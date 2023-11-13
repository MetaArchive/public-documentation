Cache Manager
=============

**Cache Manager** is a web-based software tool developed by MetaArchive and LOCKSS to monitor the network.  It queries LOCKSS caches about their status and presents the information in a web based user interface. It incorporates command line report generators.  

Cache Manager is available at: **<http://monitor.metaarchive.org/>**

Background
----------

* Cache Manager is a Ruby application built by Monika Mevenkamp at Emory University/Educopia.
* The software lives in a private GitHub repository
* Some of the tool's functionality overlaps with [Conspectus](/public-documentation/MetaArchive Cooperative/Knowledge Base/Conspectus)

Status
------

* Cache Manager is one of the only places where you can find that replications have been made, because Conspectus isn't currently showing them.
* Cache Manager reports on all the AUs in the network; a lot of the functionality has degraded over time, but the information is still up-to-date.
* Cache Manager is still communicating with caches via the SOAP API.  It is aware of new ingests of AUs.  Not a source of truth, but helpful as a sanity check. Not doing all it was intended to do, but still helpful.
