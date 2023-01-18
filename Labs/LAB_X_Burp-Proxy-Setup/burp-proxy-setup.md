# Setup Burp Suite for Proxy and Interception Testing 
In this lab we will setup a web proxy using *Burp Suite's Community Edition* and route traffic from our virtual mobile device in Corellium to our MobileApp VM where Burp resides. Following this setup, we will have the capability to intercept web requests made by a given mobile application, as well as inspect and/or manipulate network traffic for the purposes of mobile application testing. 

In order to ensure network traffic is routed from the virtual mobile device to our MobileApp VM, we first need to establish a VPN connection between the two hosts. More details on how to setup a VPN connection can be found [here] (https://github.com/deruke/AndroidLabs/blob/main/Labs/Corellium_Setup/gettingstarted.md#VPN).

## Open and Configure Burp
1. With a VPN connection established, return to your MobileApp VM and launch Burp Suite Community Edition by either running to following command or clicking on the Burp icon in the Favorites Toolbar.
 
 - Option 1: Launch Burp via the command line.
   `/home/mobileapp/BurpSuiteCommunity/BurpSuiteCommunity &`

 - Option 2: Launch Burp via the Favorites Toolbar.

 ![Launch Burp Suite](https://github.com/deruke/AndroidLabs/blob/main/Labs/LAB_X_Burp-Proxy-Setup/images/burp-temp-project-1.jpg)

2. Select **Temporary project**, then click **Next**

 ![Launch Burp Suite](https://github.com/deruke/AndroidLabs/blob/main/Labs/LAB_X_Burp-Proxy-Setup/images/burp-temp-project.jpg)

3. Using Burp's menu items, navigate to **Proxy -> Options**

4. Uncheck the "Running" checkbox for interface 127.0.0.1:8080

5. Next click **Add**, then **Bind to address**, and select the IP address assigned to the tap0 interface. Also, enter the port number in the **Bind to port** field. An example configuration is shown below.  NOTE: The address assigned to your tap0 interface may be different.
 
 ![Burp Proxy Configuration](https://github.com/deruke/AndroidLabs/blob/main/Labs/LAB_X_Burp-Proxy-Setup/images/burp-configure-listener-1.jpg)

 6. You should now have an active listener in Burp.

 ![Burp Proxy Configuration](https://github.com/deruke/AndroidLabs/blob/main/Labs/LAB_X_Burp-Proxy-Setup/images/burp-proxy-options.jpg)

## Configure the Virtual Mobile Device's Certificate Trust for the Burp Proxy Certifcate Authority (CA) - User-Trust

The following steps will walk you through the installation of Burp's CA certificate to the User-Trust Store on your virtual mobile device in Corellium.

**IMPORTANT:** Starting with Nougat (Android 7.0 - API level 24) certificates installed to the User-Trust store are ignored by default; however, with Corellium's implementation of Android devices, some naitive applications have been "patched" to trust the user cert store. If you are using a different mobile device solution for testing, Android devivces 7.0+ (API >= 24) will require the Burp CA cert to be installed to the System-Trust store (see XXX Lab for adding Burp's CA to the System-Trust on Android devices).  

1.  



