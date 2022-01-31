![The PCB](https://github.com/andilge/Futai-Encoder-WS2811-ring/blob/main/images/board-front-and-rear.png?raw=true)

# Futai RGB encoder, 12 WS2811 F5 LED ring on a translucent blank cover panel
The ultimate DIY human light controller interface plenty of colored LEDs.

## Credits
Inspired by [isotope-engineering's RGB rotary encoder](https://github.com/isotope-engineering/RGB-Encoder-Board "isotope-engineering's RGB rotary encoder").

Shoutout to [ezcGman](https://github.com/ezcGman "ezcGman") for the assistance with the KiCad symbols and footprints, hints about thermal reliefs on pads and the continuous feedback about his experiences while building up the circuit with the board.

## KiCad dependencies
This project uses custom KiCad symbols and footprints and 3D models. Follow folder 'libs' with all details.

## Parts list
The folder 'fabrication' contains the zipped production files for pcb ordering and interactive bill of material ibom.html with purchase links for the components.

Additional to this you can purchase 10 blank cover panels on [aliexpress.com](https://www.aliexpress.com/item/32884601740.html "aliexpress.com")

### SPECIAL ATTENTION REQUIRED !
*There are reports about wrong pin out for the addressable LEDs (D1-D12)*

The [official data sheet from the producer](http://cn.world-semi.com/DownLoadFile/98 "official data sheet from the producer") says
|  pin # |   description   |
|:------:|:---------------:|
|   1    |       DOUT      |
|   2    |       VCC       |
|   3    |       GND       |
|   4    |       DIN       |


With the purchase URL in the BOM, you might get LEDs with 180 degree flipped around pin out
|  pin # |   description   |
|:------:|:---------------:|
|   1    |       DIN       |
|   2    |       GND       |
|   3    |       VCC       |
|   4    |       DOUT      |

If you solder these faulty LEDs on the board "the right way around" the following will happen:
No light turns on and the LEDs instantly burn off to nirvana, some with, others without magic smoke :astonished: rip

The board continues following the LED's specification and can handle these faulty LEDs if you just place them "the wrong way around". Basically, flipped pins together with flipped placement turns out as success again :man_facepalming:.

**IMPORTANT**: Please test a LED from the sent bunch first to get a reality approach about which way around you should use them !

Special thanks to [ezcGman](https://github.com/ezcGman "ezcGman") for burning time and components to achieve this particular insight.

## Connector pinout
| silkscreen | description                                                                   |
|:----------:|-------------------------------------------------------------------------------|
| 5V         | 5 Volt                                                                        |
| GND        | Ground                                                                        |
| EncA       | Encoder A                                                                     |
| EncB       | Encoder B                                                                     |
| SW         | Switch. On pressing the switch, 3.3 Volt are being passed to this header pin. |
| RED        | Red LED in the rotary encoder. *See more information below !                  |
| GRE        | Green LED in the rotary encoder. *See more information below !                |
| BLU        | Blue LED in the rotary encoder. *See more information below !                 |
| Din        | Data bus in for the adressable LEDs                                           |
| Dout       | Data bus out for the adressable LEDs                                          |

*For compatibility reasons with RGB strips, the board exptects 24V (also dimmed with pwm) at the rgb pin headers. If you're driving your **strip with 12V**, please change the value for **R51, R61 and R71 to 5.1kΩ**.
![Voltage deviders for encoder LED](https://github.com/andilge/Futai-Encoder-WS2811-ring/blob/main/images/v-devider-for-encoder-LED.png?raw=true)

## Schematic
Dive deeper into technical details in the folder 'datasheets-and-schematic'.

## Tools list
### Required
- A soldering iron
- Solder

### Optional
- For SMD components and addressable LEDs:
  - A hot air soldering/re-flow station. However, the smallest parts are 0805 SMD components which can be soldered with a soldering iron. The LED's legs are very close together and easier to solder with hot air.
  - Solder paste
- Tweezers
- The famous IKEA cork coaster (Onderzetter) that gently takes up the heat of your soldering tools.

