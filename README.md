Skyhook Mark II
===============

A network bootable Linux live environment for preparing machines for installation.


Overview
--------
The Mark II image is a Debian based live system built and managed by the Debian live-build suite of tools.  This is the first image of the project to be managed using this method.

The image can be customized to suit your needs in accordance with the Debian live-build procedures.  Here is a quick overview of a few common tasks:

* **Packages:** The packages that will be installed in the image are defined in _config/package-lists/*.list_
* **Files:** Files can be inserted into the boot image by placing them into their full filesystem paths under _config/includes.chroot/_
* **Hooks:** Custom scripts can be run both during the image build and boot process by placing them in _config/hooks/_ as _*.chroot_ (build) or _*.binary_ (boot).  For example; _config/hooks/cleanup.chroot_ would execute while the image is being built on your machine, whereas _config/hooks/ping.binary_ would execute when the image is booted.



Prerequisites
-------------
* Tested on Ubuntu 12.10, but should build on any recent Ubuntu/Debian system
* `$ apt-get install debootstrap squashfs-tools live-build live-config build-essential`

Build Instructions
------------------
```
$ make
```

If successful, resultant images will be in _binary/live_ as **vmlinuz** (kernel), **initrd.img** (initramfs), and **filesystem.squashfs** (the root filesystem image).


Customization Shortcuts
-----------------------
* See _auto/config_ for adding custom and/or local package repositories.
* See the file _config/hooks/example.chroot_ for details on customizing the image.
* See the [package lists](config/package-lists/README.md)

See Also
--------
* Debian _live-build_ Manual: http://live.debian.net/manual/current/html/live-manual.en.html
