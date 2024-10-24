**Wireless Setup Flow for scrcpy, ensure the device is connected to the same Wi-Fi network as the computer.**

Enable **Developer Options**

**On the device, navigate to Developer Options**
  -Turn on USB Debugging.
  -Turn on Wireless Debugging.

**On the device, go to Settings → About Phone → Status or Network to find the IP Address.**
  -Obtain Device IP Address

**Open scrcpy-win64-v2.7 folder**
  -Run the command: scrcpy-wireless-connect.
  -When prompted, type the device IP Address.
  
  -Connection Established

The device should now be mirrored on the computer using scrcpy.
