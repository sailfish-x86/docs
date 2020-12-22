
Installation on external media
==============================

Here we will install Sailfish x86 on an external bootable media, without writing to the internal disk of the computer. 

Prepare the installation media
------------------------------

Get your bootable media you will use to run Sailfish x86. Here we will install Sailfish x86 on the media. This should have at least 4GB capacity.

This media must be bootable by your target device. Most devices accept USB drives, and some accept SD cards. Check your BIOS for details. 

All data on the media you select will be destroyed. Needless to say, make sure you back it up.

Partitioning (UEFI)
-------------------

Create two partitions:

- EFI partition, FAT32 filesystem, marked as an EFI partition, 300MB. Label "EFI"
- Root partition, Ext4 filesystem, rest of the disk. Label "sfos_root"

Unpack the rootfs
-----------------

Mount the sfos_root partition. Obtain the rootfs tarball and extract it in the mountpoint. You should see the mountpoint populated with the standard Linux filesystem structure. 

Install the bootloader
----------------------

It is recommended to have the GRUB2 bootloader already installed to the internal storage of the device. However, if it is not, you can install GRUB2 to the USB drive. Make sure to use the ``--root-directory``, ``--boot-directory``, and ``--efi-directory`` options in ``grub-install`` to make sure you do not install to the wrong drive. 

Boot the system
---------------

Shut down your device completely and insert your bootable medium. Then boot up your device and select your bootable medium in the UEFI/BIOS boot menu. If GRUB is already installed to the internal storage, you do not have to do this. When you get to GRUB, if there is a menu, hit ``c`` to get to a prompt. Type ``ls`` to list the disks that GRUB has detected. List the contents of each to find the disk that corresponds to your bootable medium with Sailfish x86. For example, ``ls (hd0,msdos1)/``. After you have found it, type ``root=DISK_NAME``, for example, ``root=(hd0,msdos1)``. Then boot with the following commands; you can use Tab completion to make it easier to type the paths.

    linux /boot/vmlinuz{TAB} root=/dev/disk/by-label/sfos_root
    initrd /boot/initrd{TAB}
    boot

It should boot to the SailfishOS UI. 
