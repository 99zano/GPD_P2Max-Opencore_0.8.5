# GPD P2 Max Monterey Hackintosh
GPD P2 Max Opencore Efi folder, tested with Monterey 12.5.1 and 12.6

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
- Touchpad and keyboard :small_orange_diamond:
- TouchScreen :small_orange_diamond:

## Not Working
- Fingerprint reader
- Airdrop (never working, wireless card soldered)

## Notes :small_orange_diamond:
- In order to boot you need to set the **DVMT Pre-Allocated** from 32M to 64M, **CFG Lock** unlock is needed for enabling native power management 
- **BIOS** version installed on my GPD is 0.29, type the following in grub:
  - setup_var Setup 0x876 0x02 <sub>*(DVMT)*</sub>
  - setup_var Setup 0x587 0x00 <sub>*(CFG Lock)</sub>*
- **Touchpad:**
  - I downgraded the keyboard firmware according to @Azkali repository, requiered file is in *touchpad*
- **Touchscreen:**
  - works only using the older versions of i2c and i2cgoodix but it stops working upgrading just one of those kexts to the latest version
  - multitouch works well only up to two fingers, maybe fixable but I'm not dedicating any time on it
- **Undervolting:**
  - I'm currently running voltageshift 1.25 with all the offsets at -70mV, these values aren't searched accurately, shurely much stabler values can be found
- Remember to change itlwm **country code** in boot args according to your contry and to generate your own **serial number**

## Screenshots
<img width="1280" alt="Schermata 2022-10-24 alle 19 31 02" src="https://user-images.githubusercontent.com/106203008/197646313-9f3db39d-f832-4e36-bccb-42875691a851.png">

## <img width="1280" alt="Schermata 2022-10-24 alle 12 44 16" src="https://user-images.githubusercontent.com/106203008/197648199-6c11d572-74a5-4e25-bcd9-e00c4007d8b6.png">
 
## Credits
Thanks to @Azkali, his Clover EFI was crucial for this project, to @dortania team and the GPD guys for gave us this unique machine
