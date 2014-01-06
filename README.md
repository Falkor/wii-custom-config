-*- mode: markdown; mode: auto-fill; fill-column: 80 -*-
`toto.md`

Copyright (c) 2014 [Sebastien Varrette](mailto:<Sebastien.Varrette@uni.lu>) [www](http://varrette.gforge.uni.lu)

        Time-stamp: <Lun 2014-01-06 14:46 svarrette>

-------------------
# Wii Custom Softmod Configuration

This repository hosts personal notes on the soft-mod configuration of my Wii. 

You might want to take a look at the
[Glossary](http://wiibrew.org/wiki/Glossary) to better catch the terms used in
this file. 


> **DISCLAIMER:** 
> 
> I **do not** support piracy, it is **not illegal** to install the Homebrew Channel, 
> throught it will void your Wii's warranty, and Nintendo may refuse to do in and 
> out of warranty repairs on it, such as disc drive replacements.
>
> **In all cases, neither I nor the developpers of the used applications mentionned in 
> this file should not be held responsible in case the below instructions hurt / brick 
> you Wii.** 


Tutorial: 

* [Wiibrew tutorial](http://nintendo.about.com/gi/o.htm?zi=1/XJ&zTi=1&sdn=nintendo&cdn=gadgets&tm=19&f=20&su=p284.13.342.ip_p504.6.342.ip_&tt=29&bt=9&bts=9&zu=http%3A//wiibrew.org/wiki/WiiBrew%3AFAQ)

## Pre-requisites

Things you will need:

* A Wii console
* An SD Card (formatted in FAT16 or FAT32)
  * create a subdirectory `/private/`. If it has a `private` directory, rename it temporarily, e.g. to `privateold`. Having other saved channels on the same card will screw it up.
* An SD Card reader for your computer

[Introduction to Homebrew](http://nintendo.about.com/od/wiiliving/a/homebrew_overview.htm)

*Note* in the attached script, the SD card is supposed mounted on `/Volumes/WII_SD`

## Installing Homebrew

* [Reference](http://wiibrew.org/wiki/Homebrew_setup)
* [How to Install the Wii Homebrew Channel](http://nintendo.about.com/od/nintendowiibasics/ss/homebrew_setup.htm)

Installation with [bannerbomb](http://wiibrew.org/wiki/Bannerbomb), in particular [bannerbomb v2](http://bannerbomb.qoid.us/index.new.php)

You also need to add the [Hackmii Installer](http://bootmii.org/download/)

*Guide*

* Download [bannerbomb v2](http://bannerbomb.qoid.us/index.new.php)
  * extract the exploit (`abd6a_v200.zip`) at the root of the SD card 
* Download [Hackmii Installer](http://bootmii.org/download/) (version 1.2 on writing)
  * Copy `hackmii_installer_v1.2/boot.elf` on the root of the SD card
* Put your SD card in your Wii and turn it on. Go to the SD Card Menu on the main System Menu screen. 

  A message should appear asking to `load boot.dol/.elf`. If it freezes or does not appear, download the next .zip file from the Bannerbomb website and start over.
The homebrew on your SD card will load. Enjoy!
* (Optional) Fill out Comex's survey on the Bannerbomb website.

Now you can install the Homebrew Channel: 

* You will be presented with one of the screens below; if you have a new Wii you will only be able to install BootMii as IOS.
  
  [![install BootMii as IOS](http://wiibrew.org/w/images/thumb/c/c2/HackMiiInstallerScreen.jpg/135px-HackMiiInstallerScreen.jpg)](http://wiibrew.org/wiki/File:HackMiiInstallerScreen.jpg)

  * Select continue.
* Go to `Homebrew Channel > Install the Homebrew Channel`. You will be asked whether you want to install the channel; select yes. After installation you should get a message "finished" and return you to the initial menu.

`/!\` *If possible, install BootMii as boot2; if not install it as an IOS. [What is BootMii?](http://wiibrew.org/wiki/BootMii)*

After installing the Homebrew Channel by putting Bannerbomb and the Hackmii Installer on an SD Card, putting that in my Wii and following the instructions on the Bannerbomb site, I would up with a screen showing bubbles continually floating upward. Needless to say, I was confused.

Bannerbomb doesn’t explain this, but you also need to put applications on that SD Card in a folder called `/apps`. 
* First I downloaded the Homebrew Browser, which allows you to browse a list of homebrew games and software and download them directly to your Wii from the Internet. I had a lot of problems with HBB at first, but after I submitted a bug report I was told to try reformatting my SD disk, and after that it worked just fine, making installing new homebrew software as simple as choosing it from a list and clicking "download." (Without HBB you have to copy software from your PC to your SD card to install it.)

## Homebrew applications 

[List of apps (fr)](http://wiibrew.org/wiki/List_of_homebrew_applications/fr) -- [Full list](http://wiibrew.org/wiki/List_of_homebrew_applications/)

Create a `/apps` folder at the root of the SD card.

### Emulators

* [NES](http://wiibrew.org/wiki/FCE_Ultra_GX/fr)
* [Super NES](http://wiibrew.org/wiki/Snes9x_GX/fr)
* [Megadrive](http://wiibrew.org/wiki/Genesis_Plus/fr)
* [Neo Geo](http://wiibrew.org/wiki/GxGeo) -- [download](https://code.google.com/p/gxgeo/downloads/list)
* [MAME](http://wiibrew.org/wiki/SDL_MAME_Wii), Multiple Arcade Machine Emulator
  * [List of ROMs](http://www.freeroms.com/mame.htm) 
* [Nintendo 64](http://wiibrew.org/wiki/Wii64/fr) -- [emulateMii](http://emulatemii.com/) -- [download](https://code.google.com/p/mupen64gc/downloads/list)

You also probably want the [All-in-One loader](http://wiibrew.org/wiki/All-in-1_Emuloader) -- [site](https://code.google.com/p/gc-emuloader/).

You can find roms for these games on the following site: [freeroms](http://www.freeroms.com/)


### Utilities

* [Loadmii](https://sites.google.com/site/completesg/how-to-use/loadmii)
* [Homebrew Browser](http://wiibrew.org/wiki/Homebrew_Browser), to download the latest homebrew applications and games all through your Wii. 
  * [download](http://www.codemii.com/download/) -- [guide](http://www.codemii.com/homebrew/guide/)
  * Copy the `homebrew_browser/` folder to the `/apps` folder on your SD/USB device.
  * Ensure that the little write lock switch on your SD card is off.
* [WiiXplorer](http://wiibrew.org/wiki/WiiXplorer), a multi-device file explorer for the Wii
  * [official site](https://code.google.com/p/wiixplorer/)  

## Installing custom IOS (cIOS)

Custom IOSes such as [d2x](https://code.google.com/p/d2x-cios-installer/) augment the way the Wii accesses data. For instance, in order to access a hard drive instead of the disc, an IOS is needed to convert the function calls. d2x replaces the now obsolete [IOS249](http://gwht.wikidot.com/ios249). For more information about custom IOSes, see the [IOSes Explained page](http://gwht.wikidot.com/ioses-explained).

The prime reason you want to install [d2x](https://code.google.com/p/d2x-cios-installer/) is for the IOS reload blocking, required for USB loader (see below). 

* If your Wii is not connected to the Internet, you need to use [NUS Downloader](http://gwht.wikidot.com/nus-downloader)
  * [download link](http://wiibrew.org/wiki/NUS_Downloader)

### Pre-requisite

Start up NUS Downloader. 

* Make sure that "`Pack WAD`" is enabled.
* Using the `database`button, navigate to the following files and press start NUS Download for each one:
  * IOS -> IOS56 -> v5661
  * IOS -> IOS57 -> v5918
* Open the NUS Downloader directory (the folder where you placed NUS Downloader, you can use extras -> open NUSD directory to open it easily).
  The downloaded WAD files will be there: 
  * `NUSDownloader_v19\titles\0000000100000038\5661\IOS56-64-v5661.wad`
  * `NUSDownloader_v19\titles\0000000100000039\5918\IOS57-64-v5918.wad`
  
  Copy both WAD files to the root of the SD card.


### d2x install

* Download the [cIOS Installer](https://code.google.com/p/d2x-cios-installer/downloads/list) - v3.1 tested upon writing
  * Extract the zip file and copy the `d2x-cios-installer` folder in the `/apps` folder of the SD card
* Updating the installer with the newest version
  * Download the [latest version on the cIOSD2X Website](http://code.google.com/p/d2x-cios/downloads/list) -- 
  * rename it for extraction: 
  
        $> mv d2x-v10-beta53-alt-vWii.zip d2x-v10-beta53-alt-vWii.7z

  * Extract `d2x-v10-beta53-alt-vWii.zip` on your sd card into the folder `/apps/d2x-cios-installer`.
    *NOTE:* This will overwrite the file `/apps/d2x-cios-installer/ciosmaps.xml`
    possibly present in that folder. You might want to rename it before
    extracting the d2x package.

Now it's time to insert you SD card into the Wii.

* Start it up and go to the Homebrew Channel.
* locate the cIOS D2X Installer and run it.
* Wait for the app to load. Read the text on the welcome screen (if it interests you) and press __A__ to continue.
* Time to install the cIOSs.

  You are now on the main configuration screen. 
  A lot of options will be available here
  * Your cursor will be on the `cIOS D2X Version`. Use the D-Pad to change it to the newest version (all the way to the right) (v6 upon writing)
  * Move down, and change the `IOS Base` to __56__
  * Move down again, and change the `IOS slot` to your preferred slot - most people use slot __249__.
  * If you want, you can change the version under the fourth option, though this doesn't directly change the result.
  This version is only used by the Wii when checking updates. You can set the version to maximum (65535) if the Wii keeps asking for updates after you install it.
  
  You are now ready to install, so press __A__ to continue. 
  You will land on an overview with the available cIOS slots. The slot you just selected should be blinking. Several other slots may be highlighted in red. Select the blinking slot. 
  
  * Press __A__ to start the installation.
  
    Wait for the progress to complete. It may take a while, especially for the online installation.
Once it finishes, you will land on another IOS overview screen.
Your freshly installed cIOS should be highlighted in a green color.

  * Press the __A__ button to go back to the configuration screen.

  * Next, you want to configure the second cIOS. This time, use base __57__, and choose a different slot (__250__).
  * Again, press __A__ to install it and wait for the process to finish.
* Once everything is installed, press __B__ to exit the application.

That's it! You are now able to run any backup loader you want! Enjoy!

## USB loader 

USB loaders allow you to rip your own discs to an external USB hard drive and then run them from there. This will minimise load times, generally improve performance and means you can switch which Wii game you want to play without leaving your couch.

Several choices are possible: 

* [WiiFlow](https://sites.google.com/site/completesg/backup-launchers/usb/wiiflow) -- [download](https://code.google.com/p/wiiflow/downloads/list)

  ![](https://sites.google.com/site/completesg/_/rsrc/1365270781656/backup-launchers/usb/WiiFlow.png?height=100&width=140)

* [USB Loader GX](https://code.google.com/p/usbloader-gui/) - [Instructions](https://code.google.com/p/usbloader-gui/wiki/Installation)

  ![USB Loader GX](https://sites.google.com/site/completesg/_/rsrc/1365269973627/backup-launchers/usb/USBGX.png?height=100&width=140)

* [Configurable USB Loader](https://code.google.com/p/cfg-loader/)

  ![Configurable USB Loader](https://sites.google.com/site/completesg/_/rsrc/1365270262391/backup-launchers/usb/ConfigUSB.jpg?height=100&width=140)

The one that works for me is [WiiFlow](https://sites.google.com/site/completesg/backup-launchers/usb/wiiflow)




### Offline access to covers

For offline access to the covers, get the covers from <http://www.gametdb.com/Wii/Downloads>. 

**TODO**


## Preparing game backup on USB stick

… Or how to add ISO of **your** backup games on a USB stick. 

Resources: 

* [WiiAddict](http://www.wii-addict.fr/forum/lofiversion/index.php/t28067.html)

Download [WitGUI](http://desairem.altervista.org/witgui/wordpress/category/download/) and open it.

![WitGui](http://img707.imageshack.us/img707/4523/witgui1.png)

To transfer a game on a USB stick formatted in NTFS: 

1. click on Folder and select the source directory hosting the ISO of you rbackup game
2. click on Floder again and select the destination folder (the `wbfs` folder eventually created at the root of your USB stick)
3. drag and drop the game onto the second window to convert the ISO toward a `.wbfs` file.
4. on the configuration panel: 
   * "Save as": `+ <title> { <id> }` 
   * "Format" :  use **wbfs**
   * "Split   :  **Don't** (not required as you use the NTFS file system)  
![](http://img268.imageshack.us/img268/6492/witgui3b.png)
5. click on `Save`


## FAQ Apps

### AnyRegion Changer

AnyRegion Changer is an application which allows you to make non-temporary changes to various region and language settings on your Wii's SYSCONF and setting.txt files. You may call this a "Region Mod," i.e. the settings will persist. It also allows you to install the System Menu of another region if you so desire.

## FAQ Games 

### New Super Mario Bros

You can download the complementary [`Newer Super Mario Bros`](http://newerteam.com/), a full unofficial sequel to New Super Mario Bros. 

