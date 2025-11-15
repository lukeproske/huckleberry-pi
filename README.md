![bumbleberry-1-small](https://github.com/user-attachments/assets/0861c220-9c7e-4fc5-81a6-36195ce6dd99)

[Youtube Video - How To Assemble the Bumble Berry Pi](https://www.youtube.com/watch?v=gBCb1FS4pzc)

# Bumble Berry Pi
A cheap, easy-to-build Raspberry Pi Handheld Cyberdeck

# Why Another Cyberdeck?
- I wanted a Clockwork Pi uConsole, but didn’t want to wait 90 business days
- I like the tactile feeling of a mini keyboard
- I wanted something small enough to fit into a pants pocket, so I can easily take it anywhere, but with a large enough screen to do useful things like writing little programs, running scripts, etc
- I wanted to build this quickly & cheaply, with as many off-the-shelf components as possible
- I mostly boot to the terminal interface (using tmux to manage mutliple terminal windows), but I occasionally use the GUI
- I wanted to use the Raspberry Pi's I already owned (i.e. an old 3b+), rather than having to buy a new compute module

# Key Features
- 4.3” Touch Screen Display
- Nice sized QWERTY keypad
- 37 Watt-hour battery (all day battery life with Raspberry Pi 3b+)
- Only 2 3D-Printed Parts
- Able to use a Rapsberry Pi that you probably already own
- Quick & easy to assemble (~5 minutes excluding 3D printing time): [Assembly Video](https://www.youtube.com/watch?v=gBCb1FS4pzc)
- All parts available on Amazon (excluding 3D printed parts)
- Cost: ~$60 worth of Amazon parts, not including the raspberry pi, bolts, & kapton tape.

# Parts List
*As an Amazon Associate I earn from qualifying purchases*
| Part | QTY | Cost | Buy Link | Notes |
| ----------- | ----------- | ----------- | ----------- | ----------- |
| Raspberry Pi | 1 | $53-$87 | [Pi 3b+](https://amzn.to/48danKa), [Pi 4](https://amzn.to/4oCPuxP), or [Pi 5](https://amzn.to/4hYrimS) | Pick your favorite Pi Model. I personally prefer a 3b+ for low cost and low power usage because I mostly use terminal and only occasionally use the GUI. |
| SD Card | 1 | $20 | [Amazon](https://amzn.to/3LFhqTe) | In case you don't already have one lying around |
| 4.3” Touch Screen Display | 1 | $38 | [Amazon](https://amzn.to/43xmWNH) | This Freenove screen has a nice bright display and is pretty durable |
| Mini Bluetooth keyboard | 1 | $23 | [Amazon](https://amzn.to/4oGfgkX) | This connects via bluetooth to the pi minimize the cabling required |
| 37 Watt-Hr USB Power Bank | 1 | $19 | [Amazon](https://amzn.to/3LCkwY6) | Includes a short USB-C power cable |
| USB-C to Micro-USB U-Shaped Adapter | 1 | $10 | [Amazon](https://amzn.to/49fzCMZ) | This comes in a variety-pack, however, you only need one specific part. You could probably find a cheaper one. |
| USB-C Right Angle Adapter | 1 | $9 | [Amazon](https://amzn.to/4oeygGd) | You could probably find a cheaper one, but this one looks nice |
| M3x10mm Countersunk Head Bolt | 6 | $6 per pack of 50 | [Amazon](https://amzn.to/4oQzWH2) |  |
| M2.5x8mm Socket Head Bolt | 4 | $6 per pack of 50| [Amazon](https://amzn.to/4pdl6Kn) |  |
| M3 Threaded Inserts | 6 | $7 per pack of 100 | [Amazon](https://amzn.to/4nOlhul) |  |
| 2" Kapton Tape | 1 ft | $12 per 100ft roll | [Amazon](https://amzn.to/4qZJdhe) | I prefer Kapton tape, although you could use another type of double-sided tape |
| bumble-berry-pi-enclosure-A-v3.STL | 1 |  | [Github](https://github.com/samcervantes/bumble-berry-pi/blob/main/bumble-berry-pi-enclosure-A-v3.STL) | Download from this repo an print on a 3D printer using PLA |
| bumble-berry-pi-enclosure-B-v3.STL | 1 |  | [Github](https://github.com/samcervantes/bumble-berry-pi/blob/main/bumble-berry-pi-enclosure-B-v3.STL) | Download from this repo an print on a 3D printer using PLA |


# Tools Required
- Small phillips screw driver
- M2.5mm hex driver
- Soldering iron
- Scissors

# Assembly Instructions - Videos
1. First, install the threaded inserts into the front enclosure part A. I forgot to include this in my assembly video below, so here is a generic video on how to install threaded inserts into a 3D printed part: [Youtube Video - How To Install Threaded Inserts](https://www.youtube.com/shorts/iar6NPHNPfY)
2. [Youtube Video - How To Assemble the Bumble Berry Pi](https://www.youtube.com/watch?v=gBCb1FS4pzc)

# Assembly Instructions - Detailed
1. 3D print the two enclosure parts in PLA
2. Insert the 6 threaded inserts using a soldering iron (I always love this part). If you haven't done this before, here is a short youtube video showing how: [Youtube Video - How To Install Threaded Inserts](https://www.youtube.com/shorts/iar6NPHNPfY)
3. Attach the raspberry pi to the screen using 4 phillips screws
4. Plug the ribbon cable into the rapsberry pi & display
5. Attach the screen to the front enclosure (Part A) using 4 M2.5x6mm socket head bolts
6. Attach the usb-c power cable to the rapsberry pi USB-micro power connector using the 180deg USB-C to USB-micro adapter. Route the USB-C cable through the side port as shown in the video.
7. Attach the 90deg USB-C adapter to the end of the power cable
8. Place the front enclosure (Part A) face down on the table and insert the keyboard
9. Add a piece of double-sided kapton tape to the back of the keyboard
10. Place the USB power bank in the front enclosure in the proper orientation so that the battery status indicator will be visible through the hole in the back panel (Part A)
11. Add a piece of double-sided kapton tape to the back of the power bank
12. Screw the enclosure back (Part B) onto the enclosure front (Part A)using 6 M3x10mm countersunk head bolts

# Setup instructions
Note: You might find it helpful to plug in an external USB keyboard to the Pi for the initial setup
1. Install Raspberry PI OS onto an SD card using the [Raspberry Pi Imager](https://www.raspberrypi.com/software/). I recommend Raspberry Pi OS with Raspberry Pi Desktop
2. Insert the SD card into the Raspberry Pi and power-on the pi by plugging in the USB-C power cable into the power bank
3. Using the desktop interface, pair your Bluetooth keyboard to the Pi
4. Connect your pi to the wifi network
5. If you're using a Rapsberry Pi 3b+, I recommend setting your Pi to boot to command line in raspbi-config

# Design Notes
I designed the 3D parts in Solidworks. Let me know if you're interested in the modifying the design and I can post the solidworks files.

<img width="500" alt="BumbleBerryPi" src="https://github.com/user-attachments/assets/aef40629-dcd0-4ca7-b8af-2083a04ff01f" />

