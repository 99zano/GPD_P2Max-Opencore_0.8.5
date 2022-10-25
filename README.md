# GPD P2 Max Monterey Hackintosh
GPD P2 Max Opencore Efi folder, tested with Monterey 12.5.1 and 12.6 

## Requierements
You need to set the DVMT Pre-Allocated from 32M to 64M and to unlock the CFG Lock for enabling native power management *(see notes)*

## Working
- Graphics Acceleration
- Brightness control and hotkeys
- Volume control and hotkeys (speakers, mic, jack)
- Camera
- USB's
- Battery status and native power management
- Sleep/Wake
- Bluetooth
- Internal Wifi
- Touchpad and keyboard *(see notes)*
- TouchScreen *(see notes)*

## Not Working
- Fingerprint reader (never working)
- Airdrop (obviously never working, wireless card soldered

## Notes
- **BIOS** version I used is 0.29
- For set the DVMT Pre-Allocated to 64M and unlock the CFG Lock I typed the following from grub:
  - setup_var Setup 0x876 0x02 <sub>*(DVMT)*</sub>
  - setup_var Setup 0x587 0x00 <sub>*(CFG Lock)</sub>*
- **Touchpad:**
  - I downgraded the keyboard firmware according to @Azkali repository, requiered file is inside *touchpad_fix*
- **Touchscreen:**
  - using the older versions of i2c and i2cgoodix touchscreen works but it stop working if upgraded to the latest version one of those kexts
  - multitouch isn't fully enabled and works well only up to two fingers, shurely is fixable but sadly i didn't have more time to spend on this little big guy
- **Undervolt:**
  - I'm currently running voltageshift 1.25 with all the offsets at -70mV, i did not search these values accurately, maybe much stable values can be found

## Screenshots
<img width="1280" alt="Schermata 2022-10-24 alle 19 31 02" src="https://user-images.githubusercontent.com/106203008/197646313-9f3db39d-f832-4e36-bccb-42875691a851.png">
<img width="1280" alt="Schermata 2022-10-24 alle 12 44 16" src="https://user-images.githubusercontent.com/106203008/197648199-6c11d572-74a5-4e25-bcd9-e00c4007d8b6.png">
 
## Credits
Thanks to @Azkali, his Clover EFI was crucial for this project, to the amazing @dortania team and to the GPD guys for this little big beauty 
