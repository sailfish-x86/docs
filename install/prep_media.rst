Prepare the installation media
==============================

Get your bootable media you will use to run Sailfish x86. Here we will install Sailfish x86 on the media. This should have at least 4GB capacity.

This media must be bootable by your target device. Most devices accept USB drives, and some accept SD cards. Check your BIOS for details. 

All data on the media you select will be destroyed. Needless to say, make sure you back it up.

Partitioning (UEFI)
-------------------

Create two partitions:

- EFI partition, FAT32 filesystem, marked as an EFI partition, 300MB. Label "EFI"
- Root partition, Ext4 filesystem, rest of the disk. Label "sfos_root"

