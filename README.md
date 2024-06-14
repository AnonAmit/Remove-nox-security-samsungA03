# How to Root Samsung Galaxy A03 the Proper Way

This guide will help you root your Samsung Galaxy A03 without encountering bootloops. It ensures you have a smooth rooting process and can be adapted for similar Samsung devices.

**Note:** This guide will void your warranty and trip KNOX. I am not responsible for any damage to your phone.

## Prerequisites

1. **Backup Your Data**: Your device will be factory reset.
2. **Latest Firmware**: Ensure your device is on the latest firmware.
3. **Samsung USB Drivers**: Download and install from [here](https://developer.samsung.com/mobile/android-usb-driver.html).
4. **ODIN**: Download from [here](https://odindownload.com/).
5. **7-Zip**: Download and install from [here](https://www.7-zip.org/).
6. **Firmware Zip**: Download using [Frija](https://forum.xda-developers.com/t/tool-windows-frija-samsung-firmware-downloader-checker.3910594/).

## Step-by-Step Guide

### Preparing the Boot Image
1. **Download Firmware**:
   - Download the firmware zip using Frija.
2. **Extract Firmware**:
   - Extract the downloaded firmware zip.
3. **Extract Boot Image**:
   - Extract `boot.img` from the AP archive.
4. **Patch Boot Image with Magisk**:
   - Open Magisk and patch `boot.img`.
   - Copy the patched `boot.img` back to your PC.
5. **Rename and Archive Boot Image**:
   - Rename the patched file to `boot.img`.
   - Right-click on `boot.img`, hover over 7-Zip, and click on "Add to archive".
   - Select "tar" as the archive format.

### Preparing the Device
6. **Enable OEM Unlock**:
   - Go to Developer Options (tap the build number in software info repeatedly until Developer Options are enabled).
   - Toggle "OEM unlock" in Developer Options.
   - If your device is carrier locked, you cannot proceed further.
7. **Enter Bootloader Mode**:
   - Power off the device.
   - Press Volume Up + Volume Down, then connect the USB cable from the phone to the PC.
   - A warning screen should appear.
   - Long press Volume Up, then press Volume Up again to confirm.
   - The device will reset, unlocking the bootloader.

### Flashing Patched Boot Image
8. **Enter Download Mode**:
   - Power off the device again.
   - Press Volume Up + Volume Down, then connect the USB cable.
   - Short press Volume Up to enter Download Mode.
9. **Open ODIN**:
   - ODIN should show "Added!!!" in the log. If not, reinstall the drivers and reboot.
10. **Flash Boot Image**:
    - Click the AP button in ODIN and select the `boot.tar` file.
    - Click "Start" to flash the patched boot image.
    - The device will automatically reboot.

### Finalizing the Root
11. **Setup Device**:
    - Set up your phone as usual.
12. **Install Magisk**:
    - Install Magisk on your device to manage root access.

## Optional: Removing Privacy Invasion and Software Restrictions

If you received this device through the Uttar Pradesh government's free phone initiative and need to remove privacy invasion software, follow these steps after rooting:

1. **Install Necessary APKs**:
   - Download Magisk and Termux APKs and store them on a USB drive or SD card.
2. **Access Accessibility Settings**:
   - At the welcome screen, tap on "Accessibility".
   - Toggle "Assistant menu".
   - Open the Assistant menu, swipe to "menu settings", and tap on it.
   - Tap "recommended for you", then "go to modes and routines".
3. **Create a New Routine**:
   - If APKs are already downloaded:
     - Create a new routine, set it to execute manually, and select the files app.
     - Install Magisk APK and Termux APK from the SD card.
   - If APKs are not downloaded:
     - Create a new routine, set it to open Chrome.
     - Visit [hyperio546's Knox Bypass Samsung Page](https://hyperio546.github.io/knox-bypass-samsung/).
     - Download and install Termux and Magisk APKs.
4. **Disable Knox Components**:
   - Open Termux and type `su` to gain superuser access.
   - Grant superuser access from the popup.
   - Execute the following command:
     ```shell
     pm disable-user --user 0 com.sec.enterprise.knox.cloudmdm.smdms
     ```
   - Exit Termux by typing `exit` twice.
   - Keep pressing back button in the bottom left until it gets to "Welcome!" again.
   - Setup your device like normal.
   - You have *your* device back!

By following this guide, you will successfully root your Samsung Galaxy A03 and remove any privacy-invasive software. Enjoy your fully controlled device!

## Handling OTA Updates

For Samsung devices, the OTA updater might break after rooting. To update:
1. Flash the latest official firmware using ODIN.
2. Flash the patched boot.img separately.

If successful, this process will keep your device updated and rooted.
