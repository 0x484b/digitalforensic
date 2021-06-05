# Data Acquisition

Data Acquisition means is the process of taking an image from a suspect's machine.

Type of Data Acquisition:
* Static Acquisition = gathering non volatile data, forexample: gathring data from disk, usb , cd/dvd.
* Dynamic Acquisition = gathering volatile data , forexample: gathering data from memory.

### Dead Acquisition  
Dead Acquisition refers to the attempt to acquire data from the suspect's machine without the operating system.
Reason:  the suspect's OS cannot be trusted.

### Storage Format
there are many many disk image formats:
* RAW : is the simplest format to save an image. 
** popular tools *DD* for linux and   *RAWWrite studio* for windows
$ dd if=[src] of=[dst]
* EnCase Forensic Evidence File (EWF/EVF)
* ILook Investigator IDIF, IRBF and IEIF
* PyFlag Seekable GZIP (sgzip)
* Advanced Forensics Format (AFF)
beside a RAW format, there are proprietary format such as AFF for forensics image. AFF features:
* Compression.
* save disk space.
* integrity check.
* allow to investigator to add customary fields.

