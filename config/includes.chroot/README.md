CHROOT Includes
===============================================================================

a.k.a. "This Gets Copied Into Root (/) During The Image Build Process"
-------------------------------------------------------------------------------

Put files, directories, money, jewels, private keys, and other valuable things that you would like to end up in the image's root filesystem here.  The contents of this directory (including this README) will be copied into the chroot environment of your image as it is being built.


*Some Useful Things To Put In Here:*
* /etc/rc.local file for things to do on startup
* init.d/systemd/upstart/supervisord/god service startup scripts & configuration
* Cool binaries and games
* Gold.