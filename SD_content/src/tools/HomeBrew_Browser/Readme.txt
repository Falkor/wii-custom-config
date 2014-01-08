Homebrew Browser for Nintendo Wii
---------------------------------
The Homebrew Browser allows you to download the latest homebrew applications and 
games all through your Wii. You don't need to take your SD card out. You don't 
even need a computer! You can also delete homebrew you no longer want.

No more dead links, no more extracting files, no more finding out that the homebrew 
application doesn't include an icon.png and meta.xml in the zip file! 


Features:
------------------
- One click download/(un)install/update for each homebrew application
- Auto updating when your Homebrew Browser version is out of date 


Author:
------------------
teknecal (teknecal@gmail.com) - www.codemii.com
Graphics by DayDreamOz (www.spriteattack.com)


How to install:
------------------
Copy the homebrew_browser folder to the /apps folder on your SD/USB device. (Please create the /apps directory on the root of your SD/USB device if it doesn't exist)
Ensure that the little write lock switch on your SD/USB device card is off.
Launch HBB via the Homebrew Channel.

Please view the included HBB Guide and Help webpage to learn how to use HBB and solutions to common issues.


How to use:
------------------
Supports the Wiimote, nunchuck and Gamecube controller.

Green Tick - You have the latest version of that homebrew application installed.
Yellow Question Mark - You might not have the latest version of that homebrew application installed.

A Button = Click Button
B Button = Cancel Download or Extracting
Hold B button - Move the Wiimote up and down to scroll through the list quickly
D Pad Left/Right = Change category
D Pad Up/Down = Scroll up and down the list slowly
Minus/Plus Button = Delete/Remove/Add application to download/delete queue
Home Button = Menu
Hold Home Button down = Return to loader
1 Button = Work offline
2 Button = Revert to CodeMii repository


History:
------------------
7 October 2012 (v0.3.9e)
- Updated with latest libogc which should correct network issues some users are experiencing

17 September 2012 (v0.3.9d)
- Added support for new Wiimote 
- Added a longer timeout when requesting the homebrew list

25 February 2011 (v0.3.9c)
- Fixed connecting to the backup server
- Added setting to allow use of secondary server whenever you like

31 October 2010 (v0.3.9b)
- Added secondary CodeMii server
- Added a connection test so HBB doesn't look frozen if it can't connect to the server

21 October 2010 (v0.3.9a)
- Really fixed bug with HBB calculating the wrong free space
- Fixed bug when trying to use other repositories apart from CodeMii
- Added setting to enable/disable HBB from checking for updates

31 August 2010 (v0.3.9)
- Fixed bug with HBB calculating the wrong free space
- Fixed bug with USB running HBB when HBB wasn't installed on SD card
- Added support for HBC Themes (go to Settings -> Repo then select HBC Themes and restart HBB)
- Enabled a setting to use Wiimote like GC controller
- Enabled a setting to disable the character in the menu (if he freaks you out!)
- Updated the HBB updated applications window to allow more space
- Raised timeout for homebrew list
- Compiled with devkitPPC 21, libogc SVN and libfat SVN

21 February 2010 (v0.3.8)
- Speed improvement when parsing homebrew list
- Added .ogg music support
- Added ability to disable mounting USB devices
- Added timeout for Homebrew List download
- Fixed bug when updating apps or HBB the meta.xml file was corrupted
- Fixed bug when reverting to HBB repo it would sometimes fails
- Fixed bug when updating installed apps didn't work when installed apps are hidden

10 January 2010 (v0.3.7)
- Compiled with DevKitPPC r19, libogc 1.8.1 and libfat 1.0.6
- Allowed ratings and download count in repos
- Expanded the size of the HBB updated applications display when starting up
- Added homebrew sorter support (HBB will check for boot.dol.bak and boot.elf.bak files)
- Disabled write test as some cards failed it
- Fixed bug that crashed HBB at startup when settings had Use SD but no SD was inserted
- Fixed bug that would freeze or crash HBB when accessing a repo
- Fixed bug when GC controller was plugged in, it might go straight into the menu and then exit

29 September 2009 (v0.3.6)
- Fixed scrolling list issue
- Added ability to not delete folders and not extract files if they exist
- Added ability to select starting category and sorting method
- Re-added mp3 support (add loop.mp3 and it will play it instead of loop.mod)
- Improved scrolling of the list at start up

31 August 2009 (v0.3.5)
- Added repositories functionality
- Redid SD/USB mounting method so it keeps trying to at least mount one of these
- Cleaned up the text being printed a bit

9 August 2009 (v0.3.4)
- Fixed issue with icons not being loaded, removing an application from the queue bug and updated meta.xml handling when updating HBB

25 July 2009 (v0.3.3)
- Speed up extracting using updated libfat (speeds up download too, but it's not noticeable)
- Added USB support (plug in your USB device before booting HBB and turn off "Use SD" in settings)
- Added sorting of applications by name
- Added delete functionality to the queue (press minus to queue an application to be deleted)
- Added download and extract information (MB downloaded/MB total, Extracted files/Files to extract)
- Added a check to make sure Wii Network is initialised and active before downloading applications
- Fixed bug where you couldn't cancel the download queue if you had download prompt enabled
- Fixed bug where the meta.xml file name would change back to normal when you updated an application (this allows you to keep your custom name of applications)

2 June 2009 (v0.3.2)
- Added an updated applications pop-up which can be disabled in the setting. When applications are updated, you will be notified of the date, application and version when starting HBB.
- Added number of Wiimotes supported by applications by showing the number in the Wiimote icon
- Can revert to using IP address if HBB can't find codemii.com domain
- Added a download icon to indicate which application is being downloaded when you are browsing whilst downloading
- Added setting to disable Wiimote power off as some users experienced their Wii's turning off automatically
- Fixed bug where download/delete buttons would show when rating an application
- Fixed an issue when deleting applications wouldn't delete some folders
- Fixed squares that occasionally showed after name, description, etc which would cause creating/deleting directories to fail
- Fixed download queue issue when removing applications from the queue
- Fixed code dumps that occurred when scrolling the lists

1 May 2009 (v0.3.1)
- Able to download and browse at the same time (just click on a category when downloading)
- Fixed bug which didn't show the last character for applications names, descriptions, etc.
- Fixed bug where the wrong applications were shown after downloading from download queue
- Added GC controller support (port #1)
- Added nunchuck support for scrolling the apps list
- Added ability to power off the Wii via the Wiimote power button
- Menu items are now accessible when in the help or settings screen

12 April 2009 (v0.3)
- Brand new GUI (thanks DayDreamOz)
- Ability to scroll through applications without waiting to download images (images loading or being downloaded will show as "Image not found")
- Images download in the background
- Much more information on applications which includes a longer description, author, version, size, date, SDHC support and controllers supported
- Shows the total amount of downloads for each application
- Ability to rate applications and shows an average rating
- Ability to queue applications for download in a download queue and download all at once
- Ability to sort applications by date, rating and download count
- Added background music (off by default, change loop.mod with your own music if you like)
- Uses threads
- Ability to move the cursor once downloading or extracting
- Ability to cancel extracting process
- Ability to work offline (by pressing the 1 Button when HBB is initialising the network)
- Ability to hide installed applications from the lists
- Checks for SD card to make sure there is enough free space before downloading each application
- Settings now include show SD card space, check free space, hide installed applications, retreive my rating, background music, rumble, update icon and offline mode
- Added lots of help screens
- Added widescreen support (thanks Cashman)
- Checks that server connected to is really www.codemii.com
- Added check to make sure the SD card isn't locked
- Downloads all image files before loading HBB v0.3 the first time to make things faster

6 April 2009 (v0.2.5d)
- Uses domain www.codemii.com to connect instead of an IP address

17 March 2009 (v0.2.5c)
- Fixed issue with utilities section that was causing it to be empty
- Fixed zip progress issue

24 January 2009 (v0.2.5b)
- Keep retrying networking initialisation
- Now shows the progress when extracting the zip files (thanks Tantric)
- Detects the ftpii directory when using a password like ftpii_mypass
- Keep meta.xml name when updating if it has been edited
- Added more error checking when updating HBB, if updating fails it reverts back to the previous version
- Media category becoming unavailable should now be fixed
- Fixed controller screen to display accurate Dpad information

19 December 2008 (v0.2.5a)
- Fixed XML issue which caused a code dump.
- Added update text so it now tells you what's new before you update

13 December 2008 (v0.2.5)
- Changed blue tick to yellow tick so it can be seen easier
- Made help and controls window larger
- Free space is now shown at the bottom right of screen
- Added menu when pressing home, can go into settings, reboot the wii or return to loader. Hold the home button to return to loader at any time.
- Added settings which allow you to change when the image files are downloaded; either at startup or on-demand. Can enable or disable the free space text.
- Added update all applications feature. You access this when clicking on the SD card icon. Once you are shown your applications, the SD card icon changes to an update icon which you can click.

9 November 2008 (v0.2.4)
- Able to view currently installed applications
- Fixed bug in downloading and removing applications which affected uno and may have affected other applications
- Retries increased to 10 times with a longer pause in-between
- Able to reboot the Wii by holding B and pressing Home
- Detects if you have a .elf version of any application and lets you update that application
- Now uses zip files which means download sizes are reduced (thanks Tantric)
- Added SDHC support
- Detects if HBB icon or meta file exist, if they don't then it downloads them

26 October 2008 (v0.2.3b)
- Using dol instead of elf to work with HBC beta 9

30 September 2008 (v0.2.3a)
- Wlan adapter should now work with the HBB
- Applications should now be detected properly
- When applications are downloaded/deleted from the popular category they will now appear correctly in other categories and vice versa

29 September 2008 (v0.2.3)
- Rebuilt with latest libfat CVS to fix delete corruption bug (thanks joedj)
- Added Popular category
- Updated HBB about information

6 September 2008 (v0.2.2)
- Now downloads images in real time, no more having to wait for HBB to load
- Fixed IR cursor, no more IR cursor correction is required (thanks Wil)
- Deleting applications now deletes all files from the directories created (emulator roms/saves directories aren't deleted)
- Dpad left and right now controls the categories
- Updated HBB about image to include information about wii message notifications for HBB

3 August 2008 (v0.2.1b)
- Added the ability to cancel downloads at any time by pressing B
- Added a slight rumble when moving over any button
- Moved help and controls icon to left of banner

27 July 2008 (v0.2.1a)
- Fixed the issue when downloading most of the temporary images for the first time it caused HBB to exit
- Added text to describe what each icon does when you move the cursor over it

26 July 2008 (v0.2.1)
- Cursor now rotates and disappears when IR is not pointed to the IR sensor (thanks ebool)
- Added about and controls icon
- Added functionality to remove old files that some applications don't use when you update
- Added statistics gathering which will be displayed on a webpage
- Changed IP address from wiiregionworld.com to codemii.com

13 July 2008 (v0.2.0b)
- Increased buffer size so applications that require a lot of files will work
- Added HTTP no-cache so users behind a proxy will always retrieve the latest version of the apps list

10 July 2008 (v0.2.0a)
- Small bugfix, downloading Raytracer, Wiiwhiteboard, etc should now work

9 July 2008 (v0.2.0)
- Supports applications which load files from the SD card
- Added categorisation of homebrew applications
- Ability to install HBB via wiiload
- Updated tick icons
- Updated "Download" image to change to "Update" if you already have the application installed
- New icon displays even if you have an older version of the application
- Fixed issue when downloading 4 applications HBB would exit
- Does not download the icon.png file if you already have that application installed

4 July 2008 (v0.1.2)
- Added checks to make sure the server response is valid
- Uses new graphics made by LowLines
- New mouse pointer
- "New" icon appears depending on the time
- Uses GRRLIB 3.0.1a
- Fixed images getting corrupted when loaded previous and next 6 images a few times
- Now downloads the icon.png and meta.xml files for the HBB if you update

30 June 2008 (v0.1.1)
- Fixed issue with requesting files from server (thanks joedj)
- Enabled auto updating (press B when asked if you don't want to update)
- New logo and HBC icon

29 June 2008 (v0.1)
- Initial Release


Credits:
------------------
LowLines for the Homebrew Browser v0.2.x graphics including logo, HBC icon and all other graphics
joedj - ftpii source for network read and write
NoNameNo & Redshare - GRRLIB (3.0)
Tantric - Unzip library
All the Wii homebrew developers and icon artists
All the people who tested the HBB revisions
Team Twiizers, #wiidev & #wiihelp


Misc:
------------------
Want to be notified when applications are updated?
Add hbb@codemii.com to your Wii address book
For more information about HBB and developments visit: www.codemii.com

Visit the homebrew developers on IRC at irc.efnet.org at #wiidev
Need help with running homebrew on your Wii? Visit #wiihelp