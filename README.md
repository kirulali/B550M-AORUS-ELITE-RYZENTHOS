# B550M-AORUS-ELITE-RYZENTHOS TAHOE

Opencore EFI folder for  B550m Aurous Elite Ryzen 5 3600, Sapphire Radeon 5700XT 8GB for OSX Tahoe.
This is a prebuilt EFI folder to install MACOSX Tahoe.

## SPECIFICATIONS

- Motherboard: Gigabyte B550m Aurous elite 1.3
- CPU: AMD Ryzen 5 3600
- Memory: 16GB 3200mhz Kinstone Fury Beast
- SSD: 120GB Samsung (i am used to install to as USB Drive)
- Graphics: Sapphire Radeon 5700XT 8GB
- Sound: ALC887
- Ethernet: RTL8111, RTL8125

## CONFIGURATION

The installer boot fine with this EFI folder, but you should make some modifications, exspecially when you have different processor.

If you have different processor may need to edit the config.plist, please follow this tutorial: [AMD-OSX_VANILLA](https://github.com/AMD-OSX/AMD_Vanilla)

Use [propertree](https://github.com/corpnewt/ProperTree) to edit the config.plist file

Change the SMBIOS data (please use MacPro7,1 or IMacPro1,1): [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

## AUDIO FIX

You need to download [voodoohda](https://github.com/CloverHackyColor/VoodooHDA/releases/tag/Release302) extract the zip file and run these commands:

sudo xattr -cr VoodooHDA.kext

sudo spctl --master-disable

sudo cp -r VoodooHDA.kext /Library/Extensions/

Reboot and then you have audio.

## BIOS SETTINGS

- Fastboot	Disabled 
- Secure Boot	Disabled
- IOMMU	Disabled
- CSM	Disabled
- Above 4G Decoding	Enabled (if you can't find the option then add npci=0x3000 or npci=0x2000 to boot-args)
- Resizable BAR Support	Enabled (When enabling Above 4G, Resizable BAR Support can be enabled Please ensure that Booter -> Quirks -> ResizeAppleGpuBars is set to 0 if this is enabled.)
- SATA Mode	AHCI

## WHATS NOT WORKING

running vm

## USED SOURCES

[AMD Vanilla](https://github.com/AMD-OSX/AMD_Vanilla#) - AMD Cpu patch

[Dortania](https://dortania.github.io/OpenCore-Install-Guide/) - Install guide for opencore

[Acidanthera](https://github.com/acidanthera) - OpenCore Bootloader kexts


If you like to support me than hit the buymeacoffee button :)

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black)](https://www.buymeacoffee.com/felhasznalonev)


