# BT-LinkkeySync
Script to synchronize bluetooth link keys from macOS to windows.
It generates a registry file for windows on macOS, which can afterwards be imported with the tool regedit in windows.

## Instructions
1. Pair all your bluetooth devices to your Mac (e.g. keyboard, mouse, headphones)
2. Open the Terminal and navigate to the folder where you have downloaded the file`BT-Linkkeysync.py`
2. Mark the script as executable with `sudo chmod +x BT-Linkkeysync.py`
3. Run the script with `sudo ./BT-Linkkeysync.py`(you will be asked for your password)
4. Store the generated file `btkeys.reg` file to a location accessible by windows.
5. Download [psexec](https://docs.microsoft.com/sysinternals/downloads/psexec)
   and store it to `C:/Windows/System32/`
6. Run the command:
   `psexec -s -i regedit`
7. Import the file `btkeys.reg`
8. No need to reboot
9. Use your keyboard on macOS and Windows

## Information
Test Environment:

* OSx86 Hackintosh with Asus BT-400 (USB-Bluetooth Adapter)
* macOS Sierra 10.12.1
* Windows 8.1 Prof
* Python 2.7

Tested Devices:

* Apple Magic Trackpad
* Apple Magic Keyboard
* Apple Magic Mouse
* LogiLink ID0032 Bluetooth Laser Mouse

## Limitations
BT 4.0 LE/Smart Devices (e.g. Logitech MX Master) do not work yet.
If you know how to get it working feel free to contribute :)

## TODO's
Try the other way round (Pair on Windows and import in macOS) maybe get Bluetooth 4.0 LE Working

## Credits
Related [Blog Post on InsanelyMac](http://www.insanelymac.com/forum/topic/268837-dual-boot-bluetooth-pairing-solved/) of camoguy

## Links
* [Dual Boot Bluetooth Pairing Solved](http://www.insanelymac.com/forum/topic/268837-dual-boot-bluetooth-pairing-solved/)
* [Dual pairing in OS X and Windows](https://discussions.apple.com/thread/3113227?start=0&tstart=0)
* [OS-X-Bluetooth-Pairing-Value-To-Windows-Value](https://github.com/Soorma07/OS-X-Bluetooth-Pairing-Value-To-Windows-Value)
