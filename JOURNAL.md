---
title: "htkbd"
author: "Heinrich Xiao @itsme"
description: "Theo's perfect keyboard https://www.youtube.com/watch?v=pL4bkyCBKxQ"
created_at: "July 6, 2025"
---

## July 5, 2025
I made the dongle and tried to use the RP2040. The dongle was a pain. It had to be small and it had to be easy to design (cuz i have skill issues), so it should ideally only have one ic. i realized this after i read through all of the rp2040 datasheet chapter 2: minimal design example and finished a schematic, with only the rp2040. then, i realized i actually had to add more stuff, like the rf controller, which i didn't have space for after the rp2040 and the stuff that came with it. so, i decided today that i was gonna use the nRF52840.

time spent: 3hr

## July 6, 2025
I made the dongle. And finished it somehow. I basically just "referenced" the datasheet and stole everything. the one decision i actually had to make was choosing the antenna, which i chose to be one of those smd ceramic ones since thats what google told be was easiest and what seemed like the easiest. i chose the 2450AT18D0100E. 

Then, i made the keyboard, which i just copied from the dongle for all the parts involving the nRF52840 and even used the same antenna. i had a five by 12 kbd matrix cuz theo wanted 60% and i didn't want to use a 5x12 since the top row (number row) has 14 keys and i didn't want any keys borrowing from other rows and my mcu had enough pins. I also chose to use a tp4056 module to charge my battery though i have not decided the battery i will use. 

then, i added the touchpad for the keyboard. it was very difficult to find a good option. first, i found the TPS65 from azoteq and thought it was perfect and just worked over i2c. then i looked at it a bit more and realized it was not gonna work since it was too small and had no way to click. after realizing this, i just had to keep looking for a decent non-custom trackpad and couldn't find one. then i stumbled across a FOSH (free and open source hardware) trackpad, the procyon. it was pretty tiny and i originally wanted to customize it, but then i looked at the creator's repos and found the peacock. which is around the size i need but it had some extra components that i didn't want (specifically, it was also a macropad and i obvi didn't need that). so, i just cloned peacock, removed the parts i didn't need in schematic, then redesign parts of the pcb for my use case, and then added it to htkbd, making sure to wire everything up right. and peacock also used i2c.

time spent: 10hr...... i have no life
