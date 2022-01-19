![The PCB](https://github.com/andilge/Futai-Encoder-WS2811-ring/blob/main/images/front-and-back.png?raw=true)

# Futai RGB encoder, 12 WS2811 F5 LED ring on a translucent white blinde plate
The ultimate DIY human light controller interface plenty of colored LEDs.

## Credits
Inspired by [isotope-engineering's RGB rotary encoder](https://github.com/isotope-engineering/RGB-Encoder-Board "isotope-engineering's RGB rotary encoder").

Shoutout to [ezcGman](https://github.com/ezcGman "ezcGman") for the assistance with the KiCad symbols and footprints, hints about thermal reliefs on pads and the continuous feedback about his experiences while building up the circuit with the board.

### SPECIAL ATTENTION REQUIRED !
***
There are reports about wrong pin out for the addressable LEDs (D1-D12) 
***

The [official data sheet right from the producer](http://cn.world-semi.com/DownLoadFile/98 "official data sheet right from the producer") says /
pin1 - DOUT /
pin2 - VCC /
pin3 - GND /
pin4 - DIN

With the purchase URL in the BOM, you might get LEDs with 180 degree flipped around pin out /
pin1 - DIN /
pin2 - GND /
pin3 - VCC /
pin4 - DOUT

If you solder these faulty LEDs on the board "the right way around" the following will happen:
No light turns on and the LEDs instantly burn off to nirvana :-( rip

If you receive LEDs with flipped pins you can still use them. The board continues following the specification and can handle these faulty LEDs if you just place them "the wrong way around". Basically flipped pin out together with flipped placement turns out as success again :man_facepalming:.

IMPORTANT: Please test a LED from the sent bunch first to get a reality approach about which way around you should use them !

Special thanks to [ezcGman](https://github.com/ezcGman "ezcGman") for burning time and components to achieve this particular insight.

## KiCad dependencies
This project uses custom KiCad symbols and footprints and 3D models. Follow folder 'libs' with all details.

## Parts list
The folder 'fabrication' contains the zipped production files for pcb ordering and interactive bill of material ibom.html with purchase links for the components.

Additional to this you can purchase 10 blind plates also on [aliexpress.com](https://www.aliexpress.com/item/32884601740.html "aliexpress.com")

## Schematic
Dive deeper into details in the folder 'datasheets-and-schematic'.

## Tools list
### Required
- A soldering iron
- Solder

### Optional
- For SMD components:
- A hot air soldering/re-flow station. However, the smallest parts are 0805 SMD components which can be soldered with a soldering iron. The LED's legs are very close together and easier to solder with hot air.
- Solder paste
- Tweezers
- the famous IKEA cork coaster (Onderzetter) that gently takes up the heat of your soldering tools

