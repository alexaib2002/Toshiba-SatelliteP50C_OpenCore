# Toshiba-SatelliteP50C_OpenCore
Open Core EFI Files for booting on Toshiba Satellite P50C

## Instructions
This repository only provides the configuration files that I used to boot macOS after following the <a href="https://dortania.github.io/OpenCore-Install-Guide/">official instructions</a>
All you need to do if you have this same laptop is download your prefered version of macOS <a href="https://github.com/acidanthera/OpenCorePkg/blob/master/Utilities/macrecovery/macrecovery.py">using macrecovery.py utility</a> (I used the latest one available, Monterey) and place it on your FAT drive. 
The bootloader has the graphical user interface enabled.
You'll need to:

- Copy the EFI folder into a FAT formatted drive.
- Select the pendrive as boot device on boot menu.
- macOS recovery image should be located on the drive's root.

You may want to add the <b>ext4</b> driver to OpenCore bootloader (I dual booted with a system on BTRFS filesystem).

## Bugs
Although I'm not working actively on fixing these problems (as I won't use macOS as my main system), its pretty usable. Keep in mind that current configuration it's not perfect, all the problems I have found so far:

- Computer isn't able to wake after sleep (seems something related to USBs/PCI layout)
- Shutting down causes random system crashes while powering off (It's not a breaking problem, though I couldn't find anything to fix this problem so...).
- Battery drains too fast (also, macOS keeps reporting there are some problems related to battery)
- No powersave option on battery menu (could have some relation with draining too fast?)

