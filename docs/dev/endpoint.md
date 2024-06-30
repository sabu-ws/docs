# Endpoint
!!! warning "Warning"

    The configurations described on this page were carried out on the **Raspbian** distribution.

## Login with custom account
```bash
nano /etc/lightdm/lightdm.conf
```
```bash
Set autologin-user customUSer (Remplace customUser)
```
Reboot your endpoint
!!! tip "Link"

    Source : [https://forums.raspberrypi.com/viewtopic.php?t=113617](https://forums.raspberrypi.com/viewtopic.php?t=113617)

## Chromium at startup
```bash
nano ~/.config/wayfire.ini
```
```bash
[autostart]
chromium = chromium-browser https://www.google.com --kiosk --noerrdialogs --disable-infobars --no-first-run --ozone-platform=wayland --enable-features=OverlayScrollbar --start-maximized
screensaver = false
dpms = false
```
!!! tip "Link"

    Source : [https://gist.github.com/rampfox/085bf3ffb9ff51e114bf7afdf3ced71b](https://gist.github.com/rampfox/085bf3ffb9ff51e114bf7afdf3ced71b)

## Touchscreen Raspberry Pi
- Method #1
```bash
nano ~/.config/wayfire.ini
```
```bash
[output:DSI-1]
mode = 800x480@60029
position = 0,0
transform = 180
```

- Method #2
```bash
nano /boot/firmware/config.txt
```
```bash
# For more options and information see
# http://rptl.io/configtxt
# Some settings may impact device functionality. See link above for details

# Uncomment some or all of these to enable the optional hardware interfaces
#dtparam=i2c_arm=on
#dtparam=i2s=on
#dtparam=spi=on

# Enable audio (loads snd_bcm2835)
dtparam=audio=on

# Additional overlays and parameters are documented
# /boot/firmware/overlays/README

# Automatically load overlays for detected cameras
camera_auto_detect=1

# Automatically load overlays for detected DSI displays
display_auto_detect=1

# Automatically load initramfs files, if found
auto_initramfs=1

# Enable DRM VC4 V3D driver
dtoverlay=vc4-kms-dsi-7inch
#dtoverlay=vc4-kms-dsi-7inch,sizex=400,invx,invy
dtoverlay=vc4-kms-v3d
max_framebuffers=2

# Don't have the firmware create an initial video= setting in cmdline.txt.
# Use the kernel's default instead.
disable_fw_kms_setup=1

# Run in 64-bit mode
arm_64bit=1

# Disable compensation for displays with overscan
disable_overscan=1

# Run as fast as firmware / board allows
arm_boost=1

[cm4]
# Enable host mode on the 2711 built-in XHCI USB controller.
# This line should be removed if the legacy DWC2 controller is required
# (e.g. for USB device mode) or if USB support is not required.
otg_mode=1

[all]

lcd_rotate=2
```
!!! tip "Link"

    Source : [https://howchoo.com/pi/raspberry-pi-display-rotation/](https://howchoo.com/pi/raspberry-pi-display-rotation/)
