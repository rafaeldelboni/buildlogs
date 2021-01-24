# omkbd's ErgoDash Keyboard [No leds] ([ErgoDash v1.2](https://github.com/omkbd/ErgoDash))

Check the [final product](#finished)  
Check the [original buildlog](https://github.com/omkbd/ErgoDash/blob/master/Doc/build-en.md)

## Check List:
- [x] [Sort the parts](#part-list-original)
- [x] [Ordering the PCB](#ordering-the-pcb)
- [x] [Firmware](#firmware)
- [x] [Prepare the PCB](#prepare-pcb)
- [x] [Solder diodes](#solder-diodes)
- [x] [Solder botton components](#solder-botton-components)
- [x] [Jumper Pads](#jumper-pads)
- [x] [Install Stabilizer](#install-stabilizer)
- [x] [Install Top-Plate](#install-top-plate)
- [x] [Solder Switches](#solder-switches)
- [x] [Solder pro-micro](#solder-pro-micro)
- [x] [Install Botton-Plate](#install-botton-plate)

## Part list ([Original](https://github.com/omkbd/ErgoDash/blob/master/Doc/Shoplist_JP.md))

- 1x  ErgoDash PCBs [Printed mine on jlcpcb](https://jlcpcb.com/)
- 1x  ErgoDash Case [Laser cut mine on Brazil](https://www.acrilicos60.com.br/)
- 70x Keycaps - 1u x 68, 2u x 2
- 2x  [Pro Micro ATmega32U4 5V/16MHz Module controller Mega32U4 Mini leonardo for Arduino with the bootloader](https://www.aliexpress.com/item/32768308647.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 70x [Thru-hole diodes IN4148 DO-35](https://www.aliexpress.com/item/32881432301.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)
- 2x  [Momentary Tactile Switch 3X6X4.3 with stand](https://www.aliexpress.com/item/1068889297.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)
- 2x  [PJ320D 3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32785315917.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 1x  [1m 4 pole Stero audio cable Car AUX MP3/MP4 3.5mm male to male](https://www.aliexpress.com/item/32459681560.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 70x [Holy Pandas switches](https://www.aliexpress.com/item/1005001465063863.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 2x  [Stabilizers 2u PCB Stab](https://www.aliexpress.com/item/32864774665.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)
- 22x [M2×5mm Screws](https://www.aliexpress.com/item/33055570766.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)
- 6x  [M2×5mm Screws](https://www.aliexpress.com/item/33055570766.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)
- 6x  [M2×8mm Spacer](https://www.aliexpress.com/item/4001231387908.html?spm=a2g0s.9042311.0.0.70084c4dCbGJQc)

![Sorting Parts](/ergo-dash-v1.2/01-sort-parts-01.jpg)

## Ordering the PCB

I pretty much uploaded the [latest cherry gerber file avalilable on omkbd's repository](https://github.com/omkbd/ErgoDash/blob/master/PCB/Rev1.2/gerber/ergodash.zip) in https://jlcpcb.com and let all defaults settings.
Later I receiced an email complaing about some fragilities the holes could cause, I asked then to kindly just proceed because I wasn't planning to use that part of the thumbcluste, [I opened an issue about this problem](https://github.com/omkbd/ErgoDash/issues/39), but after asking then to proceed everything was ok.


## Firmware

You can follow pretty much what I did for the corne keyboard [here](https://github.com/rafaeldelboni/buildlogs/blob/main/crkbd-v3.md#installconfigure-qmk)
Just swap the command for Compile/Flash the firmware with this one:

```bash 
make ergodash/rev1:default:flash
```

## Building

### Prepare the PCB

Removed the thumbclusters with my own hands carefully.
![Sorting Parts](/ergo-dash-v1.2/02-remove-extra-thumb-01.jpg)

I used POSCA for painting the pcb sides.
![Sorting Parts 2](/ergo-dash-v1.2/03-detailing-pcb-01.jpg)

### Solder diodes
![Diodes 1](/ergo-dash-v1.2/04-diodes-01.jpg)
![Diodes 2](/ergo-dash-v1.2/04-diodes-02.jpg)
![Diodes 3](/ergo-dash-v1.2/04-diodes-03.jpg)
![Diodes 4](/ergo-dash-v1.2/04-diodes-04.jpg)
![Diodes 5](/ergo-dash-v1.2/04-diodes-05.jpg)

### Solder botton components
![Soldering botton components 1](/ergo-dash-v1.2/05-soldering-botton-components-01.jpg)
![Soldering botton components 2](/ergo-dash-v1.2/05-soldering-botton-components-02.jpg)
![Soldering botton components 3](/ergo-dash-v1.2/05-soldering-botton-components-03.jpg)

### Jumper Pads
![Jumper pads](/ergo-dash-v1.2/06-jumper-pads-01.jpg)

### Install Stabilizer
![Stabilizers 1](/ergo-dash-v1.2/07-stabilizer-01.jpg)
![Stabilizers 2](/ergo-dash-v1.2/07-stabilizer-02.jpg)
![Stabilizers 3](/ergo-dash-v1.2/07-stabilizer-03.jpg)

### Install Top-Plate
![Top Plate 1](/ergo-dash-v1.2/08-top-plate-01.jpg)
![Top Plate 2](/ergo-dash-v1.2/08-top-plate-02.jpg)

### Solder Switches
![Switches 1](/ergo-dash-v1.2/09-switches-01.jpg)
![Switches 2](/ergo-dash-v1.2/09-switches-02.jpg)
![Switches 3](/ergo-dash-v1.2/09-switches-03.jpg)

### Solder pro-micro
![Promicros](/ergo-dash-v1.2/10-pro-micro-01.jpg)

### Install Botton-Plate
![Botton Plate 1](/ergo-dash-v1.2/11-botton-plate-01.jpg)
![Botton Plate 2](/ergo-dash-v1.2/11-botton-plate-02.jpg)
![Botton Plate 3](/ergo-dash-v1.2/11-botton-plate-03.jpg)

### Finished
![Finished](/ergo-dash-v1.2/12-final-01.jpg)
