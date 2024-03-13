---
title: What A Keyboard!
created: 10/03/2024
tags:
  - project
  - raspberry-pi
  - kmk
  - python
github: https://github.com/DLBPointon/WAKeyboard
---
Full build diary is here: https://github.com/DLBPointon/WAKeyboard

Towards the end of 2023 I bought myself a Sofle V2, a really cool split ergo keyboard, and there were immediately issues with some soldering and a pin died. Anyhow, during the 6 week wait for a replacement I dove even further into the ErgoMech (Ergonomical Mechanical Keyboard) hobby space.

It didn't help that my daughter no wanted a fancy "space ship" keyboard, and I was happy to oblige. 

## Firmware
First, it's important to to acknowledge the firmware at play here. The major players are QMK, ZMK and KMK. Arguably, the first is the most popular but I couldn't understand how to use it ( I tried, but it just went straight over my head). 
ZMK is very nice, this is what shipped on my Sofle V2, and isn't too hard to build for your board of choice. There's a great online configurator that links to your github repository and triggers 
Finally, we have KMK a Python (Circuitpython) based keyboard firmware which is what I have used for WAKeyboard and for my [[ARTSYIO|ARTSYIO/paintbrush]] keyboard, boards I have built my self. KMK is very easy to get into and get a keyboard working.

## Hardware
I decided to use the Raspberry Pi Pico, simply because I have played with it before, it's cheap and powerful so win win. There are **alot** of other potential microcontrollers (MCU's) you could use, however, keep an eye out as some MCU's are only compatible with some firmwares and the number and layout of the pins may not be compatible with the PCB or project you work on.
Since this i've used the Elite-Pi in the [[ARTSYIO]] board, this is a board that uses the Pro-Micro layout (this is something you'll need to understand, you'll hear it alot).