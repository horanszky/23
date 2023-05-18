# 23
Armbian vs  tvbox

Armbian [Debian desktop Linux with XFCE] vs. allwinner/amlogic/rockchip tvbox with Android

Tv box with Android, and "Discreet Launcher", with a normal launcher good for streaming, gaming, but the resolution not good for desktop computing.
This low energy device with lan/bluetooth/wifi/audio/"4K" is like a cheap, silent, ideal tiny client pc with Armbian Linux + LibreOffice, Firefox ESR, Telegram.. on XFCE lightweight desktop environment.

U can touch this - it's Hammer time!

[Lookout, Armbian is pink, use Dark-Olympic theme after instalation!]
[few storage? use clouds: megasync, filen, skiff..]

1. Etcher img burner [balena, AppImage] + mSD card + Armbian*.img

2. rename: u-boot* to u-boot.ext
[mSD /BOOT/]

3. edit /BOOT/extlinux/extlinux.conf with texteditor
example:
FDT /dtb/amlogic/frankójankó.dtb
#FDT /dtb/amlogic/nem frankójankó.dtb

4. The DTB
[DeviceTree Compiler (DTC), device tree blob (DTB), device tree source (DTS), device tree overlay (DTO)]

dtb sources:

I. burned Armbian version's /BOOT/dtb/ folder
or

II. attached zip's - not the zip's, extract..
[Armbian_19, Armbian_2010, Armbian_2108, Armbian_2302, EmuELEC_42, EmuELEC_43]
or

III. root/dev/dtb.img from Android with root file explorer [FX?]
[dd if=/dev/dtb | gzip > /*/*/dtb.img.gz]
or

IV. dtc in CLI
dtc -I fs -o x.dtb /sys/firmware/devicetree/base
dtc -I fs -O dtb /sys/firmware/devicetree/base -o x.dtb
dtc -I dts -O dtb -o x.dtb x.dts
dtc -I dts -O dtb -f x.dts -o x.dtb
[pk install dtc, sudo apt-get install dtc]
or

V. 
extract-dtb /sys/firmware/devicetree/base -o /*/*/x
[pk install extract-dtb, sudo apt-get install extract-dtb]


___dtb/Amlogic chip name scheme:

gxbb > s905
gxl > s905x
g12a > s905x2
g12b > s922x
gxm > s912
sm1 > s905x3

___OS name scheme:

Armbian 23.02.1 (23-02-25)..
Armbian 22.11.4 (23-01-23)..
Armbian 22.02 (22-02-28)..
Armbian 21.08 (21-08-31)..
Armbian 21.02.1 (21-02-03)..
Armbian 20.11 (20-11-24)..
Armbian 20.08.22 (20-11-8)..

Debian 14 forky
Debian 13 trixie
Debian 12 bookworm 
Debian 11 bullseye
Debian 10 buster
Debian 9 stretch

Ubuntu 22.04 LTS Jammy Jellyfish 22-04-21
Ubuntu 20.04 LTS Focal Fossa 20-04-23
Ubuntu 18.04 LTS Bionic Beaver 18-04-26
Ubuntu 16.04 LTS Xenial Xerus 16-04-21



