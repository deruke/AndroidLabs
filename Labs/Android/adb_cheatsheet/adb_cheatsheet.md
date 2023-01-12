
* Connect to Corellium Android device with adb 

    - adb connect <VPN_IP>:5001 

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