# foostan's Corne Chocolate Keyboard ([crkbd v2.1.0](https://github.com/foostan/crkbd))

Original Foostan's [buildlog](https://github.com/foostan/crkbd/blob/main/corne-chocolate/doc/buildguide_en.md)  
Check the [final product](#finished)  

## Tools Used

| Name | Count | Remarks |
|:-|:-|:-|
| Soldering Iron | 1 piece | CXG 110WT - https://www.aliexpress.com/item/33031529555.html |
| Solder wire | 1 piece | 0.8mm - https://www.aliexpress.com/item/33023323860.html |
| Multimeter | 1 piece | https://www.aliexpress.com/item/4000991575808.html |
| Flux Soldering Pen | 1 piece | https://www.aliexpress.com/item/32908270559.html |
| Tweezers | 1 piece | https://www.aliexpress.com/item/1005003632772720.html |

![01-tools-used](/crkbd-choco-v2.1.0/01-tools-used.png)

## Part List

### Required

| Name | Count | Remarks |
|:-|:-|:-|
| PCB | 2 pieces | https://jlcpcb.com/ |
| Top plate | 2 pieces | https://jlcpcb.com/ |
| Bottom plate | 2 pieces | https://jlcpcb.com/ |
| Pro Micro protection plate | 2 pieces | |
| Pro Micro | 2 pieces | Type-C USB - https://www.aliexpress.com/item/32768308647.html |
| TRRS Jack | 2 pieces | https://www.aliexpress.com/item/32368285821.html |
| Tactile switch | 2 pieces | 1136-4.3 DIP Black - https://www.aliexpress.com/item/1005001629184984.html |
| Diode | 42 pieces | 1N4148W T4 SOD-123 - https://www.aliexpress.com/item/32921490945.html |
| Kailh PCB Socket (for Choc) | 42 pieces | https://www.aliexpress.com/item/33023283633.html |
| Key switch | 42 pieces | Compatible with Choc (low profile) only - https://www.aliexpress.com/item/4000907409650.html |
| Key-caps | 42 pieces | 1u 40, 1.5u 2 - https://www.aliexpress.com/item/32979973961.html |
| OLED module | 2 pieces | https://www.aliexpress.com/item/32777216785.html |
| 4 pin headers | 2 pieces | 24PIN-Wide - https://www.aliexpress.com/item/32864156728.html |
| 4 pin sockets | 2 pieces | 4 P - https://www.aliexpress.com/item/4001211882272.html |
| Spacer M2 4.5mm | 10 pieces | M2-5mm - https://www.aliexpress.com/item/32970573343.html |
| Spacer M2 9mm | 4 pieces | M2-9mm https://www.aliexpress.com/item/32970573343.html |
| Screw M2 4mm | 28 pieces | M2-4mm - https://www.aliexpress.com/item/32661182311.html |
| Cushion rubber | 8 pieces | https://www.aliexpress.com/item/1005002618681200.html |
| TRS (3 pole) or TRRS (4 pole) cable | 1 piece | https://www.aliexpress.com/item/32459681560.html |
| Micro USB Cable | 1 piece | https://www.aliexpress.com/item/4000802127824.html |
| Round Copper Wire | 1 piece | 0.5mm - https://www.aliexpress.com/item/4000781904492.html |

### Optional

| Name | Count | Remarks |
|:-|:-|:-|
| SK6812MINI(SK6812 3535 / MINI) | 54 pieces | 42 for backlight, 12 for under-glow - https://www.aliexpress.com/item/32830413032.html |

![02-parts-used](/crkbd-choco-v2.1.0/02-parts-used.png)

## PCB
I pretty much uploaded the v2.1.0 chocolate gerber file [avalilable on foostan's repository](https://github.com/foostan/crkbd/releases/tag/corne-chocolate-v2.1.0) in https://jlcpcb.com and let almost all defaults settings.

_After a day I placed the order they sent me an email asking for an extra U$ 15.2 because the PCB case has to many holes, I replied that I was OK with that, paid the extra charge and all good._
![02-02-pcb-order](/crkbd-choco-v2.1.0/02-pcb-order.png)

## Firmware

### Install/Configure QMK
See [The Complete Newbs Guide To QMK](https://docs.qmk.fm/#/newbs).

### Compile/Flash Firmware

```bash
sudo qmk flash -kb crkbd/rev1 -km default
```

## Leds
I've decided to do the leds first because I thought that with less components soldered in the PCB would make easier to solder such fragile and delicate part, but the problem with this approach is that later on when I was building the other parts of the keyboard, the mechanical torsion and the heat of soldering the other components could break some led soldering or even burning them.

SK6812MINI is very heat sensitive and breaks easily, you will need a soldering iron with a temperature control function and operating at a temperature of about 220°C to 270°.
I've used 250°C for the leds and 300°C for all the rest.

That said, **I really don't recommend this build** if you are planning to use leds a lot, they will eventually stop working, there are better builds that have use better leds out there.
![03-leds](/crkbd-choco-v2.1.0/03-leds-06.jpg)

### Under-glow
Solder the part so that the black part circled below is on the bottom and the silk mark indicated by the arrow is on the top. Note that the direction changes.
![03-leds](/crkbd-choco-v2.1.0/03-leds-02.jpg)
![03-leds](/crkbd-choco-v2.1.0/03-leds-03.jpg)
![03-leds](/crkbd-choco-v2.1.0/03-leds-04.jpg)

### Per-key
Perform soldering so that the largest pad surrounded by a circle and the silk mark indicated by an arrow are adjacent to each other, as shown below.
![03-leds](/crkbd-choco-v2.1.0/03-leds-05.jpg)

### Testing
I used a 3.5v font, attached the it in `VCC` and `GRD` pins and touched with the tweezers the pin `LED` (you can short this pin with `VCC` for a brief moment to trigger on the leds with a random color).

Keep in mind that i don't know what I'm doing, not sure if I can recommend you doing this. **Do at your own risk.**
![03-leds](/crkbd-choco-v2.1.0/03-leds-01.jpg)

## Diodes
The SMD diodes are trick at first, they are pretty small and they have polarity, make sure to match the polarity with PCB, align your as picured bellow.
![04-diodes](/crkbd-choco-v2.1.0/04-diodes-01.jpg)

To make it easier to solder, first put some solder on one of the PCB diode contacts and then with a tweezer hold the diode over the solder and heat it to stick the diode, proceed to the other diode contact and solder it normally.
![04-diodes](/crkbd-choco-v2.1.0/04-diodes-02.jpg)

## Kailh Hotswap
Very similar to soldering the diodes, but with a way bigger component.
![05-kailh-hotswap](/crkbd-choco-v2.1.0/05-kailh-hotswap-01.jpg)

## Top Components
An easy thru-hole solder.
![06-top-components](/crkbd-choco-v2.1.0/06-top-components-01.jpg)
![06-top-components](/crkbd-choco-v2.1.0/06-top-components-02.jpg)

## Soldering Promicro
My poor man's promicro socket version, since I can't find to buy the [mill max](https://splitkb.com/products/mill-max-low-profile-sockets) for a decent price.

I've used copper Wire 0.5mm to this, just remember to sand off the isolation layer.  

I used some masking tape to help me organize the wires.
![07-soldering-promicro](/crkbd-choco-v2.1.0/07-soldering-promicro-01.jpg)
Start by the corners
![07-soldering-promicro](/crkbd-choco-v2.1.0/07-soldering-promicro-02.jpg)
Insert the promicro and continue adding the wires
![07-soldering-promicro](/crkbd-choco-v2.1.0/07-soldering-promicro-03.jpg)
Also another benefit of using masking tape is to don't let the solder go thought the hole and "glue" with the PCB socket.
![07-soldering-promicro](/crkbd-choco-v2.1.0/07-soldering-promicro-04.jpg)
You can trim off the excess of the wires
![07-soldering-promicro](/crkbd-choco-v2.1.0/07-soldering-promicro-05.jpg)

## Mounting OLED
![08-mounting-oled](/crkbd-choco-v2.1.0/08-mounting-oled-01.jpg)
![08-mounting-oled](/crkbd-choco-v2.1.0/08-mounting-oled-02.jpg)

## All Components Soldered
![09-all-components-soldered](/crkbd-choco-v2.1.0/09-all-components-soldered-01.jpg)
![09-all-components-soldered](/crkbd-choco-v2.1.0/09-all-components-soldered-02.jpg)
![09-all-components-soldered](/crkbd-choco-v2.1.0/09-all-components-soldered-03.jpg)
![09-all-components-soldered](/crkbd-choco-v2.1.0/09-all-components-soldered-04.jpg)
![09-all-components-soldered](/crkbd-choco-v2.1.0/09-all-components-soldered-05.jpg)

## Switchs
I like to attach all the switchs in the PCB case grid
![10-switchs](/crkbd-choco-v2.1.0/10-switchs-01.jpg)
Just because I think is faster at the end
![10-switchs](/crkbd-choco-v2.1.0/10-switchs-02.jpg)
![10-switchs](/crkbd-choco-v2.1.0/10-switchs-03.jpg)
Always double check if all the pins of the switchs are passing through the hot-swaps
![10-switchs](/crkbd-choco-v2.1.0/10-switchs-04.jpg)

## Case
Start by the top screw and then while holding the screw with your finger turn the pcbs over and attach the spacer.
![11-case](/crkbd-choco-v2.1.0/11-case-01.jpg)
![11-case](/crkbd-choco-v2.1.0/11-case-02.jpg)
![11-case](/crkbd-choco-v2.1.0/11-case-03.jpg)

## Details

### Painting the side of the PCB
I used POSCA for painting the pcb sides, you can see how it looks better painted in the keyboard of the left.
![12-paint-side](/crkbd-choco-v2.1.0/12-paint-side-01.jpg)
![12-paint-side](/crkbd-choco-v2.1.0/12-paint-side-02.jpg)
Nice!
![12-paint-side](/crkbd-choco-v2.1.0/12-paint-side-03.jpg)

### Rubber foots
![13-rubber-foots](/crkbd-choco-v2.1.0/13-rubber-foots-01.jpg)

## Finished without keycaps
![14-finished-no-caps](/crkbd-choco-v2.1.0/14-finished-no-caps-01.jpg)
![14-finished-no-caps](/crkbd-choco-v2.1.0/14-finished-no-caps-02.jpg)
![14-finished-no-caps](/crkbd-choco-v2.1.0/14-finished-no-caps-03.jpg)

## Finished
![15-finished](/crkbd-choco-v2.1.0/15-finished-01.jpg)
![15-finished](/crkbd-choco-v2.1.0/15-finished-02.jpg)
![15-finished](/crkbd-choco-v2.1.0/15-finished-03.jpg)
![15-finished](/crkbd-choco-v2.1.0/15-finished-04.jpg)
