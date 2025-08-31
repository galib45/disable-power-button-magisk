# Disable Power Button – Magisk Module
This Magisk module disables the power button by commenting out the relevant key mapping in `/system/usr/keylayout/Generic.kl`. Useful for devices with a faulty power button that triggers unintended presses or long presses.  


## Features
- Disables the power button to prevent accidental shutdowns or screen locks.
- Safe and reversible via Magisk module management.


## Installation
1. **Download the Module:**  
   Go to the [Releases](https://github.com/galib45/disable-power-button-magisk/releases/latest) section and download the latest ZIP file.

2. **Install via Magisk:**
   1. Open the **Magisk Manager** app.  
   2. Tap **Modules** → **Install from storage**.  
   3. Select the downloaded ZIP file.  
   4. Reboot your device.

3. **Verify:**  
   After reboot, pressing the power button should no longer trigger screen on/off or other power button actions.


## How It Works
- The module edits `/system/usr/keylayout/Generic.kl` by commenting out the line responsible for the power button (key code 116).  
- This effectively disables the hardware power button without modifying other system functions.  

**Original line in `Generic.kl`:**
```
key 116 POWER
```
**After module installation:**
```
# key 116 POWER
```

## Removal

1. Open **Magisk Manager** → **Modules**.  
2. Find **Faulty Power Button Fix** in the list.  
3. Tap **Remove** → **Reboot**.  

After reboot, your power button will function as before.  

## Notes
- Only intended for devices with a faulty power button.  
- Ensure you have an alternative way to reboot your device (e.g., ADB or volume key shortcuts) before disabling the power button.  
- This module modifies system key layouts; it may not work on all devices.  

## License
This is free and unencumbered software released into the public domain under [The Unlicense](https://unlicense.org/).
