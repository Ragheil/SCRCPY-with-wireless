# 📱 SCRCPY-with-wireless

![GitHub repo size](https://img.shields.io/github/repo-size/Ragheil/SCRCPY-with-wireless?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/Ragheil/SCRCPY-with-wireless?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/Ragheil/SCRCPY-with-wireless?style=for-the-badge)
![GitHub license](https://img.shields.io/github/license/Ragheil/SCRCPY-with-wireless?style=for-the-badge)

> A simple Windows bundle of [scrcpy](https://github.com/Genymobile/scrcpy) that supports **wireless screen mirroring** between your Android device and your PC.

---

## 🧭 Table of Contents
- [Overview](#-overview)
- [Features](#-features)
- [Requirements](#-requirements)
- [Installation](#-installation)
- [Wireless Setup](#-wireless-setup)
- [Usage](#-usage)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)
- [FAQ](#-faq)
- [Credits](#-credits)

---

## 🧐 Overview

**SCRCPY-with-wireless** is a pre-packaged version of **scrcpy** for Windows users who want to easily set up **wireless Android screen mirroring** without complex ADB commands.

The repository includes:
- `scrcpy.exe`, `adb.exe`, and related binaries
- Batch scripts for easy setup
- Quick launch tools for both **USB** and **Wi-Fi** modes

After a one-time setup using USB, you can control and mirror your Android device **wirelessly** over Wi-Fi.

---

## ✨ Features

✅ Wireless screen mirroring (no USB needed after setup)  
✅ Easy-to-use batch scripts (`.bat`)  
✅ No installation required — portable & ready-to-use  
✅ Built-in ADB & scrcpy binaries  
✅ Supports video mirroring and input control via mouse/keyboard  

---

## ⚙️ Requirements

To use SCRCPY-with-wireless, you need:

- 🪟 **Windows 10/11 (64-bit)**  
- 📱 **Android device** with:
  - Developer Options enabled  
  - **USB Debugging** enabled  
  - **Wireless Debugging** (Android 11+) enabled  
- 🌐 Both PC and phone connected to the **same Wi-Fi network**

---

## 🧩 Installation

1. **Download or clone this repository:**
   ```bash
   git clone https://github.com/Ragheil/SCRCPY-with-wireless.git
   ```
   Or download the ZIP and extract it.

2. Navigate to the extracted folder (for example: scrcpy-win64-v2.7).

3. (Optional) Check out the included batch scripts:
   - `scrcpy-wireless-setup.bat`
   - `scrcpy-wireless-connect.bat`
   - `open_a_terminal_here.bat`

4. Connect your phone via USB for the initial setup.

---

## 📶 Wireless Setup

On your Android device:

- Go to Settings → Developer Options
- Enable:
  - ✅ USB Debugging
  - ✅ Wireless Debugging (if available)
- Find your phone’s IP address:
  - Usually in Settings → About Phone → Status → IP Address.

On your PC:

1. Open the project folder.
2. Run:
   ```bash
   scrcpy-wireless-setup.bat
   ```
   Follow the prompts to enable ADB over TCP/IP.
3. Then run:
   ```bash
   scrcpy-wireless-connect.bat
   ```
   Enter your device IP address when prompted.

If successful, your Android screen will appear on your PC — wirelessly!

---

## 🖥️ Usage

After setup, you can use SCRCPY wirelessly anytime:

Run:
```bash
scrcpy-wireless-connect.bat
```
Enter your device’s IP when prompted.

The mirrored screen will appear on your PC.

You can interact with your phone using:

🖱️ Mouse for touch control  
⌨️ Keyboard for typing and shortcuts

Example (manual command):
```bash
scrcpy.exe --tcpip=<device-ip>
```

---

## 🧰 Troubleshooting

### ❌ Device not found / Connection refused
- Ensure both devices are on the same Wi-Fi network.
- Disable client isolation (some routers block peer-to-peer connections).
- Check if Wireless Debugging is still active on your phone.
- Reconnect via USB and re-enable TCP/IP mode with:
  ```bash
  adb tcpip 5555
  adb connect <device-ip>:5555
  ```

### ⚠️ High latency or lag
- Use a 5GHz Wi-Fi network instead of 2.4GHz.
- Reduce resolution or bitrate:
  ```bash
  scrcpy.exe --max-size 1024 --bit-rate 4M
  ```

### 🧩 Common Issues
- Firewall: Allow ADB and scrcpy through Windows Firewall.
- Dynamic IP: Your device IP might change—set a static IP in router settings.
- Permissions: Run batch files as Administrator if needed.
- No video: Try reconnecting or rebooting your phone and PC.

💡 Tip: Always verify USB mirroring works before enabling wireless mode.

---

## 🤝 Contributing

Contributions are welcome!  
If you’d like to help improve this repository:

1. Fork the repo  
2. Make your changes  
3. Submit a Pull Request  

Please ensure your updates are:
- Tested on Windows 10/11  
- Compatible with multiple Android versions  
- Documented clearly in the README  

---

## 📜 License

This project builds on scrcpy by Romain Vimont and contributors.  
Please check the LICENSE file for the exact license and redistribution terms.

---

## ❓ FAQ

**Q:** Do I still need USB after setup?  
**A:** Only for the initial pairing. After that, Wi-Fi is enough.

**Q:** Why can’t my PC find the device IP?  
**A:** Make sure both are on the same Wi-Fi network and Wireless Debugging is enabled.

**Q:** Does this mirror audio too?  
**A:** No, scrcpy mirrors only video and input. For audio, use other apps such as SoundWire or AudioRelay.

**Q:** Will this work on macOS or Linux?  
**A:** This bundle is designed for Windows (Win64). Use the original scrcpy for other platforms.

**Q:** Is the mirrored screen interactive?  
**A:** Yes! You can control your device with mouse and keyboard—click, type, drag, etc.

---

## ⭐ Credits

- Genymobile/scrcpy — Core project  
- Android Open Source Project  
- Ragheil — Packaging and Windows wireless setup scripts  

🧡 If this project helps you, consider giving it a ⭐ on GitHub!

