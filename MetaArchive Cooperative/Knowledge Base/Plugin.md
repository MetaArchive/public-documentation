Plugin
======

In LOCKSS jargon, a **Plugin** is an XML structured file that conforms to the organization of content into [Archival Unit](https://confluence.educopia.org/display/MET/AUs+-+Archival+Units)s on a web server.  It instructs the LOCKSS software how to crawl, in terms of defining a starting [URL](http://en.wikipedia.org/wiki/URL), where to look for [Manifest Pages](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/HTML-Manifest-Page), and how to decide which URLs to ingest/copy from the content providing web site.

**Plugin Identifier** JAVA style identifier, eg org.lockss.ingest, that identifies a plugin uniquely in a LOCKSS network  [Term from MetaArchive Wiki]

**Plugin Name** short descriptive name for your plugin  [Term from MetaArchive Wiki]

**Plugin Repository** LOCKSS daemons are configured to read plugin definitions from web accessible plugin repositories. Plugins are deployed to plugin repositories as signed and jared files.  [Term from MetaArchive Wiki]

Learn how to create plugins at: [Building a Plugin](/public-documentation/MetaArchive-Cooperative/Technical-Workflows/Ingest-Content/Building-a-Plugin)

As of 2023-02, some older plugins are no longer working due to a Java update that makes the older plugins appear Unsigned. See: [Repackaging some plugins required for OpenJDK 8u362 or Oracle Java 8u351](https://github.com/lockss/community/wiki/Repackaging-some-plugins-required-for-OpenJDK-8u362-or-Oracle-Java-8u351)

**External Links**

* [ADPNet Wiki: LOCKSS Plugin](https://adpn.org/wiki/LOCKSS_Plugin)
* [ADPNet Annotation: Example Plugin formatting (PDF)](https://adpn.org/docs/pdf/ADPNAnnotation.pdf)
