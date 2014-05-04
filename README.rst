Pageant with notifications
==========================

This version of pageant supports notifications when your agent is being used.
It shows a balloon in the system tray indicating which key has been used.

This can help you detect unapproved use of your keys, specially when used forwarded SSH agents.

Build on Linux
--------------

- Get Mingw.
- Edit windows/Makefile.cyg and remove all mentions of mno-cygwin

.. code::

	$ perl mkfiles.pl
	$ cd windows
	$ make VER="-DSNAPSHOT=$(date '+%Y-%m-%d') -DSVN_REV='$(svnversion)' -DMODIFIED" TOOLPATH=i686-w64-mingw32- -f Makefile.cyg pageant.exe

Resulting binary is pageant.exe.
