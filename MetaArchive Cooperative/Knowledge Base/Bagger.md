[Bagger](https://github.com/LibraryOfCongress/bagger) is a software program maintained by the Library of Congress which serves as an integral piece of the ingestion of collection data into the MetaArchive preservation network. This program makes data packages called “Bags” of collection data. 

* Bagger creates packages of associated digital content that interacts well with the MetaArchive preservation infrastructure. The program also runs some basic data integrity functions such as generating checksums for digital files.
* All collection files as well as metadata files are included in a Bag.

Bag Profile
-----------

* To create a Bag, you must also create a Bag profile. This profile includes essential information about the institution and Bag. This data is written by the Bagger program into a text file and included in the final Bag with the original digital collection content.
	+ sample JSON file that can be customized for your institution: [bu-profile.json](https://confluence.educopia.org/download/attachments/80248839/bu-profile.json?version=1&modificationDate=1648481860082&api=v2)
	+ where it needs to be located:
		- For Windows - Windows (C:) > Users > [username] > bagger
		- For Mac -
	+ *Bag Profile Metadata Elements:*
		- Source Organization: Full official name of the member institution
		- Organization Address: Mailing address of the member institution
		- Contact Name: The primary liaison personnel at the member institution
		- Contact Phone: Phone number for Contact Name
		- Contact Email: Email address for Contact Name
		- External Description: A description of the collection which makes up the particular Bag
		- Bagging Date: The date the Bag was created
		- External Identifier: The file name of the Bag being created. This identifier must be constructed and recorded accurately and logically, as it will interface in a critical way with the MetaArchive Conspectus system.
	+ The file name of the Bag and the file it is contained in need to be configured in a logical way that allows for Bag ingestion to be easily tracked. Bag names should include the institutional acronym, name of the collection, and Bagging date.

More information
----------------

* Bagger [Releases](https://github.com/LibraryOfCongress/bagger/releases)
* Part I of the [InDiPres Technical Appendix](https://docs.google.com/document/d/1gGmkd-HNZo_ByfCnC6Y5Je2OUUDL5UFX/edit)
* [Bagger User Guide](https://docs.google.com/document/d/1MHvO13tW0fMCgzCFzHDFIIsr25mqYNOc/edit?usp=sharing&ouid=117497300378972443949&rtpof=true&sd=true) from Library of Congress
* [User Guide](https://archives.ncdcr.gov/media/800/open) on creating and validating bags with Bagger from the North Carolina Department of Natural and Cultural Resources and/or their [videos](https://www.youtube.com/watch?v=vK2aKQ64XCQ).

Advantages and Limitations
--------------------------

* Graphical user interface is easy to navigate and is great for folks not comfortable with command line.

  


* Some folks may run into a persistent Java Runtime error which prevents Bagger from launching.
	+ Solution: Go to Window's start button and type "Environment Variables." Select "Edit the system environment variables." Click the "Environment Variables" button. Under System Variables either add JAVA\_Home (if Java Development Kit is installed) or JRE\_HOME (if Java Runtime Environment is installed). Under Variable Value add the installation path. If the environment variable JAVA\_HOME or JRE\_HOME already exists, click edit and simply update the installation path so that it matches your version of Java.

MetaArchive members who are using and can answer questions
----------------------------------------------------------

  


