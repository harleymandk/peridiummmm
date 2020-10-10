Peridiummmm by SVatG - Source code
==================================

This directory contains the source code for SVatG's demo "Peridiummmm", for the
STM32F4DISCOVERY eval board. It is released into the public domain. You are free
to use it for anything, and we take no responsibility whatsoever for what happens.

Hardware
--------

The demo runs on the STM32F4DISCOVERY board by STMícroelectronics:

http://www.st.com/internet/evalboard/product/252419.jsp

It features a 168 MHz Cortex-M4F microcontroller with 192k of RAM and 1M flash memory.
It costs around $20, and is available from various electronics suppliers, such as
Farnell, Mouser or DigiKey. Probably plenty of other places too.

It needs a VGA adapter to display output. The board itself does not have any video
output, so a simple DAC constructed from resistors is used. A schematic is provided
in Documentation/Schematic.png. It is very simple to build.

Compiler
--------

The code was built with the devkitARM toolchain, release 36. Later versions may work,
earlier versions probably not, as you need Cortex-M4 support. Due to bugs in the
multilib implemenation in devkitARM, a custom gcc specs file, Terrible.specs, is used.

Source code
-----------

The following files should be sane, reusable, and helpful:

Accelerometer.c/h
Audio.c/h
BitBin.c/h, BitBinTables.h
GPIO.h
LED.h
RCC.h
Startup.c
System.c/h
VGA.c/h

The following subdirectories also contain code which is somewhat sane and useful,
but not crucial:

Graphics/
VectorLibrary/

Any OTHER files MAY CONTAIN DEMO CODING. We take NO RESPONSIBILITY WHATSOEVER for what
might happen to your COMPUTER or your SANITY if you attempt to USE or LOOK AT them!
YOU HAVE BEEN WARNED.

Building
--------

Building has been tested on Linux and Mac OS X, using the above-mentioned toolchain.
Building on Windows will probably require a few Unix utilities to be available, such
as make, rm, mkdir and a perhaps something else. This is untested, and you are on
your own for that.

To build, type "make". That should be it. If all goes well, a .bin file will be
produced.

Uploading
---------

The Makefile also contains an "upload" target to try and upload the file to the board
using OpenOCD. This requires a new enough version of OpenOCD to contain support for
the STM32F4DISCOVERY board, which probably means 0.6 and above, which at the time
of writing is still under development.

There are probably other methods you might use to upload the .bin file to the board.
None have been tested, but feel free to experiment.

Recommendations
---------------

Do try hacking the STM32F4! It is a very fun platform: Not much RAM, but plenty of
processing power. It can probably do a lot more than what we've done in this demo,
and it is cheap, simple and fairly easy to use and program. Let's make more demos for
it!



--- SVatG 2012 ----
