I publish this repo because properly compiling and uploading the 

## FlipperZero ready to use blackmagic binaries
Compiled with no changes from https://github.com/flipperdevices/blackmagic-esp32-s2/commit/473bdd4d0952a731ae1abd7ac0644401fed65eaa


### Installation

Download the zip repository file and unzip it inside a folder.
Press the boot button on the ESP32S2 en plug it into the PC
Run cmd and move to this folder (for example):
```sh
cd C:\Users\bob\Desktop\FlipperBlackMagicReady
```
Run this command inside the extracted folder replacing the COM1 port with yours:
```sh
esptool.exe -p COM1 -b 460800 --before default_reset --after hard_reset --chip esp32s2  write_flash --flash_mode dio --flash_size detect --flash_freq 40m 0x1000 bootloader.bin 0x8000 partition-table.bin 0x10000 blackmagic.bin
```

Enjoy

### Configuring
Connect to the created network:
SSID: blackmagic
Password: iamwitcher

Type 192.168.4.1
Change the settings to your desire
Click save
Reboot

### Support
If this help you please leave a star to this repo or donate using my donation link:
https://pypal.me/alvarotorijano

