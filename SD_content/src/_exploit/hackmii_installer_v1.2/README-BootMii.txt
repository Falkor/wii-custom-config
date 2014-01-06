BootMii 1.5
Copyright 2007-2012, Team Twiizers
All rights reserved; do not redistribute


       Release Notes:


This software has received only limited testing.  We consider it to be stable
(and safe), but it still contains bugs and has only been tested on a handful
of Wiis.  It does not contain many features that will be useful or interesting
to most Wii owners, so we recommend that only expert users or developers
install it.  If you encounter any bugs, please provide feedback so we may fix
them in the next release.


       Runtime files


When installing BootMii, the HackMii Installer will create several files on
your SD card:

/bootmii
/bootmii/armboot.bin - Starlet-resident code (MINI) -- this loads ppcboot.elf
/bootmii/ppcboot.elf - BootMii shell - this is the GUI that is displayed
                       when BootMii runs.
/bootmii/bootmii.ini - BootMii shell configuration file.  See below


       Installation notes


You have two options to install BootMii.  Each carries its pros and cons, and
not all options are available for all Wiis.  Specifically:

* BootMii/boot2:  This mode will install BootMii into 2 blank blocks in the
                  boot2 area of your Wii.  It will take over the function of
                  the normal boot2.  If no SD card is detected or armboot.bin
                  is not found on the SD card, the drive slot LED will flash
                  briefly and the normal system menu will boot.

           Pros:  Independant of system menu and the rest of NAND flash.  Can
                  boot even if the rest of the system is completely corrupted.
                  Allows for safe backup / restore of NAND flash from SD card.
                  Allows direct boot of The Homebrew Channel, or other
                  programs.

           Cons:  Relies on a vulnerability in boot1 that was fixed mid-2008;
                  if your Wii is newer than this, the HackMii Installer will
                  not allow you to install this form of BootMii.  Installation
                  is complicated and slightly risky; we have tested it and
                  believe it to be safe, but a power failure at the wrong time
                  during installation could leave your system unusable.

* BootMii/IOS:   This mode will install BootMii into your NAND filesystem as an
                 IOS (IOS254).  It behaves identically to BootMii/boot2, but
                 you must launch it from a special program (The Homebrew
                 Channel, or your own code.)

           Pros:  Universal compatibility with all Wiis.  Allows booting
                  arbitrary code on ARM / PPC.  Supports speedy backup of NAND
                  to SD.  Very safe to install.

           Cons:  Easily deletable or overwritten by a system update.   NAND
                  restore is technically possible, but not safe because you
                  cannot boot to BootMii/IOS in case the contents of your NAND
                  flash are corrupted.


       NAND Backup/Restore


The NAND Backup option will create the file /nand.bin on your SD card. The NAND
Restore option will restore /nand.bin.  Both options take some shortcuts to
improve backup and restore speed.  Upon backup, if your card is not "properly
formatted", then you will be prompted for permission to reformat the card.  It
will be reformatted as FAT32 and given the volume "backupmii", and a nand.bin
file will be created in the root directory of the card.  We suggest that you
make a backup of your Wii's NAND Flash, label the SD card and store it in a
safe place in case you ever need to recover from it.


       Configuration file


BootMii will look for a configuration file at /bootmii/bootmii.ini.
It expects to see a file in the following form:

VIDEO=NTSC (or PAL50/PAL60/PROGRESSIVE)
AUTOBOOT=HBC (or SYSMENU)
BOOTDELAY=5 (or any other number)

More options may be added in the future.


       bootmii client / USBGecko support


A USBGecko-powered executable loader is available at http://gitweb.bootmii.org/
While BootMii is running, you can upload a new armboot.bin or ppcboot.elf file
without restarting your system.  BootMii will also output diagnostic messages
to the USBGecko as it boots.

You can invoke the client as "bootmii -a armboot.bin" to load code to the ARM
(e.g. a modified version of MINI), or "bootmii -p ppcboot.elf" to load code to
the PPC.  Please note that the ARM code will generally reload the PPC code from
SD, so if you want to load code to both processors, load the ARM code first,
followed by the PPC code.


       SD Menu


We have included a simple launcher for PPC ELF files on the SD card.  Please
note that any binary that gets loaded will be running under mini, not under
IOS.  libogc binaries will not run; we are investigating options for a future
release.


P.S. ios cat iz in ur wiiz watchin ur isoz

