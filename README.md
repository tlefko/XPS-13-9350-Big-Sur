# Site
- checkout our official site! https://twortech.wixsite.com/pcmac
# Version Info

This build is compatible up to Big Sur Beta
- Now Compatible with macOS 11
- Please leave feedback with issues or w/o
- Comitted to Updating up to OS 11
- MULTITOUCH TOUCHSCREEN SUPPORT

# Latest Release Notes
- Fixed Bluetooth and Wifi Stability Issues
- Improved Preformance and Power Managements
- Can Provide Files for Display Overrides
- Additional Patches for 3K Display
- updated for 15.4 rev 1
- if using unsupported wifi card disable it in bios
- use config.plist not HD520
- Perfect Sleep/Wake for 1080P Model no-touch, still bugs for 3K
- Exact same functionality as Catalina

# Notes
- Never tested USB C except for charging, works great
- USB devices eject on sleep (not really an issue)
- 4K model has minor sleep wake issues occasionally, 1080P is fully functional
- 4K sleep has been heavily improved however and glitches are rare, fixed by reopening lid

# POST

- run sudo pmset -a hibernatemode 0
- If on 3K disable sleep completely for maximum stability
- If no mouse, install all voodoo kexts using Kext Utility

# Description

- This esentially an ultra-simplistic version that is stable without the use of a deploy or complicated file installations and copies.
- You can easily view all the SSDT patches along with configuration files for the bootloader as they are all documented clearly in the files.
- This does include a copy of Clover, which of course I do not contribute to and am only responsible for the provided files, patches, and kext placements

This guide provides a working setup with little knowledge of the topic and without "optimization" (because often they can break things). But, it is fully functional and preforms properly and is stable
- Make sure you are using DW1560 for wifi or else KP. If not using remove BRCM kexts from CLOVER>kexts>other.

# BIOS Setup
-  Set all SATA operation as AHCI
- Disable Secure Boot, Fast Boot
- For Coil Whine improvement disable C-States
- Enable UEFI Booting

# INSTALL (VERY IMPORTANT)
- Due to structural changes in the setup of apple's Big sur, this EFI cannot boot the installer it can only boot into a system / device that has already been created and setup.
- To do this, you need to install Big Sur to a virtual machine (lots of guides online) and then create an dmg of that system, and restore it onto your HDD using the 'dd' command
- There are various guides online how to get this virtual machine setup complete.
- You can then use the attached EFI folder to boot and use macOS big Sur
- You can use this video to show you how to get your macOS pre-installed onto your hard drive https://www.youtube.com/watch?v=HMU3nhcbWHw
 
 # Boot Entry Setup
 - Boot into the BIOS of the computer, then navigate to the Boot setup (or entries (not sure what it is called exactly, but it will be a list of the options your computer selects to boot)
 - Click add new, and make sure the USB isn't plugged in.
 - Select the only option that is avaiable, and in FS0 navigate to Boot/BOOTx64. Add this as an entry, then select this as whatever priority you would like.
 
  # Messages and Facetime
 - Gnerate your own Serials, Board Numbers, MLB
 - There are various guides online to do this and as default they're set to essentially Null (Fakeserial)
 - This is fairly straightforward and there is lots of external recourses, or you can contact me for support.
 # Headphones and Audio
 - All audio from speakers should work perfectly along with Bluetooth and USB audio
 - To resolve headphones static issue (wired) install combojack 
 
 # Finished!
 - Congratulations, there really aren't any more steps that are required. Feel free to contact me with any questions. 

# Donations 
- Send me a coffee lefkotyler@gmail.com
