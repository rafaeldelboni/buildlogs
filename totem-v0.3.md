# GEIST's TOTEM Keyboard ([TOTEM](https://github.com/GEIGEIGEIST/TOTEM))

Check the [official build guide](https://github.com/GEIGEIGEIST/TOTEM/blob/main/docs/buildguide.md)  
Check the [final product](#finished)  

## Tools Used

| Name               | Count | Remarks |
|:------------------ |:----- |:------- |
| Soldering Iron     | 01    | CXG 110WT - https://www.aliexpress.com/item/33031529555.html |
| Solder wire        | 01    | Sn63/Pb37 - 1.0mm - https://www.aliexpress.com/item/1005002646781061.html |
| Multimeter         | 01    | https://www.aliexpress.com/item/4000991575808.html |
| Flux Soldering Pen | 01    | https://www.aliexpress.com/item/32908270559.html |
| Tweezers           | 01    | https://www.aliexpress.com/item/1005006596532239.html |

![01-tools-used](/crkbd-choco-v2.1.0/01-tools-used.png)

## Part List

### Required

| Name            | Count | Remarks |
|:--------------- |:----- |:------- |
| TOTEM PCB       | 01    | You can find the files for it [here](https://github.com/GEIGEIGEIST/TOTEM/tree/main/PCB) |
| Seeed XIAO      | 02    | NRF52840 - https://www.aliexpress.com/item/1005004459618789.html |
| Diodes 1N4148W  | 38    | SOD123 - https://www.aliexpress.com/item/32921490945.html |
| reset button    | 02    | Alps SKHLLCA010 - https://www.aliexpress.com/item/1005004288216606.html|
| power switch    | 02    | MSK12C02 - https://www.aliexpress.com/item/1005003308186629.html |
| Lipo battery    | 02    | There is space for a 15 x 22 x 7.5 mm battery |
| USB-C cable     | 01    | Any will work for connecting the keyboard to your PC |
| Choc key switch | 38    | Kailh Choc - https://chosfox.com/products/kailh-chocs?variant=42514647777474 |
| Hotswap socket  | 38    | Hotswap Kailh choc - https://chosfox.com/products/kailh-choc-switch-1350-hot-swap-sockets?variant=42699465621698 |
| 1u Choc keycaps | 38    | https://chosfox.com/products/chocfox-cfx-choc-keycaps?variant=42171505377474 |

### 3DP CASE PARTS

| Part name                 | Count | Remarks |
| :------------------------ | :---- | :------ |
| 3D printed case           | 02    | Find the case files [here](https://github.com/GEIGEIGEIST/TOTEM/tree/main/case) |
| 6mm M2 standoffs          | 08    | https://www.aliexpress.com/item/1005006049595637.html |
| 6mm M2 countersunk screws | 16    | https://www.aliexpress.com/item/1005002365855820.html |
| 8.5mm rubber feet         | 08    | https://www.aliexpress.com/item/1005002618681200.html |

## PCB Preparation
After breaking the PCBs, you will see some burrs that I like to sand off with some sandpaper.
![02-prep-pcb-01](/totem-v0.3/02-prep-pcb-01.jpg)
![02-prep-pcb-02](/totem-v0.3/02-prep-pcb-02.jpg)
I usually do the extra step and paint the edges using a Posca pen.
![02-prep-pcb-03](/totem-v0.3/02-prep-pcb-03.jpg)

## Diodes
Pay attention to the diode orientation, the diodes have some lines indicating their side, that you will align with the line in the PCB.
![03-diode-01](/totem-v0.3/03-diode-01.jpg)
First, add some solder to one of the pads.
![03-diode-02](/totem-v0.3/03-diode-02.jpg)
Then with the tweezers hold the diode over the pad with solder and heat it until the diode is secure.
![03-diode-03](/totem-v0.3/03-diode-03.jpg)
Move the other pad and add solder.
![03-diode-04](/totem-v0.3/03-diode-04.jpg)
All diodes are soldered.
![03-diode-05](/totem-v0.3/03-diode-05.jpg)
I was building 2 keyboards, and here is the current state of the builds.
![03-diode-06](/totem-v0.3/03-diode-06.jpg)
Don't be like me and don't forget those two diodes on the other side of the PCB.
![03-diode-07](/totem-v0.3/03-diode-07.jpg)

## Hotswap
If you planning to use the 3D printed case keep in mind that the hot swaps have an orientation that can impact when you assemble the case later.
![04-hotswap-01](/totem-v0.3/04-hotswap-01.jpg)
The process is the same for the diodes, add solder to one of the pads.
![04-hotswap-02](/totem-v0.3/04-hotswap-02.jpg)
Then hold the hot-swap over the pad and heat the solder until it's secure in place.
![04-hotswap-03](/totem-v0.3/04-hotswap-03.jpg)
Solder the other pad.
![04-hotswap-04](/totem-v0.3/04-hotswap-04.jpg)
All hot swap soldered.
![04-hotswap-05](/totem-v0.3/04-hotswap-05.jpg)
The current state of the builds.
![04-hotswap-06](/totem-v0.3/04-hotswap-06.jpg)

## Power Toggle
For this step, I recommend using flux for the small pins.
![05-power-switch-01](/totem-v0.3/05-power-switch-01.jpg)
Hold in place with the tweezers and solder the side pads first.
![05-power-switch-02](/totem-v0.3/05-power-switch-02.jpg)
With some flux, a small tip solder iron, and patience solder the three pins left.
![05-power-switch-03](/totem-v0.3/05-power-switch-03.jpg)
All toggles soldered
![05-power-switch-04](/totem-v0.3/05-power-switch-04.jpg)
The current state of the builds.
![05-power-switch-05](/totem-v0.3/05-power-switch-05.jpg)

## Reset Switch
Insert the reset in the PCB.
![06-reset-01](/totem-v0.3/06-reset-01.jpg)
If you planning to use the 3D-printed case, you will need to keep this vertically aligned with the PCB.
![06-reset-02](/totem-v0.3/06-reset-02.jpg)
Solder the pins.
![06-reset-03](/totem-v0.3/06-reset-03.jpg)
All reset soldered.
![06-reset-04](/totem-v0.3/06-reset-04.jpg)
The current state of the builds.
![06-reset-05](/totem-v0.3/06-reset-05.jpg)

## Xiao
The Xiaos need to be soldered directly in the PCB in case you will use the 3D printed case. So make sure to test them before this step, connect to your computer, and even try entering the bootloader mode.
![07-xiao-01](/totem-v0.3/07-xiao-01.jpg)
I used some pins just to make sure the pinout would be aligned, there are some bottom pads that you will need to solder later, so I thought using these pins temporarily would help.
![07-xiao-02](/totem-v0.3/07-xiao-02.jpg)
As you can see after soldering some pads I removed the pins and continued until all the pads were soldered.
![07-xiao-03](/totem-v0.3/07-xiao-03.jpg)
After soldering one or two pads check if the pads below are aligned.
![07-xiao-04](/totem-v0.3/07-xiao-04.jpg)
To solder then you will need a lot of flux, patience, and again a small tip solder iron.
![07-xiao-05](/totem-v0.3/07-xiao-05.jpg)
All Xiaos soldered.
![07-xiao-06](/totem-v0.3/07-xiao-06.jpg)
The current state of the builds.
![07-xiao-07](/totem-v0.3/07-xiao-07.jpg)

## Batteries
The batteries are the easiest part, I bought mine in a local store just need to be in the dimensions specified (15 x 22 x 7.5 mm). If you have a multimeter, check the voltage before soldering and keep sure the power switch in the PCB is off before installing.
![08-batt-01](/totem-v0.3/08-batt-01.jpg)
Red wire for positive (+) and black for negative (-).
![08-batt-02](/totem-v0.3/08-batt-02.jpg)
All batteries are soldered, you can turn the power switch on and if you have no firmware installed in the Xiao a small LED should blink super fast (at least in my version that happened), you can use the multimeter to check if the battery voltage is getting in the Xiao pads (the one's bellow).
![08-batt-03](/totem-v0.3/08-batt-03.jpg)
The current state of the builds.
![08-batt-04](/totem-v0.3/08-batt-04.jpg)

## Flashing the firmware
Since this project uses ZMK, I suggest following their documentation:
https://zmk.dev/docs/user-setup

## Case
For the 3D-printed case, I inserted the standoffs in the holes.
![09-case-01](/totem-v0.3/09-case-01.jpg)
At this moment I have already screwed the top screws.
![09-case-02](/totem-v0.3/09-case-02.jpg)
Then I proceeded to screw the PCB and the bottom part together.
![09-case-03](/totem-v0.3/09-case-03.jpg)
Next, I inserted the switches on the Hotswap over the case.
![09-case-04](/totem-v0.3/09-case-04.jpg)
And moved to the keycaps.
![09-case-05](/totem-v0.3/09-case-05.jpg)
Case assembled 1
![09-case-06](/totem-v0.3/09-case-06.jpg)
Case assembled 2
![09-case-07](/totem-v0.3/09-case-07.jpg)
The current state of the builds.
![09-case-08](/totem-v0.3/09-case-08.jpg)

## Finished
![10-finished-01](/totem-v0.3/10-finished-01.jpg)
![10-finished-02](/totem-v0.3/10-finished-02.jpg)
![10-finished-03](/totem-v0.3/10-finished-03.jpg)
![10-finished-04](/totem-v0.3/10-finished-04.jpg)
![10-finished-05](/totem-v0.3/10-finished-05.jpg)
![10-finished-06](/totem-v0.3/10-finished-06.jpg)
