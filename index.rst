.. Sailfish x86 documentation master file, created by
   sphinx-quickstart on Mon Dec 21 13:53:20 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Sailfish x86 Documentation
==========================

Welcome to the documentation of Sailfish x86. Sailfish x86 is a port of Jolla's Sailfish OS for x86_64 computers with
a standard UEFI BIOS, with kernels, modules, and firmware from Ubuntu 20.04. Therefore, many devices will be
supported. However, slight configuration changes may be needed for some devices. 

Sailfish x86 is maintained by Heng Ye, with help of the SailfishOS Porters community, on freenode and Telegram.
Special thanks go to TheKit and Elros34. The port is based on the Xiaomi Mi Pad 2 port, by Adam Pigg. 

It is possible to run Sailfish x86 on any standard x86_64 PC with a UEFI BIOS that supports the GRUB bootloader
and Ubuntu 20.04. However, it may need slight tweaks for the best experience.

.. toctree::
   :maxdepth: 1
   :caption: About
   :name: sec-about

   about/issue_tracking
   about/devices

.. toctree::
   :maxdepth: 1
   :caption: Installation
   :name: sec-install

   guide/install/prerequisites
   guide/install/external_media
   guide/install/setup
