A **checksum** is a small-sized [block](https://en.wikipedia.org/wiki/Block_(data_storage) "Block (data storage)") of data derived from another block of [digital data](https://en.wikipedia.org/wiki/Digital_data "Digital data") for the purpose of [detecting errors](https://en.wikipedia.org/wiki/Error_detection "Error detection") that may have been introduced during its [transmission](https://en.wikipedia.org/wiki/Telecommunication "Telecommunication") or [storage](https://en.wikipedia.org/wiki/Computer_storage "Computer storage"). By themselves, checksums are often used to verify [data integrity](https://en.wikipedia.org/wiki/Data_integrity "Data integrity") but are not relied upon to verify [data authenticity](https://en.wikipedia.org/wiki/Data_authenticity "Data authenticity").[[1]](https://en.wikipedia.org/wiki/Checksum#cite_note-1) The [procedure](https://en.wikipedia.org/wiki/Algorithm "Algorithm") which generates this checksum is called a **checksum function** or **[checksum algorithm](https://en.wikipedia.org/wiki/Checksum_algorithm "Checksum algorithm")**. (Wikipedia, accessed 2022-12-09)

Checksums are generated to create a "digital fingerprint" that identifies a file or group of files.  If any part of that file(s) gets changed or corrupted, for example due to [data degradation](https://en.wikipedia.org/wiki/Data_degradation) (aka "bit rot"), then the checksum will also change.  Using computer scripts, we can compare checksums quickly in an automated way, helping to quickly identify files that have problems.  When combined with [polling and voting](/public-documentation/MetaArchive-Cooperative/Knowledge-Base/Polling-and-Voting), checksums ensure data integrity.

[MD5](https://www.digitizationguidelines.gov/term.php?term=md5checksum) used to be the go-to, then many practitioners switched to a [SHA](https://csrc.nist.gov/glossary/term/sha) (SHA1, SHA256, SHA512) after a paper talked about MD5's vulnerabilities. Some institutions use two checksums.

When selecting a checksum algorithm, think about your intention. SHA are cryptographic - more secure, but not always needed. MD5 is weaker over the long term (it can be spoofed), but more efficient in terms of energy consumption and time to create.

Checksums are easily created using [bagging](https://confluence.educopia.org/display/MET/Bags+and+Bagging) software.

However, checksums are **not** required for the LOCKSS software to work, but they will help confirm file fixity if you recover the AU in the future.

  


For more information about this topic, see the iPres paper at <https://phaidra.univie.ac.at/o:923643>.

This answers the AirTable Question: "[What manifest algorithms are recommended? What are the pros and cons of each option?](https://airtable.com/shrC6B0dj791XsSAa/tblEkzKRxJh7Cea7g/viwciniHrChrmIqDs/recpLv5gYnRuCOvCS)"

