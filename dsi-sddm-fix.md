# DSI Touchscreen Black Screen at SDDM Login (Raspberry Pi 5 / KDE Plasma)

On Raspberry Pi 5 with a DSI touchscreen and KDE Plasma, the touchscreen may go black at the SDDM login screen but work fine once logged in. This is because SDDM's X11 greeter doesn't automatically initialize the DSI display.

## Fix

**1. Create the SDDM Xsetup script:**

```bash
sudo nano /etc/sddm/Xsetup
```

Add the following:

```bash
#!/bin/sh
xrandr --output DSI-1-1 --auto --primary
xset s off
xset -dpms
xset s noblank
```

Make it executable:

```bash
sudo chmod +x /etc/sddm/Xsetup
```

**2. Configure SDDM to use X11 and the Xsetup script:**

```bash
sudo nano /etc/sddm.conf.d/kde_settings.conf
```

Add these lines to the end (keep any existing lines like the theme setting):

```ini
[General]
DisplayServer=x11

[X11]
DisplayCommand=/etc/sddm/Xsetup
```

**3. Reboot.**

## Notes

- The output name `DSI-1-1` is what xrandr uses during the SDDM greeter. Once logged in, the same display may appear as `DSI-1`.
- This fix forces SDDM's greeter to run on X11. You can still choose between Wayland and X11 for your actual session at the login screen.
- For my touchscreen, some of the icons on the login/greeter screens are slightly cut off (such as the change user button).
