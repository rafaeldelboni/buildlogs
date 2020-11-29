# foostan's Corne Keyboard ([crkbd v3](https://github.com/foostan/crkbd))

Check the [final product](#finished)

## Check List:
- [x] [Sort the parts](#part-list-original)
- [x] [Install/Configure QMK](#installconfigure-qmk)
- [x] [Compile/Flash Firmware](#compileflash-firmware)
- [x] [Prepare the OLEDS](#prepare-oleds)
- [x] [Prepare the PCB](#prepare-pcb)
- [x] [Solder PCB top components](#solder-pcb-top-components)
- [x] [Solder pro-micro](#solder-pro-micro)
- [x] [Solder OLEDs](#solder-oleds)
- [x] [Solder diodes](#solder-diodes)
- [x] [Solder hot-swaps](#solder-hot-swaps)
- [x] [Solder under-glow leds](#solder-under-glow-leds)
- [x] [Solder per-key leds](#solder-per-key-leds)
- [x] [Mount the case](#mount-the-case)

## Part list ([Original](https://github.com/foostan/crkbd/blob/master/corne-cherry/doc/v3/buildguide_jp.md))

- 1x  Corne PCBs [Printed mine on jlcpcb](https://jlcpcb.com/)
- 1x  Corne Case [Laser cut mine on Brazil](https://www.acrilicos60.com.br/)
- 42x Keycaps - 1u x 40, 1.5u x 2
- 2x  [Pro Micro ATmega32U4 5V/16MHz Module controller Mega32U4 Mini leonardo for Arduino with the bootloader](https://www.aliexpress.com/item/32768308647.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 2x  [OLED 128X32 OLED Display Module 0.91" IIC Communicate for ardunio](https://www.aliexpress.com/item/32777216785.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [Kailh Hot-swappable PCB Socket Sip For Mechanical Keyboard](https://www.aliexpress.com/item/4001051840976.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [SMD diodes 1N4148 SOD-123](https://www.aliexpress.com/item/32916398082.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 1M  [Round Copper Wire 0.5mm](https://www.aliexpress.com/item/4000781904492.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 4x  [2.54mm Pin Header Female Single Row 40](https://www.aliexpress.com/item/32817226478.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 2x  [PJ320D 3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32785315917.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 1x  [1m 4 pole Stero audio cable Car AUX MP3/MP4 3.5mm male to male](https://www.aliexpress.com/item/32459681560.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 2x  [Micro Switch Push Button 3.5X6.0X4.3mm 1136-4.3 DIP Black](https://www.aliexpress.com/item/1068908059.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [Holy Pandas switches](https://www.aliexpress.com/item/1005001465063863.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 24x [Screws M2 6mm](https://www.aliexpress.com/item/32661182311.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 10x [Spacers M2 7mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 4x  [Spacers M2 10mm](https://www.aliexpress.com/item/32970573343.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [Leds SK6812-mini-E](https://www.aliexpress.com/item/4000476037223.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 12x [Leds ws2812b](https://www.aliexpress.com/item/4000750610574.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)

## Firmware

### Install/Configure QMK

First to compile the crkbd qmk firmware you will need to use avr-gcc 8. 

In Arch use the following commands to install the dependencies:
```bash
sudo pacman --needed -U https://archive.archlinux.org/packages/a/avr-gcc/avr-gcc-8.3.0-1-x86_64.pkg.tar.xz
sudo pacman -S --needed \
       arm-none-eabi-binutils \
       arm-none-eabi-gcc \
       arm-none-eabi-newlib \
       avrdude \
       avr-binutils \
       avr-libc \
       base-devel \
       clang \
       dfu-programmer \
       dfu-util \
       diffutils \
       gcc \
       git \
       libusb-compat \
       python \
       python-pip \
       unzip \
       wget \
       zip
```

Then clone the [qmk firmware](https://github.com/qmk/qmk_firmware) and then

### Compile/Flash Firmware

```bash 
make crkbd:default:flash
```

This will compile and start to flash the firmware, make sure your pro-micro is connected in the usb port and the following message will be shown:
```bash
QMK Firmware 0.9.19
WARNING:
 Can not run bin/qmk! This tool will be required when the develop branch is merged on 2020 Aug 29.

 Please run util/qmk_install.sh to install all the dependencies QMK requires.

Making crkbd/rev1 with keymap default and target flash

avr-gcc (GCC) 8.3.0
Copyright (C) 2018 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Size before:
   text    data     bss     dec     hex filename
      0   21574       0   21574    5446 .build/crkbd_rev1_default.hex

Copying crkbd_rev1_default.hex to qmk_firmware folder                                               [OK]
Checking file size of crkbd_rev1_default.hex                                                        [OK]
 * The firmware size is fine - 21574/28672 (75%, 7098 bytes free)
Detecting USB port, reset your controller now..................
```

At this moment, with some tweezers, reset the pro-micro
![Reseting Pro-Micro](/crkbd-v2/01-flashing-the-firmware-1.jpg)

If you did right the following will be shown:
```bash
Device /dev/ttyACM0 has appeared; assuming it is the controller.
Waiting for /dev/ttyACM0 to become writable..

Connecting to programmer: .
Found programmer: Id = "CATERIN"; type = S
    Software Version = 1.0; No Hardware Version given.
Programmer supports auto addr increment.
Programmer supports buffered memory access with buffersize=128 bytes.

Programmer supports the following devices:
    Device code: 0x44

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.00s

avrdude: Device signature = 0x1e9587 (probably m32u4)
avrdude: NOTE: "flash" memory has been specified, an erase cycle will be performed
         To disable this feature, specify the -D option.
avrdude: erasing chip
avrdude: reading input file ".build/crkbd_rev1_default.hex"
avrdude: input file .build/crkbd_rev1_default.hex auto detected as Intel Hex
avrdude: writing flash (21574 bytes):

Writing | ################################################## | 100% 1.64s

avrdude: 21574 bytes of flash written
avrdude: verifying flash memory against .build/crkbd_rev1_default.hex:
avrdude: load data flash data from input file .build/crkbd_rev1_default.hex:
avrdude: input file .build/crkbd_rev1_default.hex auto detected as Intel Hex
avrdude: input file .build/crkbd_rev1_default.hex contains 21574 bytes
avrdude: reading on-chip flash data:

Reading | ################################################## | 100% 0.16s

avrdude: verifying ...
avrdude: 21574 bytes of flash verified

avrdude: safemode: Fuses OK (E:CB, H:D8, L:FF)

avrdude done.  Thank you.
```

Do this for both pro-micros and you good to go.

![Flashing Pro-Micro](/crkbd-v2/01-flashing-the-firmware-2.jpg)

## Building

### Prepare OLEDs

Remove the oleds legs for socketing can be quite challenging, I lost some oleds during this phase.
![Preparing oleds](/crkbd-v3/01-preparing-oled.jpg)

### Prepare PCB

Just cut the the pcb out
![Preparing pcb 1](/crkbd-v3/02-preparing-pcb-01.jpg)

Those conections are ugly let's trim them out.
![Preparing pcb 3](/crkbd-v3/02-preparing-pcb-03.jpg)

I like to paint the sides of the pcb to have a better finish.
![Preparing pcb 4](/crkbd-v3/02-preparing-pcb-04.jpg)
![Preparing pcb 5](/crkbd-v3/02-preparing-pcb-05.jpg)

I used POSCA for painting the pcb sides.
![Preparing pcb 6](/crkbd-v3/02-preparing-pcb-06.jpg)

### Solder PCB top components

An easy thru-hole solder.
![Soldering top pcb 1](/crkbd-v3/03-soldering-top-01.jpg)

I used some masking tape to help me.
![Soldering top pcb 2](/crkbd-v3/03-soldering-top-02.jpg)

Result.
![Soldering top pcb 3](/crkbd-v3/03-soldering-top-03.jpg)

### Solder pro-micro

I used some masking tape to help me organize the wires.
![Soldering pro-micro 1](/crkbd-v3/04-soldering-promicro-01.jpg)

Also another benefit of using masking tape is to don't let the solder go thought the hole and "glue" with the PCB socket.
![Soldering pro-micro 2](/crkbd-v3/04-soldering-promicro-02.jpg)

Result.
![Soldering pro-micro 3](/crkbd-v3/04-soldering-promicro-03.jpg)

### Solder OLEDs

I used isolation tape to separate the led from the pro-micro
![Soldering oled 1](/crkbd-v3/05-soldering-oled-01.jpg)

Same process as the pro-micro.
![Soldering oled 2](/crkbd-v3/05-soldering-oled-02.jpg)

Result.
![Soldering oled 3](/crkbd-v3/05-soldering-oled-03.jpg)

### Solder diodes

The SMD diodes are trick at first, they are pretty small and they have polarity, make sure to match the polarity with PCB.
![Soldering diodes 1](/crkbd-v3/06-soldering-diodes-01.jpg)

To make it easier to solder, first put some solder on one of the PCB diode contacts and then with a tweezer hold the diode over the solder and heat it to stick the diode, proceed to the other diode contact and solder it normally.
![Soldering diodes 2](/crkbd-v3/06-soldering-diodes-02.jpg)

### Solder hot swaps

Very similar to soldering the diodes, but with a way bigger component.
![Soldering hotswap 1](/crkbd-v3/07-soldering-sockets-01.jpg)
![Soldering hotswap 2](/crkbd-v3/07-soldering-sockets-02.jpg)

### Solder under glow leds

All leds have polarity make sure you align your as picured bellow.
![Soldering underleds 1](/crkbd-v3/08-soldering-underleds-01.jpg)

As the diodes, first put some solder on one of the PCB led's contacts and then with a tweezer hold the led over the solder and heat it to stick on the pcb, proceed to the other leds contacts and solder it normally.
![Soldering underleds 2](/crkbd-v3/08-soldering-underleds-02.jpg)

This led is quite challenging to do, be prepared fo some arduous solder job, make sure you have some flux to guide your lead.
![Soldering underleds 3](/crkbd-v3/08-soldering-underleds-03.jpg)

### Solder per-key leds

Exacly as the other leds, this leds also have polarity align as picured bellow.
![Soldering keyleds 1](/crkbd-v3/09-soldering-keyleds-01.jpg)

Result.
![Soldering keyleds 2](/crkbd-v3/09-soldering-keyleds-02.jpg)

### Mount the case

Just some screws and the build was almost finished.
![Mount the case 1](/crkbd-v3/10-case-01.jpg)
![Mount the case 2](/crkbd-v3/10-case-02.jpg)

Adding the switches over the case.
![Mount the case 3](/crkbd-v3/10-case-03.jpg)

### Finished

Some led showoff.  
![Finished 1](/crkbd-v3/11-finished-01.gif)

With the keycaps.
![Finished 2](/crkbd-v3/11-finished-02.jpg)
