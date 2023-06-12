# Introduction 🗣️
This is a very interesting tablet, especially for those who are not familiar with it. It is one of the rare devices that exclusively have 32-bit UEFI without legacy BIOS, which makes it a bit challenging to install anything that isn't specifically designed for it. While 32-bit distros and 32-bit Windows seem to work well, you're here because you're looking for something different, right?

## Hardware
- HOST: Dell Venue 8 Pro 3845
- CPU: Intel Atom Z3735G (4) @ 1.832GHz 🐌
- GPU: Not provided by neofetch :/
- RAM: 1GB 😲
- RES: 800x1280
- STORAGE: 32GB internal eMMC + SD card reader (NOT BOOTABLE, DO NOT TRY 😠)

## Requirements for tomfoolery 
- Micro-USB to USB adapter
- USB splitter/hub
- USB stick of at least 4GB, but preferably more
- Brain (only a little, don't worry)

# Distros I've tried 📖
To be honest, I haven't tried many. I attempted PostmarketOS, Android x86 (didn't work for me), and Debian (could have installed it if desired). I have heard that Fedora is a good option, but I haven't personally tested it.

# Booting USB 💾
Figuring out how to boot from USB isn't easy, but it's not difficult either. Here are the steps:
1. Plug in the adapter, hub, USB stick, and any other USB accessories you want.
2. Press and hold the Windows button on the side, then press the power button for a few seconds.
3. Release the Windows button and quickly press the volume up button.
4. Read the text on the screen and select the option with "USB" in its name.
5. Profit?

# Installing 64-bit Distros
It's relatively simple. You just need to have [bootia32.efi](https://raw.githubusercontent.com/lamadotcare/bootia32-efi/main/bootia32.efi) in your boot partition, and everything *should* work. Alternatively, you can try to find a 32-bit distro, but good luck with that.

# Installing PostmarketOS ‼️‼️‼️
1. Install [pmbootstrap](https://wiki.postmarketos.org/wiki/Pmbootstrap).
2. Run `pmbootstrap init` with options from [config.txt](config.txt).
3. Run `pmbootstrap install --sdcard=/dev/sdc`, replacing `sdc` with your USB device.
4. Boot the USB on the tablet.
5. Establish network, then repeat steps 1-3 ON THE TABLET, but set `--sdcard=/dev/mmcblkX` (without the SD card inserted, it will be the only one).
6. Use `shutdown` from the system to ensure the flashing process finishes.
7. Profit?

## Additional Notes on PostmarketOS 📝
As of now, not everything works or works well on PostmarketOS. I intend to contribute and improve some aspects, but I cannot make any promises. Getting it to function at all was a combined effort between me and @craftyguy on the PostmarketOS matrix.

I don't have a specific TODO list yet, but I would like to make the power button work normally, enable auto-rotation, and maybe get the cameras functioning. However, no promises.
