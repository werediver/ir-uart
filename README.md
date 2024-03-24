# IR UART

This is an IR UART adapter. Its transmitter and receiver are independent, there is no automatic echo suppression. The receiver is based on [TSDP34156](http://www.vishay.com/docs/82667/tsdp341.pdf) IR receiver. The transmitter is built using [TSAL6400](https://www.vishay.com/docs/81011/tsal6400.pdf) 940 nm IR LEDs and a carrier generator based on [74HC132](https://assets.nexperia.com/documents/data-sheet/74HC_HCT132.pdf) quad-NAND CMOS gate.

The nominal transmission rate is 9600 baud. The carrier generator should be tuned to 57.6 kHz (with 6 cycles per bit it gives $57600 / 6 = 9600$ baud).

The adapter can be powered from 3.3 V or 5 V and will operate with the corresponding logic levels.

The board size is just 21x36 mm and provides 8 unconnected PTH (plated through holes) for mounting purposes. It should fit the [Pico (RP2040)](https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf) board well.

| · | · |
| - | - |
| ![Assembly top view](images/assembly-top.png) | ![Assembly overview](images/assembly-overview.png) |
| ![PCB top view](images/pcb-top.png) | ![PCB bottom view](images/pcb-bottom.png) |

![Schematic](images/schematic.svg)

## Performance

With minor adjustments after the first tests, the modules work as expected transmitting and receiving 1 kHz test signal. Using the modules with UART hasn't been tested yet.

Some more photos and/or info may be found at [hackaday.io/project/195022-ir-uart](https://hackaday.io/project/195022-ir-uart).
