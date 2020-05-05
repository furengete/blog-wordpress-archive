---
title: "Hackintosh: Installing macOS High Sierra 10.13.5 on PC"
date: "2018-07-12"
---

Computer Specifications:

- Motherboard: Xeon E3 - 1200 v6/7th Gen Intel Core - 591F - 100 Series/C230 Series
- CPU: i5-7400 with Intel HD 630 Build-in Graphic card
- GPU: Nvidia GeForce 1050 Ti
- SSD: Samsung SSD 860 EVO SATA
- RAM: 2 x 8GB DDR4
- Audio: ALC887
- Ethernet: RTL8111
- System Detonation: Mac 18,2

Websites:

1. [https://www.tonymacx86.com](https://www.tonymacx86.com)
2. [https://hackintosher.com](https://hackintosher.com)
3. [the macOS Sierra step-by-step install guide](https://www.youtube.com/watch?v=pugSN7REHQg&index=2&list=LLt2bfUmmBFjrH7ZEvMkPxgg)
4. [Hackintosh Step-by-Step Build Guide - $1000 4K Editing Monster](https://www.youtube.com/watch?v=3MUznCgBmwM&list=LLt2bfUmmBFjrH7ZEvMkPxgg&index=5)
5. [HACKINTOSH HIGH SIERRA 10.13.5 UPDATE GUIDE](https://hackintosher.com/guides/hackintosh-high-sierra-10-13-5-update-guide/#kext)

Note:

Timeline: 7/5/18 - 7/10/18

- 7/5/18 macOS Virtual Machine Installed successfully with VMware 14.1, macOS High Sierra 10.13.5 downloaded in the virtual machine on Windows 10
- 7/6/18 Try to Install bootable USB drive on VM with Unibeast 8.3.2 failed ( There are an error creating your Unibeast drive: Copy of apfs.efi failed )
- 7/7/18 Samsung 860 EVO SSD Purchased $65 + $3 ( transport ) and still trying to install bootable USB drive with Unibeast succeed when I after reading [Unibeast Troubleshooting](https://www.tonymacx86.com/threads/unibeast-8-troubleshooting-notes.235489/). Plus to make sure destination volume type ‘df -lh’ in Terminal 
- 7/8/18 SSD installed and failed to boot USB drive on PC
- 7/9/18 NVIDIA 1050 Ti GPU uninstalled then PC automatically switch the GPU to Intel HD630 build-in CPU
- 7/10/18 Created the bootable USB drive with Clover 4458 to Boot successfully and installed macOS high Sierra on SSD

\* I failed about 5 times when booting by the bootable USB drive which Unibeast created. There are 2 mistakes I have made:

1\. Erase the USB Volume and I do not know how to chose the scheme option to GUID Partition Map. My VM macOS System default the view to Show only Volumes. So I just erased the volume instead of the whole disk. [No partition scheme option when erasing a USB disk in MacOS High Sierra?](https://apple.stackexchange.com/questions/304131/no-partition-scheme-option-when-erasing-a-usb-disk-in-macos-high-sierra) 

2\. The Unibeast is not updated for 10.13.5 version installation, I noticed that it build at 2018-04-06 contains Clover version 2.4k rev 4428 but 10.13.5 released at 2018.6.1.

He got the same issue [Installing High Sierra 10.13.5 - Stuck at Apple Logo Black Screen - First Hackintosh](https://www.tonymacx86.com/threads/installing-high-sierra-10-13-5-stuck-at-apple-logo-black-screen-first-hackintosh.253457/). 

Finally, I decided to try Clover to install by myself instead, also I see someone failed [issue with clover 4586 - MacOS 10.13.5](https://www.tonymacx86.com/threads/report-issue-with-clover-4586-macos-10-13-5.255268/) by using Clover latest update and he says Clover 4458 works fine for him.) 

Main steps:

1. Download macOS High Sierra 10.13.5 in App Store. The Application **Install macOS High Sierra** will appear in /Applications.
2. Create a bootable USB drive with Clover 4458. Open /Applications/Utilities/Disk Utility, select show all devices, then Highlight the USB drive in the left column, click **Erase** button, For Format: choose Mac OS Extended (Journaled), click **Erase** then **Done**. Then open up the terminal window enter command string below to loads the macOS installer on your USB driver, it takes 30mins+. Then download Clover Bootloader EFI 4458 and kexts like FakeSMC.kext, Lilu.kext, just follow the tutorial.
3. Use recommended BIOS settings on [tonymacx86.com](http://tonymacx86.com) 
4. Boot from the USB drive to install macOS High Sierra on SSD. For best results, insert the USB in a USB 2.0 port. I got an issue “macOS could not be installed on your computer”, someone reported here [High Sierra: Fresh Install Issue - "The installer resources have expired"](https://www.tonymacx86.com/threads/high-sierra-fresh-install-issue-the-installer-resources-have-expired.249020/) and I see a reply which is works for me. 
5. Install NVIDIA Web Driver [Download 10.13.5 -387.10.10.10.35.106 (17F77)](https://images.nvidia.com/mac/pkg/387/WebDriver-387.10.10.10.35.106.pkg) and copy all kext files [Kext Page List](https://hackintosher.com/kexts/) to EFI/Clover/kexts/Other folder after Clover done its own jobs on SSD or post installation with MultiBeast directly.

Troubleshooting: [Troubleshooting and Optimizations on tonymacx86.com](https://www.tonymacx86.com/threads/unibeast-install-macos-high-sierra-on-any-supported-intel-based-pc.235474/#uefi_settings)

1. Window glitching: install 1050 Ti back instead of keep using Intel HD630
2. HHKB Driver for iMac [Mac用ドライバ （HHKB Professionalシリーズ専用）](https://www.pfu.fujitsu.com/hhkeyboard/macdownload.html) 
3. No Audio detected: [THIS IS HOW TO GET HACKINTOSH AUDIO WORKING](https://hackintosher.com/guides/get-hackintosh-audio-working/)
4. Detected Audio but sound not working: [AppleALC Supported Codecs](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs) layout is 1 
5. Sleep Breaks Audio: [RehabMan-CodecCommander-2017-0501](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/downloads/)
6. Video Playback Freezes: [Incompatible Kext Fix](https://hackintosher.com/guides/get-hackintosh-audio-working/#Incompatible-Kext)
7. [Fix incorrect time in Windows + OSX dual boot](https://www.tonymacx86.com/threads/fix-incorrect-time-in-windows-osx-dual-boot.133719/)
8. [AMD/Nvidia Primary Display with AirPlay Mirroring](https://www.tonymacx86.com/threads/amd-nvidia-primary-display-with-airplay-mirroring.118662/#post721605)
9. [MONITOR HEALTH SENSORS: TEMPERATUE, VOLTAGE, FANSPEED](https://hackintosher.com/guides/hwmonitor-hackintosh-guide/)
10. [Check Sirial Number](https://checkcoverage.apple.com)
