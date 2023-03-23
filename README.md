# Dell-Latitude-E5480-Hackintosh
**NOTE**
* OC ver: 0.8.3
* Generate new SMBIOS before using.
* You should adjust DVMT and disable CFG-Lock
* Work fine on Monterey. If using BigSur, you'll need to make some changes with kext.
* If you want to use Ventura, add boot-arg -lilubetaall, update Airportitlwm.kext and change device-id in DeviceProperties to 7th Gen KabyLake (to fix iGPU).

## My Laptop Specs

**Dell Latitude E5480**
- **CPU:** Intel® Core™ i5-6300U Skylake
- **GPU:** Intel® HD Graphics 520
- **RAM:** 8GB DDR4
- **Ethernet:** Intel® Ethernet I219-LM
- **Wi-Fi:** Intel® Dual Band Wireless-AC 3168
- **Sound Card:** ALC256 (ALC3246)
- **Touchpad:** I2C HID Device (I can't find its extract name)
- **Disk:** SSD Kingston NV1 M.2 PCIe Gen3 x4 NVMe

## Working
✅ Graphics Acceleration  
✅ Display with HDMI  
✅ All USB Ports  
✅ Ethernet  
✅ Wifi, Bluetooth (not Airdop)  
✅ Audio (Jack, Speaker and Microphone)  
✅ Webcam  
✅ Sleep and Wake  
✅ iMessages and Factime  
✅ Multi Gestures Trackpad  

## Not Working
❌ Airdrop and Handoff  
❌ DRM  
❌ Please tell me  

## Not tested yet
⚫ Display with VGA and USB-C (because I don't need them)  
⚫ Card Reader  
