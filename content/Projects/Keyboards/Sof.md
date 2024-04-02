---
title: Sof
tags:
  - keyboard
  - zmk
  - Y2024
created: 23/03/2024
github: https://github.com/DLBPointon/zmk-config-sof
---
GitHub: [zmk-config-sof](https://github.com/DLBPointon/zmk-config-sof)

After [[WAKeyboard]] and before my Sofle returned from the builder, I decided to try and build another Sofle. Why not?

Well, because i'm a beginner in this space, I burnt out a data pin. This is particularly annoying when your working on a PCB. So after figuring this out and having a look at the schematics, I figured i could just buy another MCU or go the hard way and learn a few things along the way. No prizes for figuring out which way i went. 

It turned out that Pin 11 on the board had died. I don't know when or how but it did. I also I noticed there is a spare and unused pin (22) just sat there waiting to be used.

So after a significant amount of research, it turns out that you can change the pin assignments in ZMK with overlay and dtsi files. This was much harder said than done, in theory it is switching one value to another. In reality, I couldn't find alot of docs on messing with this and the pro micro pins and and pins in the mini micro I have don't match up number wise. This matters as by the looks of it the ZMK firmware is based on the assumption of a pro micro pin out.

### The Pro Micro Pinout
![[promicro.png|450]]

### The Super Mini / Mini Micro pinout
![[supermini.png|550]]
So the number is different which means that the dead pin was actually Pin 14 on the Pro Micro/Pin 11 on the Super Mini. which meant the replacement pin was Pin 4 or 22. At the time, I didn't have the helpful diagram above, so it was much harder figuring this out on the fly.

Now we have the reason, step 2 is how do I fix this? Earlier I mentioned dtsi and overlay files, after asking around the community I figured out what needed to be done. [This](https://github.com/DLBPointon/zmk-config-sof/blob/main/boards/shields/sof/sof_left.overlay). See where the 4 is, just that one line.

## Wiring
Now, we need to connect the dead pins socket to the new pin. Luckily, I had some copper wire so was able to cut the pin from the controller and thread the wire between the new pin and the old socket pin (which was no longer connected to the MCU). I then added some solder to the joint as it was intermittently working, but it was working
### A terrible fix
![[fixup1.png|450]]
![[fixup2.png|550]]


Boom it worked.

I then downloaded some stl files from Thingiverse for a simple Sofle case, eventually figured out how to mirror it in Fusion360 and got it printed, in bright orange, by the UK company [SurfaceScan](https://www.surfacescan.co.uk/3d-printing-services/), I've used them a couple of times now and they've been great.

I also got the [Dwarven Ortholinear Keycap set from DROP](https://drop.com/buy/drop-the-lord-of-rings-mt3-dwarvish-keycap-set?defaultSelectionIds=968648). Which looks great, just be aware that the runes don't match up with the latin alphabet, because they are made to follow someone else's Dwarven font? I don't know, seems like a weird thing to have done to me.

< IMAGE TO COME >