Format USB Drive in Unix Systems
=================================

Step 1
------
### Identifying the USB or SD Card Name
List out all the devices. - ***lsblk***

Securely Wipe Up the Data(Unrecoverable)
----------------------------------------
Before formatting the drive, you can securely wipe out all the data on it by overwriting the entire drive with random data. This ensures that the data cannot be recovered by any data recovery tool.

- Use the **dd** command line tool to wipe out all data securely.
- _sudo dd **if**=/dev/zero **of**=/dev/sda bs=4096 status=progress_
- Be very careful before running the ***of***,because it's the output device so don't mess up with your filesystem.
- Depending on the size of the drive, the process will take some time to complete.
- Once the disk is erased, the dd command will print “No space left on device”

Creating a Partition and Formatting
-----------------------------------
The most common file systems are __exFAT__ and __NTFS__ on Windows, __EXT4__ on Linux, and __FAT32__, which can be used on all operating systems.

Method 1 - __Fdisk__
----------------

1. To check the format and info of a Drive. - ***fdisk -l***
2. Run fdisk with the device name - ***fdisk*** */dev/sda*
3. Delete all the existing Partions(d).
4. Create New Partion (n)
5. Make the type Fat32 (t)
6. Write the changes(w)
7. Use */dev/sda1* rather than */dev/sda* because we created a new partion inside /dev/sda
8. Format the partition to FAT32 - ***sudo mkfs.vfat -F32 /dev/sda1*** or  ***sudo mkfs.vfat /dev/sda1***
9. Lable the Drive - ***sudo fatlabel /dev/sda1 "SONY 8GB"***


***Note***

- If you are partitioning a new drive, before starting to create partitions first, you need to create a partition table.
- Use MBR to boot the disk in legacy BIOS mode(2 TiB Max)
- Use GPT to boot the disk in UEFI mode(2 TiB > ).

Method 2 - __Parted__
---------------------
### Format with FAT32
Create the partion table

 - _sudo parted /dev/sdb --script -- mklabel msdos_
 
Create a Fat32 partition that takes the whole space

- _sudo parted /dev/sdb --script -- mkpart primary fat32 1MiB 100%_

Format the boot partition to FAT32

- _sudo mkfs.vfat -F32 /dev/sdb1 _

Once done, use the command below to print the partition table and verify that everything is set up correctly

- _sudo parted /dev/sdb --script print_

That’s all! You have formatted your device.

Format with EXT4
----------------
### Create a GPT partition table
- _sudo parted /dev/sdb --script -- mklabel gpt_
- _sudo parted /dev/sdb --script -- mkpart primary ext4 0% 100%_
- _sudo mkfs.ext4 -F /dev/sdb1_
- _sudo parted /dev/sdb --script print_

Conclusion
----------
Formatting a USB drive or SD card on Linux is a pretty straightforward process. All you need to do is insert the drive, create a partition table, and format it with FAT32 or your preferred file system


Extra Info
----------
### How to mount a drive with a directory.

- _sudo mkdir -p /mnt/audio /mnt/video_

> **Mount** the new partions.

> - _sudo mount /dev/sdb1 /mnt/audio_
> - _sudo mount /dev/sdb2 /mnt/video_
