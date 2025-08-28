RADXA ROCK 5C
==============
https://docs.radxa.com/en/rock5/rock5c/hardware-design/hardware-interface

Build:
======
  $ make rock5c_defconfig
  $ make

Files created in output directory
=================================

output/images
.
├── Image
├── rk3588_bl31_v1.40.elf
├── rk3588_ddr_lp4_2112MHz_lp5_2736MHz_v1.12.bin
├── rk3588-rock-5c.dtb
├── rootfs.ext2
├── rootfs.ext4
├── rootfs.tar
├── sdcard.img
├── u-boot.bin
└── u-boot-rockchip.bin

Creating bootable SD card:
==========================

Simply invoke (as root)

sudo dd if=output/images/sdcard.img of=/dev/sdX && sync

Where X is your SD card device.

Booting:
========

Serial console:
---------------
The Rock 5C has a 40-pin GPIO header. Its layout can be seen here:
https://docs.radxa.com/en/rock5/rock5c/hardware-design/hardware-interface#40-pin-gpio-header

The Uart pins are as follows:

pin 6:  gnd
pin 8:  tx
pin 10: rx

Baudrate for this board is 1500000.

Login:
------
Enter 'root' as login user, and the prompt is ready.

wiki link:
----------
https://forum.radxa.com/c/rock5
