# Setup Corellium and Establish Remote Connections
Corellium URL: https://app.corellium.com/login
## Creating an Android Device in Corellium
Login to your Corellium account and select the **DEVICES** tab and click **CREATE DEVICE**.

![Create a New Device](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/create-device.jpg)

Next, select **ANDROID -> Generic Android** and select **NEXT**

![Create an Android Device](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/create-android-device.jpg)

Select the firmware package, **12.0.0 (Build r26 userdebug)**, from the dropdown menu and click **SELECT**.

![Firmware Package](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/android-firmware-package.jpg) 

Leave the checkbox unchecked and select **CREATE DEVICE**

![Create Device Confirm](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/create-device-confirm.jpg)

Corellium will then proceed to create the virtual deivce. 

![Creating Device](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/creating-device.jpg)

Once the build is complete, you should now have a virtual Android Device with menu options as shown below.

![Android 12 - Rooted](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/android-12-device-rooted.jpg)

## Navigating Menu Items in Corellium ##

The menu items associated with your Android device should look like the following.

![Device Menu Items](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/images/device-menu-options.jpg)

The following list contains a high-level description of each menu item.
 * Connect - This feature allows the tester to remotely connect to the virtual Android device for testing. 
 * Files – Corellium gives you control over the device filesystem, allowing you to upload, download, delete, modify, and search for files.
 * Apps – Manage Apps installed on the virtual device (i.e., install/uninstall, launch/kill apps).
 * Network – The Network Monitor captures, presents, and monitors HTTPS traffic, transparently defeating certificate pinning.  
 * CoreTrace:
 * Settings
 * Frida
 * Console – Use the Console option to see system and kernel logs and quickly run commands without needing to connect over ADB or SSH.
 * Sensors
 * Snapshots

## Remotely Connecting to your Virtual Mobile Device ##

Establishing a network connection between your mobile device and your testing platform is required to perform actions such as proxying and intercepting Internet traffic, which enables security practitioners to further evaluate a given mobile application under an active/running state. Additionally, tools like the Android Debugger (adb) can be leveraged remotely from the tester’s virtual machine to the virtual mobile device running in Corellium. 
In this section we will cover two options for establishing remote network capabilities to/from your MobileApp Virtual Machine and the virtual mobile device running in Corellium: SSH and VPN.

### SSH ###
1. Create a unique SSH keypair (public and private certificates) from your MobileApp VM:
 a. From the command prompt, type the following command and hit enter.

### VPN ###
