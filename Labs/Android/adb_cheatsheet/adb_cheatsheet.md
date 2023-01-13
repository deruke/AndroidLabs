This lab will familiarize you with a mobile app testing tool that is indispensible for Anrdoid testing, Android Debug Bridge (adb). You will exercise some of the most common features of adb such as gaining shell access to an Android device, moving files, installing APKs, and monitoring the system logger.

The first step will be to connect to your Android device in Correllium with adb. If you have a local Android device (i.e. plugged directly into your testing system), you generally don't need to perform this step. However, since our Android device is hosted in the cloud, we'll need to take advantage of adb's TCP connection feature to remotely access the device.

Navigate to Type the following command and hit `Enter`.

`adb connect <VPN_IP>:5001`

* Query adb for connected devices 

    - adb devices -l 

* Shell access with adb 

   - adb shell [cmd] 

* Install APK with adb 

    - adb install <path_to_apk> 

* Push files with adb (copy file to device)

    - adb push <local_path> <path_on_device> 

* Pull files with adb (copy file from device) 

    - adb pull <path_on_device> <local_path> 

* Install APK with adb 

    - adb install <path_to_apk> 

* Extract APK with adb 

    - List all package names 

         - adb shell pm list packages 

    - Find path to package 

        - adb shell pm path <package_name> 
        - 
    - Copy apk from device

        - adb pull <path_to_package> <local_path> 

* System log monitoring 

    - adb logcat 

* Find PID of app’s process 

    - adb shell ps | grep -i <package_name> 

* Filter logger on PID 

    - adb logcat | grep <PID> 