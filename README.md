# wLED_ESP32_S2
A quick tutorial on how to setup an ESP32-S2 with WLED and audio reactive usermod from scratch.
## Overview

Required components:
1. ESP32-S2
2. USB-C Cable
3. USB power adapter

## Setup

1. Download the firmware "ESP32-S2 (4MB Flash, with Audio reactive Usermod)" from [WLED Software Installation](https://wled-install.github.io/) and save the *.bin
2. Open the [Tasmota online installer](https://tasmota.github.io/install/)  in a chrome based broser (e.g. Chromium, if not already available `sudo apt-get install chromium`)
3. On the Tasmota website hit "connect", a window with ports should open
4. Press and hold the "0" button on the ESP32-S2 and only then connect it to the PC, "ESP32-S2" should become available as a connection, select it and hit "Connect"
![Screenshot of a popup](https://github.com/adruino-io/wLED_ESP32_S2/blob/main/wled_tutorial.png)
5. In the "Device Dashboard" select "Install Tasmota"
![Screenshot of device dashboard](https://github.com/adruino-io/wLED_ESP32_S2/blob/main/wled_tutorial_3.png)
6. Select "Erase device", proceed with "NEXT" and "Confirm Installation" with "INSTALL", wait until the installer is finished
7. Close the "Device Dashboard" via "X"
8. Unplug the ESP32-S2 and plug it into an USB power supply, scan for WIFI networks and connect to "tasmota-*****"
9. Open a browser and connect to the ip "192.168.4.1", then connect the ESP32 with your network.
![Screenshot connecting the ESP32 to network](https://github.com/adruino-io/wLED_ESP32_S2/blob/main/wled_tutorial_6.png)
10. Wait for reconnection and select the "Firmware Upgrade" tab, use the "Use file upload" to upload the *.bin file
![Screenshot of uploading modified firmware](https://github.com/adruino-io/wLED_ESP32_S2/blob/main/wled_tutorial_8.png)
12. Start the upgrade with "Start upgrade", until a "success screen" is shown.
![Screenshot of success screen](https://github.com/adruino-io/wLED_ESP32_S2/blob/main/wled_tutorial_10.png)
13. The ESP32-S2 should now disconnect. If a "WLED-AP" WIFI network becomes available the flashing was successfull
14. Connect to "WLED-AP" with the default password "wled1234" and resume with configuring the ESP32

## FAQ

1. Why not simply use the tasmota online tool to upload the *.bin directly? -> tried but did not work
2. Why not simply upload the firmware in step 9. before connecting to the network? -> tried but this failed due to memory constraints
