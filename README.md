# Hackintosh-Dell-G15-5510 (i7 10870H - RTX 3060)

EFI file for a Dell G15 5510 with i7 10870H and RTX 3060 (OpenCore 1.0.2, tested on Ventura 13.6.5 — Sonoma not tested yet)

HDMI don't work

airdrop don't work (of course)

everything else works !

If u don't know how to do a hackintosh, follow the guide : https://dortania.github.io/OpenCore-Install-Guide/

# Some tips to know to make your Dell hackintosh 

- make a good configuration of your BIOS (disable thunderbolt, fastboot and other things explain in the guide)

- during installation your pc will restart several times, be sure that the priority at the time of the reboot is on the disk containing opencore

# Quick tutorial for beginners

- Get the raw or iso file of macOS

- Flash your USB (16GO, tool : BalenaEtcher)

- Use tool to change the name of the EFI partition (tool : MiniTool Partition Wizard)

- Use tool to replace the EFI file by mine (tool : Explorer++)

- Restart your pc and go to the BIOS and change somes settings

- Select your USB for booting

- Go read a book

# Before you boot

- Generate your own SMBIOS values (serial, MLB, UUID, ROM) for `MacBookPro16,4` with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) and put them in `PlatformInfo` : don't reuse the ones shipped in `config.plist`

- SIP is partially disabled in this config (`csr-active-config` = `850A0000`). If you want it fully enabled, set it to `00000000` and reset NVRAM

- Only the drivers and tools enabled in `config.plist` are shipped. If you need another one, take it from the matching [OpenCore release](https://github.com/acidanthera/OpenCorePkg/releases)

# Tools

- BalenaEtcher : https://www.balena.io/etcher

- MiniTool : https://www.partitionwizard.com/free-partition-manager.html

- Explorer++ : https://explorerplusplus.com/download


# Miscellaneous

This EFI file is not only from me but also from people on Reddit and discord so thanks to them

Thanks to [KD-MM2](https://github.com/KD-MM2) for the OpenCore 1.0.2 and kexts update

I took 4 days to make a perfect configuration for my pc, if you don't have the right configuration look on github or dedicated forums, if you find optimizations or modifications for future MacOs updates do not hesitate and above all SHARE YOUR CONFIGURATION THIS CAN HELP OTHERS

I am currently working to solve the HDMI problem if you find before me do not hesitate to give a tutorial !
