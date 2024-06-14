# Removing Uttar Pradesh Government Privacy Invasion and Software Restrictions on Samsung Galaxy A03

The Uttar Pradesh government has been distributing free phones and tablets, but these devices come with restrictive work policies and software that invades your privacy. This guide will help you root your Samsung Galaxy A03 and remove these restrictions. Note that this process requires root access.

## Prerequisites
- **Root Access**: Ensure your device is rooted. If your device is already set up, you'll need to flash stock firmware and then flash a patched boot.tar file, as factory reset is disabled due to work policies.
- **Firmware**: Your device should be running the latest firmware.
- **Necessary APKs**: Download Magisk and Termux APKs and store them on a USB drive or SD card (not in internal storage).

## Preliminary Steps
1. **Internet Connection**:
   - If using mobile data, ensure you are connected.
   - If using Wi-Fi, navigate to the Wi-Fi setup screen, enter your password, and press the back button immediately.

## Step-by-Step Guide
1. **Access Accessibility Settings**:
   - At the welcome screen, tap on "Accessibility".
   - Toggle "Assistant menu".
   - Tap on the menu, swipe until you find "menu settings", and tap on it.
   - Keep pressing the back arrow in the top left until the main accessibility window appears.
   - Tap on "recommended for you".
   - Tap on "go to modes and routines".

2. **Install Required APKs**:
   - **If APKs are already downloaded**:
     1. Create a new routine, set it to execute manually, and select the files app.
     2. Execute it, allow the files app to access files.
     3. Tap on the SD card and install Magisk APK first, then Termux APK, and open Termux when prompted.
   - **If APKs are not downloaded**:
     1. Create a new routine, set it to open Chrome.
     2. Visit [hyperio546's Knox Bypass Samsung Page](https://hyperio546.github.io/knox-bypass-samsung/).
     3. Download Termux APK and Magisk APK from the respective links.
     4. Install the APKs in the same order as specified above.

3. **Disable Knox Components**:
   - Open Termux and type `su` to gain superuser access.
   - Grant superuser access from the popup.
   - Execute the following command:
     ```shell
     pm disable-user --user 0 com.sec.enterprise.knox.cloudmdm.smdms
     ```
   - Exit Termux by typing `exit` twice.

4. **Complete Setup**:
   - Press the back button until you return to the "Welcome!" screen.
   - Proceed with setting up your device as usual.

5. **Optional Step**:
   - To remove the assistant menu, repeat step 1 to access "menu settings" and toggle it off.

By following these steps, you should successfully root your device and remove the privacy-invasive software, giving you full control over your Samsung Galaxy A03.
