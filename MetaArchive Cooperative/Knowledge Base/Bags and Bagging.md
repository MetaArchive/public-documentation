Bags and Bagging
================


* 1 [Terms](#BagsandBagging-trueTerms)
* 2 [bag-info.txt](#BagsandBagging-bag-info.txt)
	+ 2.1 [Completing bag-info.txt with Bagger](#BagsandBagging-Completingbag-info.txtwithBagger)


Terms
===============================================================================================================================================================================================

**Bags** are based on the concept of "bag it and tag it," where a digital collection is packed into a directory (the bag) along with a machine-readable manifest file (the tag) that lists the contents. Bags have a sparse structure that envelopes any institutional data architecture and format. It can hold documents, pictures, music, movies and even other folders. Anything digital can fit into a bag.

A bag is like a folder or directory on a computer. It is essentially composed of three elements: 

1. A bag declaration text file, which is like a seal of authenticity;
2. a text-file manifest listing the files in the collection; and
3. a subdirectory – usually titled “data” – filled with the digital content.

The manifest is machine-readable for automated data ingest. The receiving computer analyzes the manifest and runs checksums on the contents; if the checksums match, the transfer is successful.

**Bagging** is the act of creating a bag, and several tools are available to automate the process.  MetaArchive does not mandate a particular tool for bagging content, but member institutions have used:

* [Bagger](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Bagger)
* [BagIt Python](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/BagIt-Python)
* [DART](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/DART)
* [Exactly](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Exactly)

This answers the AirTable Question: "[What bagging tools can be used? What are the pros and cons of each tool](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/recBUQp5T4LXrUqXa)?"  


bag-info.txt
============

A bag can also contain an optional text file, titled "**bag-info.txt**," that contains a small amount of administrative metadata, such as contact information for the collection owner and a brief description of the collection. Users can include much more metadata about the collection, but the Library recommends storing it in the "data" directory with the rest of the collection in order to keep the bag root directory uncluttered. Users can note in the "bag-info.txt" file that additional metadata exists and resides in the "data" directory. - Library of Congress [Digital Content Transfer Tools](https://www.digitalpreservation.gov/series/challenge/data-transfer-tools.html) site.

Most BagIt tools have ways of setting metadata values themselves (preventing you from needing to edit this file directly).

Below is a listing of bag metadata fields (required/recommended/optional) we would like you to use for your MetaArchive ingest, as well as some instructions on how to appropriately fill out their values. This information can also be found beginning on page 2 of the [MetaArchive BagIt Usage Instructions](https://confluence.educopia.org/download/attachments/93716500/MetaArchiveBagItUsageInstructions.pdf) (pdf).



<table class="wrapped confluenceTable">
 <tbody>
  <tr>
   <th>
    Field Name
   </th>
   <th>
    Priority
   </th>
   <th>
    Description
   </th>
   <th>
    Help
   </th>
   <th>
    <br/>
   </th>
  </tr>
  <tr>
   <td>
    Source-Organization
   </td>
   <td>
    Required
   </td>
   <td>
    The organization where the bag was made. (No abbreviations)
   </td>
   <td>
    Institution name
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Organization-Address
   </td>
   <td>
    Recommended
   </td>
   <td>
    The address of the Source-Organization.
   </td>
   <td>
    Insert proper mailing address here
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Contact-Name
   </td>
   <td>
    Required
   </td>
   <td>
    The name of the person responsible for the bag.
   </td>
   <td>
    Insert primary collection contact person
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Contact-Phone
   </td>
   <td>
    Required
   </td>
   <td>
    Phone number of the person from Contact-Name.
   </td>
   <td>
    Insert primary collection person’s contact phone
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Contact-Email
   </td>
   <td>
    Required
   </td>
   <td>
    Email address of the person in Contact-Name.
   </td>
   <td>
    Insert primary collection person’s contact email
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    External-Description
   </td>
   <td>
    Required
   </td>
   <td>
    A thorough description of the bag’s contents for those outside of your organization.
   </td>
   <td>
    Can be a truncated summary of Dublin Core collection descriptive metadata or a list of included collections if more than one collection is included in the “bag”
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Bagging-Date
   </td>
   <td>
    Required
   </td>
   <td>
    The date the bag was created on.
   </td>
   <td>
    Insert Bag creation date
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    External-Identifier
   </td>
   <td>
    Recommended
   </td>
   <td>
    A sender-supplied identifier for the bag.
   </td>
   <td>
    control number, unique identifier, or collection folder filename repurposed for naming this bag
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Bag-Size
   </td>
   <td>
    Required
   </td>
   <td>
    The size of the bag. This is usually set for you by the bagging tool.
   </td>
   <td>
    Set for you by the BagIt utility
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Payload-Oxum
   </td>
   <td>
    Required
   </td>
   <td>
    This is usually set for you by the bagging tool.
   </td>
   <td>
    Set for you by the BagIt utility
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Bag-Group-Identifier
   </td>
   <td>
    Optional
   </td>
   <td>
    A unique name given to the “bag group” if this bag is part of a bag group (more than 1 bag).
   </td>
   <td>
    This identifier must be unique across the sender's content, and if recognizable as belonging to a globally unique scheme, the receiver should make an effort to honor reference to it.
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Bag-Count
   </td>
   <td>
    Optional
   </td>
   <td>
    This bag’s sequence number, if part of a “bag group”.
   </td>
   <td>
    Ex: 1 of 2
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Internal-Sender-Identifier
   </td>
   <td>
    Optional
   </td>
   <td>
    The ID assigned to this content internally to your institution, if any.
   </td>
   <td>
    Insert local identifier for the bagged collection if applicable
   </td>
   <td>
    <br/>
   </td>
  </tr>
  <tr>
   <td>
    Internal-Sender-Description
   </td>
   <td>
    Optional
   </td>
   <td>
    A sender-local prose description of the contents of the bag.
   </td>
   <td>
    e.g., Dublin Core collection descriptive metadata
   </td>
   <td>
    <br/>
   </td>
  </tr>
 </tbody>
</table>


This answers the AirTable Question: "[What are some examples of the external and internal identifiers and descriptions that other MA members use when creating bag metadata?](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/recRIioNIaPchJ0zR)"

### Completing bag-info.txt with Bagger

A complete version of the recommended MetaArchive profile above is available from Educopia here (<https://docs.google.com/file/d/0B1gETO3iL-OsejhOZlRtV3c1OGM/edit?usp=sharing>). If you are using Bagger you can save this JSON file in the appropriate directory depending on your platform.

The steps for loading this profile with Bagger can be found on pages 4 & 5 of the [**MetaArchive BagIt Usage Instructions** (pdf)](https://confluence.educopia.org/download/attachments/93716500/MetaArchiveBagItUsageInstructions.pdf).

  


