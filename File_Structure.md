regardless of the operating system, every file has a specific structure to arrange its components, those components are file name, size, signature, contents, etc.
the file structure is universal and the same for any operating system.
### Metadata
metadata in general is defined as **Data describing other data**. file metadata is the data that describes the file itself and is used by the OS' application to make an opening, recognize,
and processing that the file easier.

metadata is found in different location, but as a starting point, the three location you need to start looking for metadata when analyzing a file are:
- MFT Record
- File Header
- Magic Number
### MFT Record
The NTFS file system contains a file called the master file table, or MFT. There is at least one entry in the MFT for every file on an NTFS file system volume, including the MFT itself. All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in MFT entries, or in space outside the MFT that is described by MFT entries. As files are added to an NTFS file system volume, more entries are added to the MFT and the MFT increases in size on the other hand each file has one or more MFT record.

MFT record can be used when searching for files whithin the file system. this record used for an evidence to prove the existence of lost or deleted files.
**directory snoop** is a great tool to perform the MFT record search and required task. another great tools **DiskExplorer for NTFS** from Runtime Software.
### File Header
File header is a unique identification section found at beginning/head of every file. header usually contains data used by the application that opens the file.
the header could contain things like: name, author, date of creation, size, etc.

different files have different headers and it is important to remember that some headers are known standard and others  are preparatory, also the some file don't have a header at all. foreample, txt file don't have header.

final note, most file formats have a header and a **trailer**. e.g. PDF files have a section called **XREF** in addition to the header and trailer. we can check header and trailer of files with hex editor.
### Magic Number
magic number is another method used by application (mostly unix/linux) to try and ID the file without the need for reading the whole header. a magic number is a unique string, usually at the beginning of the file, which can be used ti identify the type of the file.

in linux, the **File** command can be used to identify the type of the file.a list of magic number can also be found on most linux system in:
**/usr/share/file/magic**
### Metadata Type
metadata files which are relevant to forensic investigation and can be categorized into three nain type:
- System metadata
- Substantive metadata
- Embedded metadata and Externam metadata
#### System Metadata
