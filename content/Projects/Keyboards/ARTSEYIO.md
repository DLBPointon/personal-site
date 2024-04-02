#kmk #keyboard #Y2024 

GitHub: https://github.com/DLBPointon/kmk-artseyio/tree/main

I have recently set up my PC for dual-booting. Currently, just Windows 11 and Pop OS. The issue is that the choice between OS's is before Bluetooth initialisation and I don't want to plug my [[Sofle]] in all the time.

So, i went hunting for a macropad style thing and found the [ARTSEYIO paintbrush](https://keebd.com/en-gb/products/paintbrush-keyboard-kit). An 8 key macropad which is just what I was looking for. I didn't realise how cool this thing was until looking for some firmware.

I saw a nice macropad, but this is a one handed keyboard combo-king keyboard designed to help those who, for any reason, can only use one hand. It achieves this by using a ton of combos with surprisingly few layers. You can see below.

![[artseyio.png]]
Quite frankly, this is cool as hell.

Only issue? I could get none of the available firmware working. Neither of the pre-bundled ZMK or QMK files would work, one would not get loaded onto the Elite PI I have driving it, and the other would load but not do anything. I tried learning some QMK, but honestly that thing scares me, I tried downloading the toolkit and working it out but I had to give up, it wasn't happening.

ZMK, i know some. My [[Sof]] and [[Sofle]] boards both use it but nothing I tried would work.

So i fell back to the simplest one I knew, KMK and boy did it save the day. After some work getting the right pin names and such, I got it working. Eventually, the whole centre column of the above image came together. However, there are/were a couple of issues...

- Something was wrong with the board that meant I had to wire up the ground as well as another pin for a column. Testing it the MCU with tweezers showed that it was working find, so I am guessing it was the PCB. This explains the extra wires in the images.

- One Shot doesn't work, for me just importing the module stops the board from working which ( due to the style of the keyboard) means shift isn't really useful at all.
    
- Layer TAP do not work. Adding the keymap including the layers, will cause the keys for that layer to not work.
    
- Layers are being a pain, full stop, adding the code for the number or nav layer will cause it to not work.

It might be that I bit off more than I can chew, so I have linked the repo at the top if anyone wants to have a go. 

And finally, the glory shot.
![[artseyioboard.png]]