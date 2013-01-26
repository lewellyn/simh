Notes on cross-compiling for QNX:
=================================

* Building an internal ROM is currently unsupported.
* By default, the makefile is configured for armv7-le and QNX 8.0.0 (BlackBerry 10).
  - To build this combination:
    $ make OSTYPE=QNX DONT_USE_ROMS=1
* You can also define the CPUARCH and OSVER variables for other combinations.
  - To build for the PlayBook Tablet OS Simulator:
    $ make OSTYPE=QNX OSVER=6.5.0 CPUARCH=x86 DONT_USE_ROMS=1
* At this time, it only knows about armlev7 and assumes everything else is x86.
* The OS_LDFLAGS are currently only appropriate for Tablet OS/BlackBerry 10.
  - To compile on other variants of QNX, you will need to modify these, at least for now.

-- Matt Lewandowsky <matt@greenviolet.net>
