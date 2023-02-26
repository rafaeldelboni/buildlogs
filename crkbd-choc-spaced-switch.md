# davidphilipbarr's Choc-Spaced-Corne Keyboard ([choc-spaced-corne switch](https://github.com/davidphilipbarr/Choc-Spaced-Corne/tree/main/chocorne-switch))

Check the [final product](#finished)  

## Tools Used

| Name | Count | Remarks |
|:-|:-|:-|
| Soldering Iron | 1 piece | CXG 110WT - https://www.aliexpress.com/item/33031529555.html |
| Solder wire | 1 piece | Sn63/Pb37 - 1.0mm - https://www.aliexpress.com/item/1005002646781061.html |
| Multimeter | 1 piece | https://www.aliexpress.com/item/4000991575808.html |
| Flux Soldering Pen | 1 piece | https://www.aliexpress.com/item/32908270559.html |
| Tweezers | 1 piece | https://www.aliexpress.com/item/1005003632772720.html |

![01-tools-used](/crkbd-choco-v2.1.0/01-tools-used.png)

## Part List

### Required

| Name | Count | Remarks |
|:-|:-|:-|
| PCB | 2 pieces | https://jlcpcb.com/ - [gerber](https://github.com/davidphilipbarr/Choc-Spaced-Corne/blob/main/chocorne-switch/ccs_gerber.zip) |
| nice!nano v2 | 2 pieces | Type-C USB - https://42keebs.eu/shop/parts/controllers/nice-nano-v2-wireless-controller/ |
| Male Pin Connector | 50 pieces | https://www.aliexpress.com/item/32945586364.html |
| Female Pin Header | 2 pieces | 1x40P 2.54mm - https://www.aliexpress.com/item/32892386779.html |
| Toggle Switch | 2 pieces | 7 Pin Mini Slide Switch On-off 2position - https://www.aliexpress.com/item/1005003829889015.html |
| Tactile switch | 2 pieces | 1136-4.3 DIP Black - https://www.aliexpress.com/item/1005001629184984.html |
| Batteries | 2 pieces | 3.7v 130 mah - https://www.aliexpress.com/item/4000384787808.html |
| Diode | 42 pieces | 1N4148 T4 SOD-123 - https://www.aliexpress.com/item/32921490945.html |
| Key switch | 42 pieces | Choc (low profile) - https://www.aliexpress.com/item/4000907409650.html |
| Key-caps | 42 pieces | 1u 40, 1.5u 2 - https://www.aliexpress.com/item/32979973961.html |

### Optional

| Name | Count | Remarks |
|:-|:-|:-|
| Cushion rubber | 8 pieces | https://www.aliexpress.com/item/1005002618681200.html |

![00-all-parts        ](/crkbd-choc-spaced-switch/00-all-parts.jpg)

## Promicro socket
Socketing your nice!nanos is a optional step, but there are some benefits of doing this.
One is that they are fragile and can break they usb connector or brick when flashing the firmware
so it's super easy to replace if you did the sockets, not losing the rest of your Keyboard
or need to expend hours desoldering the nano legs.
Another benefits is that nanos are super expensive, but you can use then is so many other
keyboard PCBs, so you could easily build another keyboard layout and use the same 
nanos in multiple keyboards.
![01-nano-socket-01](/crkbd-choc-spaced-switch/01-nano-socket-01.jpg)
I use a breadboard to make the sockets because it's easy to remove the promicro
after soldering the legs.
![01-nano-socket-02](/crkbd-choc-spaced-switch/01-nano-socket-02.jpg)
**ALWAYS USE MASK TAPE FOR THIS**, if you don't the solder will go thought the hole
and glue the promicro in the socket, making all of your work useless.
![01-nano-socket-03](/crkbd-choc-spaced-switch/01-nano-socket-03.jpg)
The male pin connector that I bought came with this black plastic separator, I don't like them
visually and I tested that the battery will fit bellow the promicro even without them
so I decided to remove.
![01-nano-socket-04](/crkbd-choc-spaced-switch/01-nano-socket-04.jpg)
Quite of manual work to be honest.
![01-nano-socket-05](/crkbd-choc-spaced-switch/01-nano-socket-05.jpg)
But in the end I liked the minimalist visual.
![01-nano-socket-06](/crkbd-choc-spaced-switch/01-nano-socket-06.jpg)
Start by the corners
![01-nano-socket-07](/crkbd-choc-spaced-switch/01-nano-socket-07.jpg)
Insert the promicro and continue adding the pins
![01-nano-socket-08](/crkbd-choc-spaced-switch/01-nano-socket-08.jpg)
![01-nano-socket-09](/crkbd-choc-spaced-switch/01-nano-socket-09.jpg)
Solder
![01-nano-socket-10](/crkbd-choc-spaced-switch/01-nano-socket-10.jpg)
You can trim off the excess of the pins
![01-nano-socket-11](/crkbd-choc-spaced-switch/01-nano-socket-11.jpg)
![01-nano-socket-12](/crkbd-choc-spaced-switch/01-nano-socket-12.jpg)
![01-nano-socket-13](/crkbd-choc-spaced-switch/01-nano-socket-13.jpg)

## Power Switch
This is a super tiny component be careful with it.
![02-power-switch-01](/crkbd-choc-spaced-switch/02-power-switch-01.jpg)
Add some solder in the pads of one side before, then with a tweezer hold it in
place and heat the pads in the pads to solder it.
![02-power-switch-02](/crkbd-choc-spaced-switch/02-power-switch-02.jpg)
Proceed to the other legs using flux to help you.
![02-power-switch-03](/crkbd-choc-spaced-switch/02-power-switch-03.jpg)
Now you can turn on the switch and with a multimeter in continuity mode check if it's working.
It should beep when is on and not beep when is off.
![02-power-switch-05](/crkbd-choc-spaced-switch/02-power-switch-05.jpg)

## Top Components
I like to use tape to hold those in place before solder
![03-top-components-01](/crkbd-choc-spaced-switch/03-top-components-01.jpg)
Then I invert the pcb, check if they are still aligned and then proceed to soldering.
![03-top-components-02](/crkbd-choc-spaced-switch/03-top-components-02.jpg)

## Diodes
The SMD diodes are trick at first, they are pretty small and they have polarity, make sure to match the polarity with PCB, align your as picured bellow.
![04-diodes-01](/crkbd-choc-spaced-switch/04-diodes-01.jpg)
To make it easier to solder, first put some solder on one of the PCB diode contacts
![04-diodes-02](/crkbd-choc-spaced-switch/04-diodes-02.jpg)
Then with a tweezer hold the diode over the solder and heat it to stick the diode
![04-diodes-03](/crkbd-choc-spaced-switch/04-diodes-03.jpg)
Proceed to the other diode contact and solder it normally
![04-diodes-04](/crkbd-choc-spaced-switch/04-diodes-04.jpg)

## Batteries
Batteries have polarity, if your PCB is like mine and don't have the polarity indicator printed on it,
make sure to check it using a multimeter in continuity mode, placing one probe in the ground
of the promicro legs and another in one of the battery pads,
when it beeps means where you will solder the negative wire.
![02-power-switch-04](/crkbd-choc-spaced-switch/02-power-switch-04.jpg)
![05-batt-01](/crkbd-choc-spaced-switch/05-batt-01.jpg)
In this pcb the pads are inverted on each side, always double check before soldering the battery,
inverting the wires here can damage your promicro.
![05-batt-02](/crkbd-choc-spaced-switch/05-batt-02.jpg)

## Flashing the firmware
Since this project uses ZMK, I suggest follow their documentation:
https://zmk.dev/docs/user-setup

## Testing
At this moment I had enough to setup a manual test, to check if all I did until here was ok.  
I went to [keyboardtester](https://www.keyboardtester.com) and plugged the new keyboard to the PC.  
I pressed the both reset buttons to pair each side and then I simulated the switch behaviour with the tweezer.
![06-test-progress-01](/crkbd-choc-spaced-switch/06-test-progress-01.jpg)

## Switchs
I like to attach all the switchs in the PCB before soldering
![07-switch-01](/crkbd-choc-spaced-switch/07-switch-01.jpg)
![07-switch-02](/crkbd-choc-spaced-switch/07-switch-02.jpg)

## Details

### Painting the side of the PCB
I used POSCA for painting the pcb sides, you can see how it looks better painted in the keyboard above.
![08-details-01](/crkbd-choc-spaced-switch/08-details-01.jpg)
![08-details-02](/crkbd-choc-spaced-switch/08-details-02.jpg)

### Rubber foots
![09-rubber-feets-01](/crkbd-choc-spaced-switch/09-rubber-feets-01.jpg)

## Finished
![10-final-01](/crkbd-choc-spaced-switch/10-final-01.jpg)
![10-final-02](/crkbd-choc-spaced-switch/10-final-02.jpg)
