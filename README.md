# ESP32 Provisioning: Enhanced HTML <a href="https://www.ohioiot.com"><img src="https://www.ohioiot.com/images/logo.jpg" width="40" ></a>


## Overview
This code serves is an output from the YouTube video [ESP32 Provisioning - Enhanced HTML](https://youtu.be/UBM_KC4RHlo).  👉 Subscribe to the [OhioIoT YouTube Channel](https://www.youtube.com/@OhioIoT?sub_confirmation=1) for more on All Things IoT: hardware, firmware, connectivity, cloud computing, and dev toolkit.


## Getting Started
```
git clone https://github.com/OhioIoT-ESP32-Provisioning-Examples/Enhanced-HTML.git
```


### Getting Started - PlatformIO
- Compile and run

### Getting Started - Arduino IDE 
- copy ***/src/main.cpp*** into a new sketch ***prov_lab/prov_lab.ino*** (or whatever name you choose) in your Arduino projects folder
- copy the ***lib/provisioner*** folder into your ***libraries/*** folder in your Arduino projects folder
- Compile and run


## About
*OhioIoT is an IoT platform designed for small-scale IoT projects (https://www.ohioiot.com).*


## Updates

**10/17/25** - Adding some logging when the provisioner starts

**10/18/25** - WiFi.begin() will put the WiFi in WIFI_STA mode automatically if it comes from WIFI_OFF.  However, if the device is coming from WIFI_AP mode, WiFi.begin() will apparently put it in WIFI_AP_STA mode, and leave the DEVICE_PROVISIONING SSID active.  So, best to explicitly call WiFi.mode(WIFI_STA) before WiFi.begin() (see _src/main.cpp_).  