This is a port of MAME for the Wii. Unlike the previous SDL MAME for the Wii,
this is not based on Wii Linux. Please note that although many games work well
with the emulator, others may not work at all. See below for details.

DEFAULT CONTROLS:
Emulator Menu: WiiMote Home Button / GameCube L-Trigger
Insert Coin: WiiMote Minus Button / GameCube Z-Trigger
Start (not all games use this): WiiMote Plus Button / GameCube Start Button
Up/Down/Left/Right - WiiMote D-Pad / Classic Controller Left Stick /
  GameCube D-Pad / GameCube Joystick
Button 1/2/3/4 - WiiMote 1/2/B/A / Classic Controller A/B/X/Y /
  GameCube A/B/X/Y
Back (Exits current game) - WiiMote Plus + Minus Buttons /
  GameCube Z + Start Buttons

Controlls can always be changed from in the emulator options.

ISSUES:

* Lots of ROMs are supported, but not all of them. If you don't see the ROM in
  the list in the emulator, then support for that ROM isn't included. This is
  to keep the size of the emulator low enough to run effectively on the Wii. A
  list of all the ones that are can be found here:
  http://www.toadking.com/wiimame-0.4.txt

* Just because a ROM is supported does not mean it will run. Even games for
  early boards like CPS-1 can fail to run due to RAM limitations. If the
  emulator suddenly kicks you out to the Homebrew Channel, look in the MAME
  mame folder (sd:/mame/) for a file called errors.txt. If it says something
  about failing to allocate space, then odds are the ROM can't run on the Wii.
  The emulator might also crash outright and leave you with a code dump if RAM
  runs out.

* Because the Wii is not a strong console, some games will be slow. Frame-
  skipping is enabled by default to make games playable.

* The default controller mapping is unsuitable for lightgun games, but there is
  currently no way to make seperate mappings for lightgun and non-lightgun
  games. You can change the button mapping for lightgun games yourself in the
  emulator options.

* On older TVs, the edges of the screen can be cut off. To fix this, in mame.ini,
  look for the option "safearea" and set the value to something around 0.8 and
  0.95. It will vary depending on your TV.

CHANGELOG:

1.0
* Rewritten frontend code entirely, no longer uses SDL.
* Added better joystick support; Gamecube joystick works!

0.6.0
* Compiled with libogc 1.8.6, USB loading should be faster now if you have IOS58
* Changed video code around. Most games get a speedup or remain the same from
  this, but at least one (frogger) is slower for some reason.
* Widescreen support
* Fixed some games giving duplication errors and causing the emulator to exit

0.5.0
* Downgraded to MAME 0.134u4 due to issues with some ROMs not working
* SDL no longer used for video; FPS is increased
* WiiMote Sensor support more stable
* Fixed default font being too small; the custom font has been removed

0.4.0
* Upgraded MAME to 0.135
* Added WiiMote Sensor support
* Stereo support fixed
* Game list now shows up to 150 ROMs instead of just 15
* Changed USB/SD detection (Tries USB first, then falls back to SD)

0.3.1
* Upgraded libfat to 1.0.6, hopefully this fixes the SD card corruption bug
* Added USB support (Start SDL MAME Wii from a USB drive to enable it)
* Fixed "Unexpected option gl_lib queried" error log
* Fixed Nunchuck control mapping
* Switched Buttons 1 and 2 around (by public demand)
* Fixed support for some games (including Donkey Kong and Frogger)
* Moved errors.txt and ui.bdf files into /mame/

0.3
* First official release
