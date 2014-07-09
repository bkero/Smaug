Smaug
=========
This is the original Smaug codebase that I've lovingly patched to get to compile on modern versions of Linux. Most of the things changed were related to the build system or some weird doesn't-work-anymore C code.

To fetch:

> $ git clone http://git.bke.ro/bkero/smaug.git

To compile:

> $ cd smaug/src

> $ make

To run:

>  $ ./startup

To connect:

> $ telnet localhost 4000

Getting started:
  - Shut down the MUD (Ctrl+C in the ./startup terminal)

> $ sed -i 's/Wizlock        1/Wizlock        0' ../system/sysdata.dat

> $ sed -i 's/Waitforauth    1/Waitforauth    0' ../system/sysdata.dat

> $ telnet localhost 4000 # Make character, look, save, quit

> $ pkill smaug

> $ sed -i 's/Level        2/Level       65' ../player/b/Bkero

  - Start the MUD up again (./startup)

> $ telnet localhost 4000 # Log in and have fun!

Relevant documentation available at:
  - doc/SMAUGDOC
  - doc/license.txt
  - doc/Object.help
