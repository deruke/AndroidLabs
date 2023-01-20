# Importing Burp's CA Certificate to the System-Trust Store (Android) 
In this lab we will import and install Burp's CA certificate to the System-Trust store of our virtual mobile device.

**NOTE**: The mobile device must be rooted in order to install a CA certificate to the System-Trust store. We'll be utilzing a rooted Android device in Corellium for this lab.

**IMPORTANT**: Starting with Nougat (Android 7.0 - API level 24) certificates installed to the User-Trust store are ignored by default; however, with Corellium's implementation of Android devices, some naitive applications have been "patched" to trust the user cert store. If you are using a different mobile device solution for testing, Android devivces 7.0+ (API >= 24) will require the Burp CA cert to be installed to the System-Trust store. Additionally, 3rd-party apps installed on a Corellium virtual mobile device may only trust CA certificates in the System-Trust store. 

(see XXX Lab for adding Burp's CA to the System-Trust on Android devices).

https://github.com/deruke/AndroidLabs/blob/main/Labs/LAB_X_Burp-Proxy-Setup/burp-proxy-setup.md#configure-the-virtual-mobile-devices-certificate-trust-for-the-burp-proxy-certifcate-authority-ca---user-trust

In order to ensure network traffic is routed from the virtual mobile device to our MobileApp VM, a VPN connection between the two hosts is required. If you don't have a VPN connection established, rerfer to the [lab](https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/gettingstarted.md#VPN) on how to setup a VPN connection.

## Export Burp's CA Certficate and Prep for Install
1. 


