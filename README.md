# KlipperOS
Welcome to the KlipperOS Live USB!

I created this to simplify klipper setup and avoid having to purchase a pi.
***Please read all of the directions below before you begin!***
Enjoy! :)

## Download
**All ISO and checksum (md5) files are found at [sourceforge.net/projects/klipperos/files/releases/](https://sourceforge.net/projects/klipperos/files/releases/)**\
(ISO files are too large to host on GitHub)
## 
Some basic information:
- Built using [Cubic](https://github.com/PJ-Singh-001/Cubic) (Unfortunately, the full directory for editing is too large to host) 
- Klipper and Moonraker services are installed and will start automatically
- The desktop shortcuts may display a warning each time they are opened. Just mark them as executable when prompted, and that will stop.
- Moonraker configuration is stored in /home/ubuntu/config
- The other configuration files are found in their default spots
- You do **NOT** need to install Ubuntu as the live OS has file persistence
- If you do install Ubuntu, the klipper files will **NOT** transfer, so only use it if you wish to add Ubuntu to your computer for other reasons

USB Requirements

- Capacity: At least 64gb, although 128gb is recommended
- At least 100MB/s read (high write speeds tend to come with that)
- Good heat dispersion, since the USB will get really warm quickly
- I used the SanDisk 128GB Ultra Flair USB 3.0 Flash Drive - SDCZ73-128G-G46 ($16.99 on [Amazon](https://www.amazon.com/SanDisk-Ultra-Flair-128GB-Flash/dp/B015CH1PJU?th=1))

Creating the USB

1. Download Rufus from rufus.ie or the microsoft store
2. It should automatically detect and select the USB drive, but one can be selected in the "Device" box
3. Under the "Boot selection" section, click SELECT and open the KlipperOS ISO
4. Under that, use the slider to allocate persistent storage (I recommend at least 20gb)
5. In the "Partition scheme" box, select either MBR or GPT
5a. GPT and NTFS is preferred, since it will boot without input; however, MBR will work better with older BIOS systems
5b. During an MBR boot, you will hit an error page about how the device is not a typewriter. Just type exit and press enter
6. Leave everything else the defaults and click START
7. Click through any warnings about data deletion on the USB

Quick-Start Guide

1. Connect to the internet using the Wi-Fi icon in the top right
2. Open Kiauh using the desktop shortcut
3. Use Kiauh to install Mainsail or Fluidd (whichever web interface you prefer)\
   3a. Type 1 into the preform action box, then press enter\
   3b. Then, type 3 or 4, depending on which interface you would like\
   3c. Reply Y to any requests about example/default configurations\
   3d. Use any port you need or the default (by pressing enter with no value typed)\
4. Copy the resulting IP (with the port attached)
5. Open the "Update Klipper IP" desktop shortcut and paste it in when prompted
6. Open the "Web Interface" shortcut, and you should see a working interface
7. Build and flash firmware to your printer's mainboard:\
   7a. Type 4 into Kiauh to open advanced settings, then type 1 for "[Build]"\
   7b. Find your boards example printer.cfg at [bit.ly/exampleconfigs](https://bit.ly/exampleconfigs)\
   7c. In the GUI, enter the firmware flashing settings found at the top of your example\
   7d. Save and quit that menu and wait for the firmware to build\
8. Each mainboard has its own particular way to flash, so follow one of the many tutorials online for your board
9. Use Kiauh to get the MCU ID once connected to the flashed printer mainboard\
   9a. Type 4 to open advanced settings, then type 4 again for "Get MCU ID"\
   9b. Reply with your connection method\
10. Open the default printer.cfg in your web interface and replace `<your-mcu-id>` with the output ID
11. Continue to develop your printer.cfg to match your printer using parts of the example you found earlier\
    11a. I recommend finding a printer.cfg tutorial online for your printer in addition to your example\
12. Enjoy your new klipper printer!

Feel free to contact me with any questions on the GitHub or at maxrosenthal712@gmail.com
