# Lenovo Yoga 7 Pro - Linux Configuration

## IMPORTANT NOTICE: The internal microphone is not detected with this setup, I'm searching for a fix. Avoid using this configuration if you need audio input.

Here you will find some configuration files to have a fully working Linux setup, on the Lenovo Yoga 7 Pro (serial: 14IRH8).

The most important fix is related to the audio part: without the options in `intel-sound-fix.conf`, I wasn't able to adjust the volume on my PC, it was 100% or none, no middle values.

The video part was working OK, but I noticed that the `xe` driver wasn't loaded, so I did that as well. If you encounter any video problems, just remove `/etc/modules-load.d/intel-video-xe.conf` from your system, and reboot.

## Hardware

- CPU: 13th Gen Intel® Core™ i7-13700H × 20
- GPU: Intel® Iris® Xe Graphics (RPL-P rev 04) 
- Audio: Realtek ALC3306 (detected as ALC287) 
- Wi-Fi: Intel Corporation Raptor Lake PCH CNVi WiFi (rev 01)
- Bluetooth: Intel Corp. AX211 Bluetooth

## Tested setup:

- Fedora 42 Workstation (kernel version: Linux 6.16.7-200.fc42.x86_64)
- Gnome 48 (Wayland) - Stock version
- BIOS Version: LWCN33WW (latest available on 09/24/2025)

## How to use

Configuration files are arranged in a folder structure similar to the one of a common linux install.

Just run these commands:

- `sudo cp etc/modprobe.d/* /etc/modprobe.d`
- `sudo cp etc/modules-load.d/* /etc/modules-load.d`

And **reboot** your computer. Done!

---

Hopefully this will help you to have a fully working Linux PC. This model had some issues, but now I'm glad everything is working beautifully (camera included!).
