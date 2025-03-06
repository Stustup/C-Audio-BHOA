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

The Amp consists of a simple differential input filter for very high frequency noise, an instrumential amplifier input stage for differential voltage amplification and 8 paralelled opamps in buffer topology per channel (of which there are 4 for differential amplification). Furthermore the outpput is protected via muting relays driven by a mosfet and a turn on timer for a startup delay. 

## TODO

