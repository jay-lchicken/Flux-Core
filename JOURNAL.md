---
title: "Flux Core"
github: "https://github.com/jay-lchicken/Flux-Core"
description: "I am trying to make my very own robotics Dev board. Currently, the goal is to just try and make a dev board. I'm following a DigiKey tutorial currently. Along the way, I'm goign to find ways to make the Dev board better for robotics application. "
created_at: "2026-10-19"
total_time: "14h 12m"
---

# October 19, 2026: Studied the RP2040 Processor

I was studying the RP2040 processor on the raspberry pi website. So apparently, compared to an esp32, the RP2040 does not have flash memory on the chip itself. so its a bit like a cpu vs apple silicon where the storage is in the apple silicon chip but the cpu needs an external storage. So for the Rp2040, it needs an external flash memory.

![](https://fabricate.hackclub-assets.com/d7043bda3309a7994c5f6b2974579c9937fb76ded0c75e2edb6f1632a295f983/image-png/Screenshot%202026-10-19%20at%209.19.51%E2%80%AFPM.png)

**Total time spent: 30m**

# October 20, 2026: Added the RP2040, Capacitors and Flash Memory

![](https://fabricate.hackclub-assets.com/9a13e7cddb6c6ef1994d07fd63f51c97f13194b186e41d5ae5b26a9822446324/image-png/Screenshot%202026-10-20%20at%204.19.21%E2%80%AFPM.png)
I added in the RP2040 MCU, connected bypass and decoupling capacitors.
I also added the Crystal Clock which the RP2040 will be using in this dev board.
Lastly, I connected up the flash memory to SCK and SD0,1,2,3.

**Total time spent: 1h 24m**

# October 21, 2026: Added in USB Port, Buck Down and XT60s connector

First added a converter from 5v to 3.3V so that VBUs from USBC can be converted into the correct voltage for the RP2040. After that, I wanted the dev board to take in up to 14.8V from the battery so I added XT60 and XT30 connecters to the dev board so they can connect to the battery directly.

![](https://fabricate.hackclub-assets.com/79149a3429ab862b020ce7832f28b8598efd287dae55bbd977cf2b5a74b96643/image-png/Screenshot%202026-10-21%20at%207.45.38%E2%80%AFAM.png)

**Total time spent: 1h 30m**

# October 23, 2026: Changed MCU, fixed buck converter and added connectors

![](https://fabricate.hackclub-assets.com/f639e1ae9632ec6730b940675297b86c2c61f9b4de75c9757f6f06f00610f842/image-png/Screenshot%202026-10-23%20at%203.04.55%E2%80%AFPM.png)


I changed the MCU to RP2354A since the original Rp2040 does not have any flash memory. By changing the MCU to Rp2354A, it has an integrated flash memory, allowing me to save some space on my PCB. I also fixed the buck-down converter resistance to ensure that it outputs ~5V. Some pins were also originally not connected properly so I fixed that.

Next, I decided to add a mix of pins and sockets for the GPIO pins so that I dont always hav to connect a female or a male connector to the dev board.

Lastly, I chose a PH2.0 connector to connect I2C pins as well as UART Pins.

**Total time spent: 2h**

# October 29, 2026: Fixed schematic errors

![](https://fabricate.hackclub-assets.com/0f17d4a01fedceb1acd3de542064c57ebf37bceffed950620e4f0d14d2d480fd/image-png/Screenshot%202026-10-29%20at%205.18.21%E2%80%AFPM.png)
I updated the values of the buck down converter schematic. Turns out, one of my connections connect before a resistor to after a resistor making the resistor obsolete. hence, that connection was deleted. There were some crucial errors in the schematic as well such as putting a 3.9nH inductor. Thankfully, ChatGPT helped me catch that error and I fixed it back to a 3.3uH resistor.
Since this microcontroller is supposed to connect to a motor driver, I decided to change from a PH2.0 Connector to a MicroFit 3.0 2x4p connector. That's it for today.

**Total time spent: 1h 30m**

# November 3, 2026: Arranged PCB layout

I decided to change away from the existing motor driver connector and changed it back to a PH2.0 Connector to reduce cost. If i continued using Microfit connectors, each cable can cost from $5-$50. Hence, the change

![](https://fabricate.hackclub-assets.com/6143890323646135c218a5f5cca21190a1959a95cc6b9dd78f8bb76db92c5c46/image-png/Screenshot%202026-11-03%20at%207.55.36%E2%80%AFPM.png)

Next, based on my existing capacitors remarks

![](https://fabricate.hackclub-assets.com/3c3826e84f01a61fe8d02bf8328db4215c71ba11abfc20b9a6be0eb35e8093b0/image-png/Screenshot%202026-11-03%20at%207.55.54%E2%80%AFPM.png)

I arranged the rough layout of the PCB

![](https://fabricate.hackclub-assets.com/0d908a38302751bb8942451605b9a4e8de54183a9e1f17add50147927fe9ad7f/image-png/Screenshot%202026-11-03%20at%207.56.14%E2%80%AFPM.png)
It looks something like, I wanted it to be small and efficient. Next things that I need to do is change the trace thickness so it can support higher current draw, especially if I am running high current motors. To be honest, most of the components are randomly placed except for bypass and decoupling capacitors. Took me a while to fix some of the design errors too such as not having footprints assigned to the symbols

That's it for this journal

**Total time spent: 2h**

# November 7, 2026: Routing the PCB

gah!!! This is so exhausting. I just spent the last 2 hours trying to route the PCB. This is the first time I'm routing such a dense PCB. Usually I just randomly throw the footprints to a random slot in the PCB. but this time, it doesn't work because the PCB is so dense that tracks often cannot reach the other components because other tracks are blocking it. I've been deleting my tracks, rearranging the layout, tryna optimize everything, but it aint working (sob)...
![](https://fabricate.hackclub-assets.com/e67cbb42aa07dbae54bb967e1e6ef3435419d4956c8c33e1f78df705d2d57878/image-png/Screenshot%202026-11-07%20at%209.47.16%E2%80%AFPM.png)
![](https://fabricate.hackclub-assets.com/540c6a66fd715459342d325588be1f02efa0ad128ded68447a7f0b1e731a6193/image-png/Screenshot%202026-11-07%20at%208.42.16%E2%80%AFPM.png)

This is the current progress. I'm so close yet so far...

My plan after this is to arrange everything by using a Plugin called Place By Schematic in KiCad. Hopefully, this can help me arrange my components optimally

**Total time spent: 2h**

# November 8, 2026: PCB ROUTING IS FINALLY DONE!!!

YESS!!! AFTER ANOTHER 1.5 HOURS, I'VE FINALLY DONE IT.
First, I rearranged everything using a plugin called place by schematic

![](https://fabricate.hackclub-assets.com/bc9d8222e03685fb69798f273f9eb6ee934b3a8fb65bfdd105d53b35a4dbab90/image-png/Screenshot%202026-11-07%20at%209.53.49%E2%80%AFPM.png)

This allowed me to easily associate components with other components. Hence, when I was arranging the PCB into a more compact form, there was less traces that cross-pathed, making direct traces easier.

![](https://fabricate.hackclub-assets.com/08f5a183cc3bc8fc3f53256ee58402c15380fee49e17c9ee881b9c08e5c00317/image-png/Screenshot%202026-11-07%20at%2010.10.11%E2%80%AFPM.png)

Above is an image after I rearranged the entire PCB. It looks a lot better arranged with the ratsnet overlapping a lot less. 

![](https://fabricate.hackclub-assets.com/a6efc53683ec7e30ced2b0b1e0e7b6259144e6804188ec124dee431edd60b30f/image-png/Screenshot%202026-11-08%20at%2011.14.36%E2%80%AFAM.png)

The routing is now better and I managed to connect everything. Yay!!! 
I'm wondering if I can make it in an even smaller footprint, but that's a challenge for another day

**Total time spent: 1h 30m**

# November 15, 2026: Completed GitHub Repository

Before I could ship my project, I needed to fix up my GitHub repository.
I first started by going into JLCPCB to get a quotation on the Prices

![](https://fabricate.hackclub-assets.com/119c5d3c57a65f192cf2d76e17edbedfc00564d640d6d45760771ab4a67390ee/image-png/Screenshot%202026-11-15%20at%209.42.34%E2%80%AFPM.png)

This took a bit of time since I had to export from KiCad the gerber files, the BOM file and the Positions file.

Next, I had to create the BOM table in the README to add in all the components that would be used in the PCB Assembly. Also added in, shipping, pcb manuafacturing and assembly costs.

After that, I exported a STEP file from KiCad to upload into GitHub under 3D models.

Lastly, I created a very very simple LED blinking code to test the microcontroller when it arrives

**Total time spent: 1h 48m**
