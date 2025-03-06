# Balanced Headphone Operational Amplifier

A high powered differential headphone amp with a focus on modularity and prototyping. Inspired by the Schiit Audio Magni Heresy.

<p align="center">
  <a href="https://github.com">
    <img src="https://github.com/Stustup/C-Audio-BHOA/blob/332225ad11ce5fdea545c27f90542c3ff10ec40b/DSCF0732.JPG" height="300px">
  </a>
</p>

## Features

- All sections of the amp should be modular (Filter, VA, CA, Output protection)
- All sections should be accessable via pin headers
- Output power >1W per channel

## Schematic

<p align="center">
  <a href="https://github.com">
    <img src="https://github.com/Stustup/C-Audio-BHOA/blob/main/Schematic.png" height="300px">
  </a>
</p>

The Amp consists of a simple differential input filter for very high frequency noise, an instrumential amplifier input stage for differential voltage amplification and 8 paralelled opamp sections in buffer topology per channel (of which there are 4 for differential amplification for a total of 16 opamps(!!!). [Mental, I know](http://www.diyaudio.com/archive/blogs/alexcp/attachments/1049d1368388175-ne5532-power-amplifier-ne553205.jpg)). Furthermore the output is protected via muting relays driven by a mosfet and a turn on timer for a startup delay. 

## TODO

- Improve stability of current amplification. Maybe high value resistors to ground to give a reference for the inputs. Also cascaded topology might be a better CA stage as per [SBOA553A](https://www.ti.com/lit/ab/sboa553a/sboa553a.pdf?ts=1741260128432)
- Improve output protection. Firstly ADD some DC protection and improve the circuit for setting delay time.
