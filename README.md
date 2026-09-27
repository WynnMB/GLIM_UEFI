# GLIM_UEFI

Create a GLIM multi-boot Linux USB drive using iOS/iPadOS.

This repository contains the files required to create a UEFI-bootable GLIM USB drive. The GLIM files are sourced from https://github.com/thias/glim, while the required GRUB2 files were obtained from Linux Mint.

This repository exists because the official GLIM project does not include the GRUB2 files needed for a standalone UEFI-only installation. Normally, these files are added automatically when running the GLIM installation script on Linux, where they are retrieved from the system's GRUB package.

Since the goal of this project is to create a UEFI-only GLIM USB drive with iOS/iPadOS, the required GRUB2 files have been bundled together with the GLIM files to allow the USB drive to be created without access to a Linux environment.

# Installation

Download the ZIP archive from the Releases page and extract its contents.

Copy the files and folders **inside** the extracted directory to the root directory of your USB drive.

**Do not copy the extracted folder itself** — only copy its contents directly to the USB drive's root directory.

# Drive Formatting

Use a FAT32 USB drive, unless copying ISOs above the 4GiB file size limit of FAT32.
If using ISOs above 4GiB, try exFAT. But remember that not all distributions support exFAT in their installer/live environment. 

# Adding or removing ISOs.

To add or remove an ISO file go to the **boot/iso** directory on the USB drive. The GLIM menu will automatically detect when you add or remove an ISO. So you don't need to manage the menu entries manually.
