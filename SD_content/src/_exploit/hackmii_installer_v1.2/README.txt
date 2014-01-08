HackMii Installer v1.2
Copyright 2007-2012, Team Twiizers
All rights reserved; do not redistribute

http://hackmii.com
http://bugs.hackmii.com
http://hbc.hackmii.com
http://bootmii.org
http://wiibrew.org


       SALES AND SCAMS

The HackMii Installer, The Homebrew Channel and BootMii are not licensed for
redistribution, sale, or bundling.  We reserve the right to request the removal
of any redistributed copies of this software. Any kind of sale, bundling,
or association with commercial activity is strictly forbidden.


       Contents of this release


In this archive, you will find the following files:

* README.txt                    This file
* README-HBC.txt                The Homebrew Channel README file
* README-BootMii.txt            BootMii README file
* boot.elf                      HackMii Installer binary
* bootmini.elf                  HackMii Installer binary, MINI version
* wiiload/                      USBGecko / TCP loader client
*       win32/wiiload.exe           Precompiled binary for Windows
*       lin32/wiiload               Precompiled binary for Linux (x86)
*       osx/wiiload                 Precompiled binary for Mac OS X (Universal)
*       wiiload.tgz                 Source code


       Installation instructions:

NOTE: The HackMii Installer will automatically install BootMii as IOS upon
startup. Starting with v0.7 it relies on it and there is no way to prevent
this step. If you don't want to have BootMii as IOS installed, you can
uninstall it after e.g. installing The Homebrew Channel. When doing so, the
HackMii Installer will automatically exit, because it can't (un)install
anything anymore without it.

If you have previously installed The Homebrew Channel, you can use it to launch
the HackMii Installer - use the boot.elf binary in this case.
This is the recommended way for all users.

If you have previously installed BootMii as boot2, you can also use the SD
browser of the BootMii shell to launch the MINI version - use the bootmini.elf
binary in this case.

If you don't yet have any means to launch homebrew applications, follow the
instructions at http://wiibrew.org/wiki/Homebrew_setup to get started.

Note about the MINI version of the HackMii Installer (bootmini.elf):
This version takes advantage of an in-place BootMii as boot2 infrastructure.
In this case, we already have full control over the hardware, which allows
the HackMii Installer to function properly without relying on any IOS flaws.
This means that you can install our software on any past, current or future
System Menu version.
Note that this will not and can not circumvent a potential deletion of BootMii
as IOS or The Homebrew Channel by future System Menu versions. As long as you
do not enter that future System Menu, you should always have a working Homebrew
Channel.


       Installation problems:


When possible, we have erred on the side of caution, so the HackMii Installer
may refuse to install on some Wiis if safety checks fail.  If this happens,
check our FAQs at http://bootmii.org/faq/ and http://hbc.hackmii.com/faq/
first.  If you think you encountered a bug, please add a new task to our bug
tracker at http://bugs.hackmii.com.  The HackMii Installer will create the
file install.log on your SD card.  Please attach this file to your report, it
will help us correct the problem.


       RISKS, CAUTIONS, and SYSTEM UPDATES:


Any persistent modification to your system (meaning, anything that does not go
away when you turn off your Wii) carries some inherent risk.  We have worked
hard to avoid this whereever possible, but we are unable to test all possible
configurations.

We do, however, believe that our software is safer to install than any other
that has been released, and once you have installed it we hope you will never
need to install another!

A special note about system updates:
The HackMii Installer relies on certain security flaws (fakesigned TMD and
ticket) that exist in older versions of the Wii's software.  The most recent
update as of this writing (dated 21 June 2010) corrected these flaws.  This
version of The HackMii Installer incorporates a workaround for this (by
exploiting a different flaw), and will work with any version up to - and
including - 4.3 of the Wii's software.  However, this new flaw may also be
fixed in the future. When it is, you may not be able to install our software.

The effects on users who have already installed our software depend on the
particular nature of the update.  Up until now, they have not been affected
and our software continued to work normally; however, this might change in the
future.  Excluding a deliberate attempt to cause harm to users, we believe
there is no danger to your system, even if you upgrade.

That having been said, we are releasing this software to you in the hope that
you will find it useful.  We can not and will not offer you any warranty on the
functionality of this software, or its impact on your Wii System.   We have
made our best effort to ensure its safety and to honestly explain the risks
involved, but the decision (and responsibility) is ultimately up to you.

We recommend that you check for news at http://wiibrew.org about compatibility
with new Nintendo System Updates before installing them; we will test each
update as soon as it is publicly available, and will announce whether any
issues have been discovered.

Note that the above information applies solely to the HackMii Installer and the
software it installs, and not to any applications launched from it. We cannot
be held responsible for any damage caused by these applications, nor do you get
bitching rights if something happens. As our software is delivered with no
warranty whatsoever, we also cannot be held responsible for any damage caused
by it.  However, in that case, you do get bitching rights.

