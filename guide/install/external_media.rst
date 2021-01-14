
Installation on external media
==============================

Here we will install Sailfish x86 on an external bootable media, without writing to the internal disk of the computer. 

Prepare the installation media
------------------------------

Get your bootable media you will use to run Sailfish x86. Here we will install Sailfish x86 on the media. This should have at least 4GB capacity.

This media must be bootable by your target device. Most devices accept USB drives, and some accept SD cards. Check your BIOS for details. 

All data on the media you select will be destroyed. Needless to say, make sure you back it up.

Flash the image
---------------

Use a tool such as Gnome-Disks or Balena Etcher to flash the disk image. If it does not support .img.bz2, decompress it and flash the .img file.

The releases are here: https://github.com/sailfish-x86/rootfs/releases/

Make sure to verify checksums.

Once you boot from the external medium it should boot to the SFOS UI.

Note: Release 0.1 should not be used.
