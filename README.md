# UX360UAK-Hackintosh
Resources for Asus Zenbook Flip UX360UAK Hackintosh
Running on macOS High Sierra 10.13.6

## What's working
Almost everything

## What's not working
- Wi-fi and Bluetooth
- Touchscreen (conflicts with trackpad because it sits on the same I2C bus)
- Fingerprint
- Card reader

## Still needs fixing
- Keyboard backlight state not persistent across shutdowns/reboots (maybe something with the NVRAM?)
- Trackpad not detected by the prefpane immediately (need to give some time for the prefpane to pick up the trackpad)
- Battery status in menu bar is not working properly (eg. battery percentage not updating, can't detect if AC power is plugged in or off)
- Can't use microphone through audio jack (maybe due to Audio ID injection)
- Few audio problems especially after sleeps (mostly addressable by reloading CodecCommander kext)

## SSDTs
- SSDT: SSDTPRGen
- SSDT-RMNE: NullEthernet
- SSDT-UIAC: USB injection
- SSDT-PNLF: Intel backlight

## Drivers64UEFI
- ApfsDriverLoader-64
- AppleImageCodec-64
- AppleKeyAggregator-64
- AppleUITheme-64
- AptioMemoryFix-64
- DataHubDxe-64
- FirmwareVolume-64
- FSInject-64
- OsxFatBinaryDrv-64
- PartitionDxe-64
- Ps2MouseDxe-64
- SMCHelper-64
- UsbKbDxe-64
- UsbMouseDxe-64
- VBoxExt4-64
- VBoxHfs-64

## Kexts
- ACPIBatteryManager
- AppleALC
- AsusNBFnKeys
- CodecCommander
- FakePCIID_XHCIMux
- FakePCIID
- FakeSMC_ACPISensors
- FakeSMC_CPUSensors
- FakeSMC_GPUSensors
- FakeSMC_LPCSensors
- FakeSMC
- GenericUSBXHCI
- Lilu
- NullEthernet
- NullEthernetInjector
- RealtekRTL8111
- USBInjectAll
- VoodooI2C
- VoodooI2CHID
- VoodooPS2Controller
- WhateverGreen

## Patches
- Fn Brightness Keys
- KeyboardBacklight Patch 4
- UX360UAK battery patch
- Disable touchscreen (TPL0)
- ZenBooks LidSleep and ScreenBackLight Patch
- Windows 10 OS patch
