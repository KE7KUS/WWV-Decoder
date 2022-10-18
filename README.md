# WWV-Decoder
GNURadio software-defined radio decoder for WWV time broadcast.

## Introduction
The advent of software-defined radio suites like [GNURadio](https://www.gnuradio.org/) and [LuaRadio](https://luaradio.io/) have created an environment where radio enthusiasts can easly (and cheaply) experiment, learn the basics of digital signal processing, software defined waveforms, and elemental computer programming.  

After several years of experimenting with [RTL-SDR](https://www.rtl-sdr.com/buy-rtl-sdr-dvb-t-dongles/) dongles as simple software-defined radio receivers, I decided to create a learning lab for those interested in a more in-depth use of these amazing devices to further understand modern signal processing techniques.  Since I developed this lab, the number of available, affordable SDR receivers has grown exponentially, however, the fundamentals taught in this lab can be applied to a wide variety of hardware candidates, thanks to projects like [SoapySDR](https://www.welle.io/devices/soapysdr) and other efforts to bring hardware support to established SDR environments.

## The Objective
After several years of using SDR's for simple tasks like W/NFM receivers, spectrum analyzers, and APRS Rx-only IGates, the learning lab project purposed to focus on some of the basics of digital signal processing.  A lab was needed that provided end-to-end flowgraph development, but at a complexity level that newcomers to SDR could understand an implement.  While there may be some steepness to the learning curve associated with this lab, it most likely lies in the realm of computer programming, and not necessarily in the realm of radio or signal processing.  The prospective learner should have an entry-level grasp of computer programming.  GNURadio leverages both C++ and Python, however, the majority of this project was done in Python, providing a well-documented, moderately easy-to-learn programming experience.

## The Method
To delve into digital signal processing basics, the project needed a source signal which was simple, readily available, and well documented.  After a brief search, I settled on a well-known radio signal to almost every radio afficionado on the planet...the WWV/WWVH broadcast time signal.  The WWV/WWVH signal is broadcast 24/7 on multiple shortwave frequencies and can be received with a modest antenna and receiver.  It provided the right level of accessibility and complexity needed for this project.

## Shifting Fire
When I first began coding this project, my intent was to create a decoder which processed the audible tones heard during the WWV broadcast.  After researching the broadcast format, I discovered I needed to shift fire from decoding the audible part of the WWV signal (clicks, tones, etc.) and focus my efforts on decoding the binary-coded decimal (BCD) signal present at 100Hz in the WWV/WWVH transmission.  The BCD signal provided the time performance I needed, while at the same time providing an excellent learning tool for the signal processing lab.

## Software Tools
Several software tools were used in this lab:

- *[GNURadio](https://www.gnuradio.org/)*: A robust software defined radio development environment.  Provides GNURadio Companion, the primary software tool used for this project.
- *[Baudline](https://www.baudline.com/)*: A 2D spectrum visualization tool allowing graphical depiction of signals in both time and frequency domains.
- *[Tenacity](https://tenacityaudio.org/)*: An audio processing suite allowing graphical depiction of signals in both time and amplitude.

