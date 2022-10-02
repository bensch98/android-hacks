# Android Hacks

This repo contains some useful stuff to dig into Android.

## Prepare Smartphone

Steps:
1. Enable developer mode: *Settings > About phone > Software information > Build number* (tap 7 times)
2. Configure developer options: *Settings > Developer options*
  - Toggle **On**
  - Toggle *USB Debugging* **On**
  - Toggle *Wireless Debugging* **On**
3. Connect device via USB to PC

## ADB

Install adb: 
```bash
sudo apt-get install android-tools-adb
adb devices
adb tcpip 5555
adb devices
```
The output lists all connected devices
```txt
List of devices attached
192.168.0.3:5555        device
```

Run interactive shell:
```bash
adb connect 192.168.0.3
# the smartphone is now registered -> unplug the USB cable of the smartphone 
adb shell
> ols:/ $
```

After doing all the work run:
```bash
adb disconnect
adb kill-server
```

## Root Smarphone

