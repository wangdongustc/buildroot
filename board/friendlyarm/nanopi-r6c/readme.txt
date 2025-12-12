FriendlyARM NanoPi R6C
======================
https://wiki.friendlyelec.com/wiki/index.php/NanoPi_R6C

How to build
============

  $ make friendlyarm_nanopi_r6c_defconfig
  $ make

Note: you will need access to the internet to download the required
sources.

How to write the SD card
========================

Once the build process is finished you will have an image called "sdcard.img"
in the output/images/ directory.

Copy the bootable "sdcard.img" onto an SD card with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX bs=4M status=progress
  $ sudo sync

# WARNING: Replace /dev/sdX with your actual SD card device (e.g., /dev/sdb).
# Double-check the device path to avoid overwriting your system disk!

Insert the micro SD card in your Nanopi R6C and power it up.

The console is on the USB-C debug port (built-in USB to TTL serial port chip).
The serial port baudrate is 1500000, 8N1.
