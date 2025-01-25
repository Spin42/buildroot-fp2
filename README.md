# Buildroot for Fairphone2 - NOT YET FULLY WORKING, UNDER HEAVY DEVELOPMENT

## Prerequisite

Make sure lk2nd is flashed on the boot partition.

1. Download latest lk2nd image here: [lk2nd-msm8974.img](https://github.com/msm8916-mainline/lk2nd/releases/download/20.0/lk2nd-msm8974.img)
2. Reboot your fp2 in fastboot mode.
3. Run `fastboot flash boot lk2nd-msm8974.img`
4. Reboot your phone.

## Build the buildroot system

1. Run `make fairphone2_defconfig`
2. Run `make all`
3. Reboot your fp2 in fastboot mode.
4. Run `fastboot flash userdata output/images/sdcard.img`
5. Reboot your phone
6. Plug a keyboard to your fp2
7. Login: root, password: root

## Standard buildroot README

Buildroot is a simple, efficient and easy-to-use tool to generate embedded
Linux systems through cross-compilation.

The documentation can be found in docs/manual. You can generate a text
document with 'make manual-text' and read output/docs/manual/manual.text.
Online documentation can be found at http://buildroot.org/docs.html

To build and use the buildroot stuff, do the following:

1) run 'make menuconfig'
2) select the target architecture and the packages you wish to compile
3) run 'make'
4) wait while it compiles
5) find the kernel, bootloader, root filesystem, etc. in output/images

You do not need to be root to build or run buildroot.  Have fun!

Buildroot comes with a basic configuration for a number of boards. Run
'make list-defconfigs' to view the list of provided configurations.

Please feed suggestions, bug reports, insults, and bribes back to the
buildroot mailing list: buildroot@buildroot.org
You can also find us on #buildroot on OFTC IRC.

If you would like to contribute patches, please read
https://buildroot.org/manual.html#submitting-patches
