---
title: "htkbd"
author: "Heinrich Xiao @itsme"
description: "Theo's perfect keyboard https://www.youtube.com/watch?v=pL4bkyCBKxQ"
created_at: "July 6, 2025"
---

## July 5, 2025
I made the dongle and tried to use the RP2040. The dongle was a pain. It had to be small and it had to be easy to design (cuz i have skill issues), so it should ideally only have one ic. i realized this after i read through all of the rp2040 datasheet chapter 2: minimal design example and finished a schematic, with only the rp2040. then, i realized i actually had to add more stuff, like the rf controller, which i didn't have space for after the rp2040 and the stuff that came with it. so, i decided today that i was gonna use the nRF52840.
