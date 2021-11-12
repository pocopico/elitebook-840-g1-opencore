# Elitebook 840 G1 Haswell,  Opencore 0.7.5

Confirmed to be working with Big Sur 11.6.1


# What Works :

- UEFI booting via OpenCore
- Dual Boot with Windows/Linux
- Built-in keyboard (with special function keys)
- Built-in trackpad (Multi-Gestures)
- Native WiFi & Bluetooth via ITLMW
- HDMI Audio/Video with hot-plug
- Native USB3 with AppleUSBXHCI using USBMap (USB2 works also)
- Native audio, including headphone
- Built-in mic
- Built-in camera
- Native power management
- Battery status
- Backlight controls with smooth transitions
- Accelerated graphics Intel HD Graphics 4400
- Wired Ethernet
- App Store
- iMessage & Facetime


# Hardware:

CPU: Intel(R) i5-4300U (Haswell)
SSD: Samsung SSD 860 EVO 500GB
RAM: 8GB DDR3
DISPLAY: 1600x900 (Touchscreen)
GPU: Integrated, Intel HD Graphics 4400
AUDIO CODEC: IDT92HD91BXX
ETHERNET: Intel I218-LM
WIFI: Intel Wi-Fi Drivers are NOW compatible for macOS, check itlwm.

# BIOS Settings:

- Disable

* Fast Boot
* Secure Boot
* Serial/COM Port
* Disable wake on USB
* Parallel Port
* VT-d (can be enabled if you set DisableIoMapper to YES)
* CSM
* Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
* Intel SGX
* Intel Platform Trust
* CFG Lock (This must be off, otherwise your hack will not boot with CFG-Lock enabled) if you can't find the option then enable AppleXcpmCfgLock under:

>     Kernel -> Quirks -> AppleXcpmCfgLock=True

- Enable

* VT-x

* Above 4G decoding
* Hyper-Threading
* Execute Disable Bit
* EHCI/XHCI Hand-off
* OS type: Windows 8.1/10 UEFI Mode
* DVMT Pre-Allocated(iGPU Memory): 64MB
* SATA Mode: AHCI
* Note: Most of these options may not be present in your firmware, we recommend matching up as closely as possible but don't be too concerned if many of these options are not available in your BIOS.

** Save and reboot in UEFI. **

# Credit:

- Apple for MacOS
- vit9696 for OpenCore
- Dortania's Guide for OpenCore Install
- InsanelyMac's OpenCore forums for finding issues with hardware and their work arounds
- RehabMan for DSDT-Patches
- itlwm Intel Wi-Fi Drivers for macOS
