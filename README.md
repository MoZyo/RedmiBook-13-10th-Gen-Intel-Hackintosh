# RedmiBook-13-10th-Gen-Intel-Hackintosh
A Hackintosh - Opencore for Xiaomi RedmiBook 13 2019-2020

### Specs:
Type | Details
| -------------- |:----------------------------:|
CPU | i5-10210u / *i7-10510u*
iGPU | Intel UHD620
dGPU | NVidia MX250
Display | 1920x1080
RAM | 8GB 
Audio | Realtek ALC256
Network | Intel 9462AC
Mobo | TIMI TM1921 (U3E1)
SSD | 500gb SAMSUNG MZNLN512HAJQ SATA
KB | Standard PS2 Keyboard
TP | ELAN I2C HID Trackpad
SMBIOS | MacBookPro 16,1
Bootloader | OpenCore 0.5.8

### What works and What doesn't or WIP:
-----
- [x] Intel UHD620 iGPU
- [x] USB Ports
- [x] Sleep / Wake
- [x] Touchpad
- [x] NVRAM
- [x] HDMI Out
- [x] Headphone Sound
- [x] Internal / External Mic

- [ ] Internal Speakers (I'M GOING NUTS!)
- [ ] Backlight Controls
- [ ] Bluetooth
- [ ] WiFi (Not yet supported)
- [ ] MX250 dGPU (Not supported)

## Important Notes:
- This is a **Work in Progress [WIP]**.
- Do not COPY & PASTE this and use on your installer or Mac disk's EFI Partition. This is to give you idea on what will work and a jump start to hackintosh this laptop.
- SSDT-RMNE and NullEthernet are used for fixing iServices. Once you are already loggen in on your iMessage, you can remove SSDT-RMNE.
- SMBIOS information are reset to default values... Apply your generated SMBIOS.
- My created layout is at layout-id 27. You are free to try it. You can also try layout-id 11.
- All guides and very much needed information can be read in [Dortania's Guide](https://dortania.github.io/vanilla-laptop-guide/ "Overview - Dortania").

- Fixes for current problems are appreciated.

## To-do after installation:
* Generate your SMBIOS and put info in the 'Generic' part of config.plist.
* Open a terminal in `ComboJack` folder and run `ComboJack_Installer/install.sh`. (Optional)
  - It is known to make headphone sound quality better.
* 

## Changelog
<details>
<summary>Read Changelog...</summary>
  <h2> 05/25/20 </h2>
  <ul>
    <li>Repository created. Will probably ask help for the dreaded internal speaker situation on Reddit.</li>
  </ul>
  <ul>
      <li>Known that FakePCIID its HDMI_Audio kexts is the key for making audio work for Intel 10th Gen with ALC256 and ALC3204/236 Sound Cards. Audio PCI must be called out with device-id in config.plist</li>
    <ul>
      <li>Tested on @R3TLIX's Dell Vostro 5590 and it worked. Thanks to <a href="https://www.hackintosh-forum.de/user/40078-noirosx/">NoirOSX</a></li>
    </ul>
  </ul>
    <ul>
      <li>Managed to get Internal Speakers on Output, Mic (works, I can see movement when I speak) in Input. Switches to Headphone when plugged in (works).</li>
      <ul>
      <li>Tried different PathMaps and Verb Data in PinConfigs.kext. (AppleHDA Patching)</li>
      <li>Tried every layout there is for AppleALC's ALC256. (none worked to make internal speaker to work).</li>
    </ul>
</details>

## Credits
- [Apple](https://apple.com) for MacOSX
- [@R3TLIX](https://github.com/R3TLIX) for assistance.
- [NoirOSX](https://www.hackintosh-forum.de/user/40078-noirosx/)
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- Hackintosh Paradise Discord Server
