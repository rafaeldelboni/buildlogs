# foostan's Corne Keyboard ([crkbd v2](https://github.com/foostan/crkbd))

Check the [final product](#final-product)  
Check the [video of this build](https://www.youtube.com/watch?v=-E7KRnVCjq8)

## Check List:
- [x] [Sort the parts](#part-list-original)
- [x] [Install/Configure QMK](#installconfigure-qmk)
- [x] [Compile/Flash Firmware](#compileflash-firmware)
- [x] [Mark pcbs side (left/right)](#mark-pcbs-sides)
- [x] [Solder OLED jumper pads](#solder-oled-jumper-pads)
- [x] [Soldering Pin Sockets (pro-micro/oled)](#soldering-pin-sockets)
- [x] [Solder diodes](#solder-diodes)
- [x] [Prepare copper wire to be the new pro-micro/OLED male pin](#prepare-copper-wire-to-be-the-new-pro-microoled-male-pin)
- [x] [Solder pro-micro male sockets "legs"](#solder-pro-micro-male-sockets-legs)
- [x] [Rewire oled socket with new "legs"](#rewire-oled-socket-with-new-legs)
- [x] [Solder TRRS](#solder-trrs)
- [x] [Manual test](#manual-test)
- [x] [Solder reset](#solder-reset)
- [x] [Solder hot-swaps](#solder-hot-swaps)
- [x] [Mount the case](#mount-the-case)
- [x] [(optional) Wood Wristrest](#optional-wood-wristrest)

## Part list ([Original](https://github.com/foostan/crkbd/blob/master/corne-classic/doc/buildguide_en.md))

- 2x  [Corne PCBs](https://keycapsss.com/keyboard-parts/pcb/53/crkbd-split-keyboard-corne-helidox-pcb-mini-e-version)
- 1x  [Corne Case](https://keycapsss.com/keyboard-parts/cases/69/corne-split-keyboard-crkbd-helidox-acrylic-plate-case)
- 2x  [Pro Micro ATmega32U4 5V/16MHz Module controller Mega32U4 Mini leonardo for Arduino with the bootloader](https://www.aliexpress.com/item/32842943705.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 2x  [OLED 128X32 OLED Display Module 0.91" IIC Communicate for ardunio](https://www.aliexpress.com/item/32672229793.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 42x [Kailh Hot-swappable PCB Socket Sip For Mechanical Keyboard](https://www.aliexpress.com/item/32951252318.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 42x [SMD diodes 1N4148 SOD-123](https://www.aliexpress.com/item/32916398082.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 1M  [Round Copper Wire 0.5mm](https://www.aliexpress.com/item/4000781904492.html?spm=a2g0o.productlist.0.0.770947e0Wl8ukF)
- 4x  [2.54mm Pin Header Female Single Row 40](https://www.aliexpress.com/item/32817226478.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 2x  [PJ320D 3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32785315917.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 1x  [1m 4 pole Stero audio cable Car AUX MP3/MP4 3.5mm male to male](https://www.aliexpress.com/item/32459681560.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 2x  [Micro Switch Push Button 3.5X6.0X4.3mm 1136-4.3 DIP Black](https://www.aliexpress.com/item/1068908059.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 42x [Zilents V2 Blue switches 67g](https://www.aliexpress.com/item/33048985466.html?spm=a2g0s.9042311.0.0.76fd4c4dCaERgB)
- 42x Keycaps - 1u x 40, 1.5u x 2

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

### Mark pcbs sides

This is self explanatory, but is very helpfull to mark your pcbs sides.

![Marking Pcbs](/crkbd-v2/02-marking-pcb-sides.jpg)

### Solder OLED jumper pads

You need to solder the oled jumper pads in order to use oleds.
![OLED jumper pads](/crkbd-v2/02-jumper-oled-1.jpg)

### Soldering Pin Sockets 

I had to double check sometimes to see if I was soldering in the right side of the pcb, that's why marking the pcbs before helps a lot thought the process.
![Pin Connetors 1](/crkbd-v2/03-soldering-pin-connector-1.jpg)
The other problem I had was that the PCB is designed to work in both sides, so you have 2 sets of holes to solder your pro micro, the trick to know which hole to use is use the ones that are inside a white box line looking from above.
![Pin Connetors 2](/crkbd-v2/03-soldering-pin-connector-2.jpg)
From bellow the holes are passing thought the white line.
![Pin Connetors 3](/crkbd-v2/03-soldering-pin-connector-3.jpg)

### Solder diodes

The SMD diodes are trick at first, they are pretty small and they have polarity, make sure to match the polarity with PCB.
![Solder diodes 1](/crkbd-v2/04-soldering-diodes-1.jpg)

To make it easier to solder, first put some solder on one of the PCB diode contacts and then with a tweezer hold the diode over the solder and heat it to stick the diode, proceed to the other diode contact and solder it normally.
![Solder diodes 2](/crkbd-v2/04-soldering-diodes-2.jpg)

All diodes soldered.
![Solder diodes 3](/crkbd-v2/04-soldering-diodes-3.jpg)

On both PCBs
![Solder diodes 4](/crkbd-v2/04-soldering-diodes-4.jpg)

### Prepare copper wire to be the new pro-micro/OLED male pin

Instead of using thru-hole diode legs for this step, I experimented doing the male pin legs with some 0.5mm copper wire, the only down side doing this is that the copper wire I bought came covered with a thin plastic layer that I had to remove in order to make it electrical conductor.
![Pro copper legs 1](/crkbd-v2/05-copper-wire-pin-1.jpg)

Left wire is the one I sanded out the plastic compared with how it came on the right.
![Pro copper legs 2](/crkbd-v2/05-copper-wire-pin-2.jpg)

I used some masking tape to help me organize the wires.
![Pro copper legs 3](/crkbd-v2/05-copper-wire-pin-3.jpg)

### Solder pro-micro male sockets "legs"

Also another benefit of using masking tape is to don't let the solder go thought the hole and "glue" with the PCB socket.
![Solder pro-micro male 1](/crkbd-v2/06-soldering-pro-micro-1.jpg)

Is a good idea to use some solder flux on the copper wires to help with the soldering
![Solder pro-micro male 2](/crkbd-v2/06-soldering-pro-micro-2.jpg)

On both PCBs
![Solder pro-micro male 3](/crkbd-v2/06-soldering-pro-micro-3.jpg)

### Rewire oled socket with new "legs"

This was the hardest part of all project, de-soldering the OLED current pins without a good solder sucker wasn't a good idea. 
![Rewire oled 1](/crkbd-v2/10-soldering-oled-1.jpg)

I was so frustrated with the results that I forgot to take pictures of this process.
![Rewire oled 2](/crkbd-v2/10-soldering-oled-2.jpg)

### Solder TRRS

An easy thru-hole solder, just had to straight the component legs before.
![Soldering TTRS 1](/crkbd-v2/07-soldering-ttrs-jack-1.jpg)

Result from above.
![Soldering TTRS 2](/crkbd-v2/07-soldering-ttrs-jack-2.jpg)

### Manual test

At this moment I had enough to setup a manual test, to check if all I did until here was ok.
![Manual Test 1](/crkbd-v2/08-first-testing-1.jpg)

I when to [keyboardtester](https://www.keyboardtester.com) and plugged the new keyboard to the PC.
![Manual Test 2](/crkbd-v2/08-first-testing-2.jpg)

I simulated the switch behaviour with the tweezer.
![Manual Test 3](/crkbd-v2/08-first-testing-3.jpg)

### Solder reset

Again an easy step, just had to straight the component legs before.
![Soldering reset 1](/crkbd-v2/09-soldering-reset-button-1.jpg)

Result from above.
![Soldering reset 2](/crkbd-v2/09-soldering-reset-button-2.jpg)

### Solder hot-swaps

Very similar to soldering the diodes, but with a way bigger component.
![Solder hot-swaps](/crkbd-v2/11-soldering-kailh-hotswap-1.jpg)

### Mount the case

Just some screws and the build was almost finished.
![Mount the case 1](/crkbd-v2/12-mounting-case-1.jpg)

Adding the switches over the case.
![Mount the case 2](/crkbd-v2/12-mounting-switches-1.jpg)

Checking if all is working before the keycaps
![Mount the case 3](/crkbd-v2/12-mounting-switches-2.jpg)

#### Final product
![Final](/crkbd-v2/13-mounting-keycaps-1.jpg)

### (optional) Wood Wristrest

I asked my father to create some wristrest for this project.
![Wood Wristrest 1](/crkbd-v2/14-finished-wood-writesrest-1.jpg)

I didn't made much in this step, but just helped him as an assistant, maybe in the future I will have enough wood skill to do so.
![Wood Wristrest 2](/crkbd-v2/14-finished-wood-writesrest-2.jpg)
