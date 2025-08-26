Macro pad 3d design at the following onshape link. Can search by "Pico Macro Pad" if link doesn't work.

https://cad.onshape.com/documents/1c13b9cfaf62a4152e213f5f/w/222868530b7b64143a231dde/e/0a95b26a9c16ad7d8a72cf47?renderMode=0&uiState=68add22a63ec93693a6da6f8

No supports needed for both parts. Print the keypad face down.

Get 4 screws from a hardware store to attach face to the enclosure. M3 or #4 machine screws with fine threads should do the trick. Must be less than 15mm deep, I would suggest around 8-12mm.

-------------------------------------------------------------------------------------------------------

Purchase 16 MX Cherry keys for the switches

Solder the GNDs together (pick one of the two pins, I chose the outter most pin of each switch).

Solder a dupont cable to the remaining pin on each key switch for connecting to the Raspberry pi GPIO pins.

Print 16 Keycaps for the switches. I used the following: https://www.printables.com/model/109679-cherry-mx-low-profile-keycap

---------------------------------------------------------------------------------------------------------

I'm using an Elegoo ESP32 dev board v1 for this. Avoid pin D2 and D34 and up due to issues with the inputs.

Flash initially with a usb cable using the web tool for ESPHome (https://web.esphome.io/?dashboard_install)

Go to home assistant and add the node to esphome

Edit the node and paste the yaml, then hit "Install".

Choose to download directly via the webtool since already plugged in

Can choose to do OTA or wireless if updates are needed later

Go to the ESPhome integration and at the device level, click the Cog and enable
  "Allow the device to perform Home Assistant actions.
  When enabled, ESPHome devices can perform Home Assistant actions, such as calling services or sending events. Only enable this if you trust the device."

