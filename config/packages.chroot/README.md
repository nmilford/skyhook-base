Custom Local Packages
=====================

To install a custom package, simply copy it to the _config/packages.chroot/_ directory. Packages that are inside this directory will be automatically installed into the live system during build - you do not need to specify them elsewhere.  Packages must be named in the prescribed way. One simple way to do this is to use `dpkg-name`. For example, `dpkg-name bar-foo.deb` will rename _bar-foo.deb_ to its full Debian package name of _ bar-foo_1.0-2_i386.deb_.  Details like version and architecture are automatically read from the package header by _dpkg-name_.

Using _packages.chroot_ for installation of custom packages has disadvantages:

* It is not possible to use secure APT.
* You must install all appropriate packages in the _config/packages.chroot/_ directory.
* It does not lend itself to storing Debian Live configurations in revision control.
* Seriously it's not an awesome idea to store binaries like packages in a VCS.  Consider this a hack at best, and opt for a local custom APT repository if you can.
