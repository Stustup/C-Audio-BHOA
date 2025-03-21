# Balanced Headphone Operational Amplifier

A high powered differential headphone amp with a focus on modularity and prototyping. Inspired by the Schiit Audio Magni Heresy.

![Picture of the PCB](DSCF0732.JPG)

## Features

- All sections of the amp should be modular (Filter, VA, CA, Output protection)
- All sections should be accessable via pin headers
- Output power >1W per channel

## Schematic

![Schematic of the Amp](Schematic.png)

The Amp consists of a simple differential input filter for very high frequency noise, an instrumential amplifier input stage for differential voltage amplification and 8 paralelled opamp sections in buffer topology per channel (of which there are 4 for differential amplification for a total of 16 opamps(!!!). [Mental, I know](http://www.diyaudio.com/archive/blogs/alexcp/attachments/1049d1368388175-ne5532-power-amplifier-ne553205.jpg)). 

![Schematic of instrumental amp](./Hardware/doc/BHOA%20Prestage.png)

The instrumental amplifier in the prestage was chosen, because it is really easy and straight forward to set the gain with just a a single resistor per channel.

![Schematic of current amp](./Hardware/doc/BHOA%20Current%20Amplifier.png)

Furthermore the output is protected via muting relays driven by a mosfet and a turn on timer for a startup delay. 

The power supply is off board to stay in the limits of JLCPCBs cheap 100x100mm PCB service. It can range from +-5V to +-18V (or how much the Opamps will take). The output relays are 5V, a simple 78l05 so8 IC is supplying them with 5V. 

## TODO

- Improve stability of current amplification. Maybe high value resistors to ground to give a reference for the inputs. Also cascaded topology might be a better CA stage as per [SBOA553A](https://www.ti.com/lit/ab/sboa553a/sboa553a.pdf?ts=1741260128432)
- Improve output protection. Firstly ADD some DC protection and improve the circuit for setting delay time.
