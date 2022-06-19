<h3>File Allocation Table (FAT)</h3>
	+ Indexes the location of bits
	<h4>Data Structures of FAT system</h4>
		+Clusters: Basic storage unit of the FAT File system
		+Directory: Contains info about file identification
		+File Allocation Table: Linked list of all the clusters
<p>exFAT: Default for SD cards >32GB.</p>
---
<h3>New Technology File System (NTFS)</h3>
	+ Created to address limitations that FAT had such as file and volume sizes
	+Features:
		-Journaling: Keeps a log of changes to the metadata in the volume. $LOGFILE in volumes root dir. NTFS is called a *journaling file system*
		-Access Controls: has access controls that define the owner of a file/directory and permissions for each user
		-Volume Shadow Copy: Keeps track of changes made to a file
		-Alternate Data Streams (ADS): Allows files to have multiple streams of data stored in a single file
	+Master File Table:
		-$MFT: First record in the volume
		-$LOGFILE: Stores the transactional logging of the file system
		-$UsnJrnl: Update Sequence Number Journal contains information about all the files that were changed in the file system and the reason for the change