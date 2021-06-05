# Data Acquisition

Data Acquisition means is the process of taking an image from a suspect's machine.

Type of Data Acquisition:
* Static Acquisition = gathering non volatile data, forexample: gathring data from disk, usb , cd/dvd.
* Dynamic Acquisition = gathering volatile data , forexample: gathering data from memory.
important to note: imaging **isn't** copying
* imaging means take a mirroring the device's entire storage on a file.
* copying means take a mirroring only the **useful** data from the source device.

### Dead Acquisition  
Dead Acquisition refers to the attempt to acquire data from the suspect's machine without the operating system.
Reason:  the suspect's OS cannot be trusted.

### Storage Format
there are many many disk image formats:
* RAW : is the simplest format to save an image. 

**popular tools *DD* for linux and   *RAWWrite studio* for windows**
```
dd if=[src] of=[dst]
```
* EnCase Forensic Evidence File (EWF/EVF)
* ILook Investigator IDIF, IRBF and IEIF
* PyFlag Seekable GZIP (sgzip)
* Advanced Forensics Format (AFF)

beside a RAW format, there are proprietary format such as AFF for forensics image. AFF features:
* Compression.
* save disk space.
* integrity check.
* allow to investigator to add customary fields.
### Acquisition Methods
* **Disk-to-Image File(imaging):** Forensic investigators commonly use this data acquisition method. It is a flexible method, which allows creation of one or more copies, or bit-for-bit repkations of the suspect drive. ProDiscover, EnCase, FTK, The Sleuth Kit, X-Ways Forensics, ILook Investigator, etc. are the popular tools used to read the disk-to-image files.
 
* **Disk-to-Disk(cloning):** Sometimes it is not possible to create a bit-stream disk-to-image file due to software or hardware errors or incompatibilities. Investigators face such issues while trying to acquire data from older drives and create a bit-stream disk-to-disk copy of the original disk or drive. Tools like EnCase, SafeBack, and Norton Ghost can help create disk-to-disk bit-stream copy of the suspect drive. These tools can modify the target disk’s geometry (its head, cylinder, and track configuration) to match the data copied from original suspect drive.
* **Logical Data Acquisition:** this is the preferred method with large data storage such as RAID servers. This method captures only specific files or file types of interest to the case. It is used when time is limited.
* **Sparse Data Acquisition:** this method is similar to creating a logical acquisition but it also collects deleted data (unallocated). Also this method is used when an investigator doesn’t need to examine the whole drive.

investigator must consider the following when determine data Acquisition Methods:
1- The size of the source disk.
2- Can you retain the source disk as an evident or must you return it to the owner?
3- Time to do perform the acquisition.
4- Location of the evidence
anyway there is no one right method that works every time. different cases have different circumstance, and with different crcumstance, different methods are nedded.
### Live Data Acquisition
live data Acquisition means collect data while the machine is running. when investigator need for volatile data and volatile data reside in RAM or Cache.

 
