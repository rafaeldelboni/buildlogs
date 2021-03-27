# rtitmuss's Torn Keyboard ([torn v3](https://github.com/rtitmuss/torn))

Check the [video of this build](https://youtu.be/7WUTQ30Datw)  
Check the [final product](#finished)  

## Check List:
- [x] [Sort the parts](#part-list-original)
- [x] [Ordering the PCB](#ordering-the-pcb)
- [x] [Solder diodes](#solder-diodes)
- [x] [Solder resistors](#solder-resistors)
- [x] [Solder zenner diodes](#solder-zenner-diodes)
- [x] [Solder Electrolytic capacitor](#solder-electrolytic-capacitor)
- [x] [Solder capacitors](#solder-capacitors)
- [x] [Solder crystal oscillator](#solder-crystal-oscillator)
- [x] [Solder fuse](#solder-fuse)
- [x] [Solder leds](#solder-leds)
- [x] [Solder reset buttons](#solder-reset-buttons)
- [x] [Solder IC sockets](#solder-ic-sockets)
- [x] [Solder TRRS jacks](#solder-trrs-jacks)
- [x] [Solder USBC jack](#solder-usbc-jack)
- [x] [Inserting ICs](#inserting-ics)
- [x] [Solder oled](#solder-oled)
- [x] [Install/Configure QMK](#installconfigure-qmk)
- [x] [Burn Bootloader](#burn-bootloader)
- [x] [Compile/Flash Firmware](#compileflash-firmware)
- [x] [Solder hot-swaps](#solder-hot-swaps)
- [x] [Solder rotary encoders](#solder-rotary-encoders)
- [x] [Mount the case](#mount-the-case)

## Part list ([Original](https://github.com/foostan/crkbd/blob/master/corne-cherry/doc/v3/buildguide_jp.md))

- 1x  [Torn PCBs](https://github.com/rtitmuss/torn/releases) Printed mine on [jlcpcb](https://jlcpcb.com/)
- 1x  [Torn Case](https://github.com/rtitmuss/torn/releases) Printed mine on [jlcpcb](https://jlcpcb.com/)
- 1x  [Torn Plate](https://github.com/rtitmuss/torn/blob/master/case/cover.dxf) Laser cut mine on [Brazil](https://www.acrilicos60.com.br/)
- 42x [Keycaps - 1u x 42](https://ohkeycaps.com/)
- 42x [Holy Pandas switches](https://www.aliexpress.com/item/1005001465063863.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [Kailh Hot-swappable PCB Socket Sip For Mechanical Keyboard](https://www.aliexpress.com/item/4001051840976.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 42x [Diodes 1N4148](https://www.aliexpress.com/item/32881432301.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 2x  [Diodes Zenner 3V6](https://www.aliexpress.com/item/4000841629104.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 2x  [Ceramic Capacitor 22pf](https://www.aliexpress.com/item/33047488252.html?spm=2114.12010615.8148356.45.a2d16c53lp1R9b)
- 3x  [Ceramic Capacitor 100nf](https://www.aliexpress.com/item/33047488252.html?spm=2114.12010615.8148356.45.a2d16c53lp1R9b)
- 1x  [Electrolytic Capacitor 4.7uf](https://www.aliexpress.com/item/32508909501.html?spm=a2g0o.productlist.0.0.28ab629c5HTmoN)
- 1x  [Fuse MF-R050](https://www.aliexpress.com/item/4001303234450.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 1x  [16MHz Crystal Oscillator](https://www.aliexpress.com/item/33047492067.html?spm=2114.12010615.8148356.1.27005d64EJaZ58)
- 1x  [MCP23017 DIP-28](https://www.aliexpress.com/item/33042254423.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 1x  [ATMEGA328P DIP-28](https://www.aliexpress.com/item/32963157048.html?spm=2114.12010615.8148356.3.24e93275FP9aeD)
- 2x  [DIP-28 Socket](https://www.aliexpress.com/item/32869251296.html?spm=a2g0o.productlist.0.0.8e862b99V3bQ13)
- 1x  [1.5k Resistor](https://www.aliexpress.com/item/1005001443193845.html?spm=a2g0o.productlist.0.0.5d4e5d62psXV2a)
- 2x  [75R Resistor](https://www.aliexpress.com/item/1005001443193845.html?spm=a2g0o.productlist.0.0.5d4e5d62psXV2a)
- 1x  [10k Resistor](https://www.aliexpress.com/item/1005001443193845.html?spm=a2g0o.productlist.0.0.5d4e5d62psXV2a)
- 5x  [5.1k Resistor](https://www.aliexpress.com/item/1005001443193845.html?spm=a2g0o.productlist.0.0.5d4e5d62psXV2a)
- 2x  [2.2k Resistor](https://www.aliexpress.com/item/1005001443193845.html?spm=a2g0o.productlist.0.0.5d4e5d62psXV2a)
- 3x  [Leds](https://www.aliexpress.com/item/4000043090015.html?spm=a2g0o.productlist.0.0.3e4048cfmUDc6K)
- 2x  [Push Button H 4.5MM + 6X6mm DIP Series](https://www.aliexpress.com/item/1058764733.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 2x  [Rotary Encoders 15mm](https://www.aliexpress.com/item/4000326517211.html?spm=a2g0o.productlist.0.0.7dfa4d4584SH2c)
- 2x  [Knobs](https://www.aliexpress.com/item/4000686931568.html?spm=a2g0s.9042311.0.0.27424c4d0oYTk1)
- 1x  [OLED 128X32 OLED Display Module 0.91" IIC Communicate for ardunio](https://www.aliexpress.com/item/32777216785.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 2x  [3.5MM Headphone TRRS Jack Socket Female Connector](https://www.aliexpress.com/item/32811541166.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 1x  [USB Type-C 3.1 Receptacle 16 Pin DIP Female Socket](https://www.aliexpress.com/item/4000967090640.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 4x  [2.54mm Pin Header Female Single Row 40](https://www.aliexpress.com/item/32817226478.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 1x  [1m 4 pole Stero audio cable Car AUX MP3/MP4 3.5mm male to male](https://www.aliexpress.com/item/32459681560.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 10x [Spacers M2 3mm Female-Female](https://www.aliexpress.com/item/33051228617.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 6x  [Spacers M2 8mm Female-Female](https://www.aliexpress.com/item/33051228617.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 16x [Spacers M2 3mm Male-Female](https://www.aliexpress.com/item/33051228617.html?spm=a2g0s.9042311.0.0.27424c4dH9gzJt)
- 6x  [Screws M2 6mm](https://www.aliexpress.com/item/32661182311.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)
- 26x [Screws M2 4mm](https://www.aliexpress.com/item/32661182311.html?spm=a2g0s.9042311.0.0.27424c4dlrgRjA)

![Parts](/torn-v3/01-sort-parts-01.jpg)

### Ordering the PCB

I really recomend jlcpcb service for this, the process is straight forward and you just need to download the precompiled gerber [here](https://github.com/rtitmuss/torn/releases), upload, select your color and you good to go.  
_In the gerber link you can find the gerber for the pcb and the top and down plates for the case._

### Solder diodes
**This part has a specific orientation**, the black bar on the diode goes on the squared hole.
![Diodes 1](/torn-v3/03-diodes-01.jpg)

Apart from the orientation, this component is very straight forward.
![Diodes 2](/torn-v3/03-diodes-02.jpg)

After clipping the legs, this is how the back of the PCB should looks like.
![Diodes 3](/torn-v3/03-diodes-03.jpg)

### Solder resistors
First I soldered all 5.1k resistors. (Green - Brown - Red)
![Resistors 1](/torn-v3/04-resistors-01.jpg)

2 goes in the PCB of the left side and other 3 on the PCB of the right.
![Resistors 2](/torn-v3/04-resistors-02.jpg)

Then I moved to the 2.2k resistors. (Red - Red - Red)
![Resistors 3](/torn-v3/04-resistors-03.jpg)

The lonely 10k resistor of this build. (Brown - Black - Orange)
![Resistors 4](/torn-v3/04-resistors-04.jpg)

The progress so far.
![Resistors 5](/torn-v3/04-resistors-05.jpg)

The fancy two 75R resistors. (Purple - Green - Black)
![Resistors 6](/torn-v3/04-resistors-06.jpg)

Progress with the 1.5k resistor. (Brown - Green - Red)
![Resistors 7](/torn-v3/04-resistors-07.jpg)

### Solder zenner diodes
**This part has a specific orientation**, the black bar on the diode goes on the squared hole.
![Zenner Diodes 1](/torn-v3/05-zenner-diodes-01.jpg)

Both zenners soldered.
![Zenner Diodes 2](/torn-v3/05-zenner-diodes-02.jpg)

The progress so far.
![Zenner Diodes 3](/torn-v3/05-zenner-diodes-03.jpg)

### Solder Electrolytic capacitor
**This part has a specific orientation**, the longer leg goes on the squared hole.
![Electrolytic Capacitor 1](/torn-v3/07-electrolytic-capacitor-01.jpg)

Insert the capacitor and fold it until it touches the PCB.
![Electrolytic Capacitor 2](/torn-v3/07-electrolytic-capacitor-02.jpg)

### Solder capacitors
Ceramic capacitor don't have specific orientation, just insert the two 22pF in the holes.
![Ceramic Capacitors 1](/torn-v3/08-ceramic-capacitors-01.jpg)

The three 100nf capacitors (yellow) in both PCBs.
![Ceramic Capacitors 2](/torn-v3/08-ceramic-capacitors-02.jpg)

The progress so far.
![Ceramic Capacitors 3](/torn-v3/08-ceramic-capacitors-03.jpg)

### Solder crystal oscillator
The crystal don't have specific orientation.
![Crystal Oscillator 1](/torn-v3/09-crystal-oscillator-01.jpg)

### Solder fuse
The fuse don't have specific orientation, insert the fuse and fold it until it touches the PCB.
![Fuse 1](/torn-v3/10-fuse-01.jpg)

### Solder leds
**This part has a specific orientation**, the shorter leg goes on the squared hole.
![Leds 1](/torn-v3/11-leds-01.jpg)

Soldered LEDs.
![Leds 2](/torn-v3/11-leds-02.jpg)

### Solder reset buttons
The reset/boot buttons don't have specific orientation.
![Reset Buttons 1](/torn-v3/12-reset-buttons.jpg)

### Solder IC sockets
**This part has a specific orientation**, the notch on the IC sockets must be pointing UP.
![Sockets DIP-28 1](/torn-v3/13-sockets-01.jpg)

Close up on the sockets installed.
![Sockets DIP-28 2](/torn-v3/13-sockets-02.jpg)

### Solder TRRS jacks
This TRRS jack that I found in Aliexpress has some extra legs.
![TRRS 1](/torn-v3/14-trrs-jacks-01.jpg)

I had to remove the extra legs marked in the red circle.
![TRRS 2](/torn-v3/14-trrs-jacks-02.jpg)

Soldered jacks.
![TRRS 3](/torn-v3/14-trrs-jacks-03.jpg)

The progress so far.
![TRRS 4](/torn-v3/14-trrs-jacks-04.jpg)

### Solder USBC jack
One of the hardest parts of this build, I just used a lot of flux and small amount of solder and the drag technique.
![USBC 1](/torn-v3/15-usbc-jack-01.jpg)

Detail on the soldering of the port pins, some will bridge because the traces and is fine.
![USBC 2](/torn-v3/15-usbc-jack-02.jpg)

### Inserting ICs
Just push the IC in the sockets mind the that the notch needs to be pointing UP.
![ICs 1](/torn-v3/16-inserting-cis-01.jpg)

ATMEGA328P on the left and MCP23017 in the right.
![ICs 2](/torn-v3/16-inserting-cis-02.jpg)

### Solder oled
This part is optional, but is very cool.
![OLED 1](/torn-v3/17-oleds-01.jpg)

### Install/Configure QMK

To install the [qmk firmware](https://github.com/qmk/qmk_firmware) do the following:
```bash
# Clone
git clone https://github.com/qmk/qmk_firmware.git
cd  qmk_firmware
./util/qmk_install.sh
```
For more information and troubleshooting check the [official documents](https://docs.qmk.fm/#/newbs_getting_started)

### Burn Bootloader
For this part I highly recommend to to follow the [official build log](https://github.com/rtitmuss/torn/blob/master/doc/bootloader.md)

Cables connected in Torn's ICSP:
 - Green is on pin 1
 - Red is on pin 2
 - White is on pin 3
 - Orange is on pin 4
 - Blue is on pin 5
 - Blue is on pin 6

![Bootloader 1](/torn-v3/18-burning-bootloader-01.jpg)

Cables connected in Arduino's ICSP:
 - Green is on pin 1
 - Red is on pin 2
 - White is on pin 3
 - Orange is on pin 4
 - nothing pin 5
 - Blue is on pin 6

![Bootloader 2](/torn-v3/18-burning-bootloader-02.jpg)

The Pin 10 is connected to Torn ICSP pin 5.
![Bootloader 3](/torn-v3/18-burning-bootloader-03.jpg)

This protoboard is optional I used to debug the flashing process more information about it [here](https://www.arduino.cc/en/Tutorial/BuiltInExamples/ArduinoISP/#loadthesketch)
![Bootloader 4](/torn-v3/18-burning-bootloader-04.jpg)

Pins GND, 9, 8 and 7 going to the protoboard.
![Bootloader 5](/torn-v3/18-burning-bootloader-05.jpg)

The hole setup.
![Bootloader 6](/torn-v3/18-burning-bootloader-06.jpg)

### Compile/Flash Firmware
First enter bootloader mode by:
 - Plug in the TRRS cable to connect the left and right sides for the keyboard
 - Plug in USB C cable between the keyboard and your PC
 - Push and hold RESET SW
 - Push and hold BOOT SW
 - Release RESET SW
 - Release BOOT SW

You can then program QMK using:
```bash 
sudo make torn:default:flash
```

### Solder hot-swaps
First put some solder in one of the pads.
![Hotswaps 1](/torn-v3/19-kailh-hotswap-01.jpg)

Then insert the hot-swaps and pressing down with your finger heat the solder applied before in the pad, you will feel that the hotswap moving down.
![Hotswaps 2](/torn-v3/19-kailh-hotswap-02.jpg)

Finish soldering the other side.
![Hotswaps 3](/torn-v3/19-kailh-hotswap-03.jpg)

### Solder rotary encoders
The rotary encoder has two legs that I need to remove.
![Rotary Encoders 1](/torn-v3/20-rotary-encoder-01.jpg)

Yeap, those ones. I bended then before cutting off.
![Rotary Encoders 2](/torn-v3/20-rotary-encoder-02.jpg)

As recommended in the official build guide, I applied some insulation surrounding the encoder.
![Rotary Encoders 3](/torn-v3/20-rotary-encoder-03.jpg)

The PCB with the rotary encoder soldered.
![Rotary Encoders 4](/torn-v3/20-rotary-encoder-04.jpg)

You can solder the encoder any time, because they pass thought the top case plate.
![Rotary Encoders 5](/torn-v3/20-rotary-encoder-05.jpg)

Encoder touches the plate, that's why you need the insulation.
![Rotary Encoders 6](/torn-v3/20-rotary-encoder-06.jpg)

### Mount the case
You need to make a sandwich with a female-male 3mm spacer + PCB + female-female 3mm spacer.
![Case 1](/torn-v3/21-case-01.jpg)

Detail on the bottom plate, as you can see I forgot one screw in the top right.
![Case 2](/torn-v3/21-case-02.jpg)

Left PCB with Top and bottom plates installed.
![Case 3](/torn-v3/21-case-03.jpg)

The progress so far.
![Case 4](/torn-v3/21-case-04.jpg)

### Finished
Some glamour shoots for the finished build, I loved building this keyboard and it will be my daily driver.
![Finished 1](/torn-v3/22-finished-01.jpg)

Some of my father's resin artisans.
![Finished 2](/torn-v3/22-finished-02.jpg)

My crkbd, will definitely retire.
![Finished 3](/torn-v3/22-finished-03.jpg)

Another father's artisan.
![Finished 4](/torn-v3/22-finished-04.jpg)

I dunno if will ever user the encoders, but they look cool.
![Finished 5](/torn-v3/22-finished-05.jpg)
