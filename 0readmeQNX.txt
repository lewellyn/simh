Notes on cross-compiling for QNX:
=================================

* Building an internal ROM is currently unsupported.
* By default, the makefile is configured for armv7-le and QNX 8.0.0 (BlackBerry 10).
  - To build this combination:
    $ make OSTYPE=QNX
* You can also define the CPUARCH and OSVER variables for other combinations.
  - To build for the PlayBook Tablet OS Simulator:
    $ make OSTYPE=QNX OSVER=6.5.0 CPUARCH=x86
* At this time, it only knows about armlev7 and assumes everything else is x86.
* The OS_LDFLAGS are currently only appropriate for Tablet OS/BlackBerry 10.
  - To compile on other variants of QNX, you will need to modify these, at least for now.
* At this time, there is no networking support. Networking support requires configuration
  of the host system and libpcap support. As the current build is BlackBerry 10/PlayBook
  only and they don't support libpcap (or any kernel level libs), network support is not
  possible.

======
=TODO=
======

* Update display so that it works on BlackBerry 10/PlayBook
* Make generic so it can work with both QNX (the OS) and BlackBerry 10/PlayBook's QNX
* Determine compiler versions automatically instead of relying on hardcoded versions
* Enable ROM builds

=========
=Authors=
=========

* Matt Lewandowsky <matt@greenviolet.net>
* Vincent Simonetti <rcmaniac25@hotmail.com>