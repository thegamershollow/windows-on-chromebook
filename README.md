# Windows on a Lenovo 100e/300e gen2 ast Chromebook

A guide to installing windows on a Lenove 100e gen2 ast chromebook (for archive purposes)


## What you need

1. A Lenovo 100e/300e gen2 ast Chromebook.
2. A sd card or usb drive.
3. A mouse (wired, or dongle only).
4. Power adapter for the chromebook.
5. Ventoy downloaded for your OS
5. Drivers downloaded from this guide.
6. Tiny11 iso downloaded from this guide.

## Downloads

1. [Tiny 11 ISO](https://www.mediafire.com/file/vn0ucvdb389sxl3/tiny11_23H2_x64.iso/file)
2. [Ventoy](https://www.ventoy.net)
3. [Visual C++ Redist](https://aka.ms/vs/17/release/vc_redist.x64.exe)
4. [CR50 TPM Driver](https://github.com/coolstar/driverinstallers/raw/master/cr50/cr50.1.0.1-installer.exe)
5. [Chrome EC Driver](https://github.com/coolstar/driverinstallers/raw/master/crosec/crosec.2.0.6-installer.exe)
6. [Radeon GPU Drivers](https://drivers.amd.com/drivers/radeon-software-adrenalin-2020-21.5.2-win10-64bit-legacyasics-june21-legacy.exe) **!!DO NOT INSTALL UNTIL READING THE GUIDE!!**
7. [Radeon GPU Driver Patch](https://coolstar.org/chromebook/downloads/drivers/stoney-amdkmdag-patch.zip)
8. [Touchpad Drivers](https://github.com/coolstar/driverinstallers/raw/master/crostouchpad/crostouchpad.4.1.6-installer.exe)
9. [Touchscreen Drivers](https://github.com/coolstar/driverinstallers/raw/master/crostouchscreen/crostouchscreen.2.9.5-installer.exe)
10. [Audio Drivers](https://github.com/coolstar/driverinstallers/raw/master/csaudioacp2x/csaudioacp2x.1.0.0-installer.exe)
11. [7Zip](https://www.7-zip.org/download.html)
12. [Supermium](https://win32subsystem.live/supermium/)

## Getting Started

#### An Overview

This guide will show you how to go from chromeOS to Windows 11, you will need an internet connection for the chromebook, and also the other requirements listed [above](/#downloads)

Let's Get Started!

## Jailbreaking the Chromebook

### Step 1: Disable Hardware Write Protection

Open up the bottom of your Chromebook and disconnect the battery, then plug it into the charger, when you power it on the power light should blink.

### Step 2: Entering your Chromebook into Dev Mode
Press Esc + Refresh + Power.

Press Control+D to enter Developer Mode.

Press enter when it asks to turn OS verification off.

After it restarts press Control + D again.

Wait until it boots into Developer Mode.

### Step 3: Install New Firmware

Connect your Chromebook to the internet, but do not setup dev mode

Press Control + Alt + Forward Arrow

When you get to a prompt saying ```localhost login: ``` login as ```chronos```

**! Make sure you have internet enabled already or the following step won't work. !**

Then run ```cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh```

follow the instruction on screen, it may reboot once if it does do the above step again.

Then type 2 on the keyboard, and follow the instructions on the screen

after that you are succesfully Jailbroken.

### Step 4: Button up the computer

reconnect the battery and close up the laptop.

replug the laptop in or it might not turn on.

## Installing Windows 11

### Step 1: Installing Ventoy onto a USB/SD Card

Download the appropriate installer for your OS, if you are on Mac OS you will need to download the ISO file and use that instead.

### Step 2: Copying Tiny 11 iso to 'Ventoy' SD/USB

Download the Tiny 11 iso and copy it to your 'Ventoy' SD/USB

### Step 3: Copying the drivers to a folder on the Ventoy drive

Download all the drivers, 7ZIP and Supermium.

Copy the drivers and other files to a folder on your 'Ventoy' USB/SD 

### Step 4: Booting the installer

Insert the sd/usb into the chromebook 

Then turn on the chromebook and continualy press the escape key, till you get to a bios screen.

Then using the arrow keys go down to the ```boot menu``` option

You should see USB or SD Device in the menu

Boot into that and it should show the ventoy menu

Boot into the Tiny 11 iso and wait for it to show the setup screen.

**You will need to have a USB mouse plugged in to continue with the windows setup**

### Step 5: Deleting the old chromeos partitions

You will need to delete the chrome os partitions in order to install windows

### Step 6: Post Install Setup

Setup a **LOCAL** user account **! Do not sign in with a microsoft account as it will remove the automatic activation of Tiny 11 !**

Install all of the drivers that you downloaded **EXCEPT FOR THE GRAPHICS DRIVER**

### Step 7: Installing the GPU driver

Open cmd

type ```bcdedit -set testsigning on```

restart windows

**Make sure you downloaded version 21.5.2 of the gpu driver! But don't install yet!**

Double click the exe and click the first install (with destination folder). But Don't click install on any further installation wizards.

Wait for the driver to extract

Extract and copy the patched ```amdkmdag.sys``` to ```C:\AMD\Radeon-Software-Adrenalin-2020-21.5.2-Win10-64Bit-LegacyASICs-June21-LEGACY\Packages\Drivers\Display\WT6A_INF\B367348\amdkmdag.sys```

Proceed with the driver installation. Windows may ask you about installing an unsigned driver. Click "Allow"

Reboot. So long as testsigning is enabled, GPU should work and start immediately

### Step 8: Finishing up

install Supermium and 7ZIP if you haven't already.

now you are done !!! 

***ENJOY***
