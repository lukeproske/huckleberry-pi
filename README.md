![huckleberry_pi](https://github.com/user-attachments/assets/fd5df14a-06ea-4e48-9721-c578457ffb42)


# Huckleberry Pi
A cheap, easy-to-build Raspberry Pi Handheld Cyberdeck, customized to meet my personal needs. 


# Credits
This design is based on the bumble-berry-pi project by GitHub user samcervantes (https://github.com/samcervantes/bumble-berry-pi). With the help of [@impy2eyes](https://github.com/impy2eyes), I redesigned the case and 3D models from the ground up to better fit my needs. 


# Changes
- To reduce costs, I wanted to use a Raspberry Pi 5 (8GB RAM) that I already owned. The case is specifically designed for a Raspberry Pi 5 and may not work with other variants.
- I tried to find ways to reduce the cost, such as removing the requirement for the threaded inserts. It was also cheaper to purchase a two pack of right angle USB-C adapters rather than buying one and a U-shaped adapter. 
- The case can be easily opened to access the Raspberry Pi if needed. There is also a cover that can be removed to access the GPIO pins.
- The case folds, although this can not be done while the battery is connected. This helps to protect the screen during transportation.


# Parts List

| Part | Link | Notes |
| ----------- | ----------- | ----------- |
| Raspberry Pi 5 | [8 GB](https://www.amazon.com/Raspberry-Pi-8GB-SC1112-Quad-core/dp/B0CK2FCG1K) | Options with more or less ram should work too. The case is designed specifically for the Raspberry Pi 5, so other models will likely not work without modification. |
| Micro SD Card | Many options available on Amazon | I used a 128 GB Micro SD card that I had previously received from a Raspberry Pi kit. |
| Raspberry Pi 5 Active Cooler (fan) | [Amazon](https://www.amazon.com/dp/B0D41NH1S8) | Raspberry Pi 5s need a fan to keep them cool, otherwise performance throttling is likely to occur. |
| FREENOVE 4.3 Inch Touchscreen Monitor (Same as original design) | [Amazon](https://www.amazon.com/dp/B0DDC4KKKF) | This is a decent sized touchscreen monitor for the price. |
| Mini Keyboard | [Amazon](https://www.amazon.com/dp/B0B46F8RS6) | A mini keyboard that is the right size. I was initially concerned about it being Bluetooth, but it seems to work well and removes the need for a dongle. |
| 5V USB Power Bank | [Amazon](https://www.amazon.com/dp/B0CB1FW5FC) | This one only supplies 3A instead of 5A (see Known Issues section), but for most situations it works well. It lasts a long time and has an indicator to show the charge remaining. |
| Two Pack of USB-C Right Angle Adapters | [Amazon](https://www.amazon.com/dp/B0F6MLJ7SP) | To save costs, the case was redesigned so that a two pack of these replace the two different adapters in the original design. |
| 3D Printed Case | See the .stl and .step files | Printed using clear PETG. |


# Operating System
I wanted my version to be able to serve as a portable penetration testing tool to learn ethical hacking. I installed Kali Linux, which has a version for ARM architecture that can be downloaded from their website (https://www.kali.org/) or within the Raspberry Pi Imager. I switched to KDE Plasma for the desktop environment, which works well with the touchscreen.


# Known Issues
- The battery does not fit snugly into the case, making it difficult to press its button. This issue can be fixed by adding a piece of tape as a spacer.
- My print used clear filament. The Raspberry Pi's light will not be visible with opaque filament. 
- The screen works for the booting process but goes black at the login screen. After blindly typing the password, the screen starts working again. This is most likely a software issue caused by Kali Linux, KDE Plasma, or the display manager. I am attempting to discover a solution, but the Cyberdeck is still perfectly usable. For now, lets just call it a "security feature."
- The battery pack can only supply 3 amps when running at 5 volts, but the recommended power for a Raspberry Pi 5 is 5V 5A. For most situations, this does not cause a problem; however, booting from USB devices is disabled and problems may be encountered when high power is needed (such as running USB devices).
- When something is plugged into or unplugged from the battery pack, it renegotiates all connections, causing the Pi to lose power momentarily and shut down unexpectedly. After starting the Pi, do not try to plug or unplug any power connections (including trying to charge the battery) without safely shutting down first.
