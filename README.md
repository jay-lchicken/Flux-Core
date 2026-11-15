# Flux Core Lite
## Why I made this

The goal of this is supposed to make making robots easier. I love to build robots and I realised they often use the same components across multiple different PCBs. These includes Buck-Down Converters, Microcontrollers, Motor drivers.

These PCBs require me to connect them via jumper wires which are very unreliable connections. Hence, this PCB combines the most common components into one PCB. However, the motor driver will be a seperate PCB in another project connected via PH2.0 Connectors (more reliable than normal jumper wires)

## Features
- This PCB features a single LED to indicate power
- It runs on RP2354A so that I do not need to connect external RAM.
- It uses a 12 MHz Crystal Clock
- It includes a reset button and BOOT button
- The PCB has a USBC port for code upload.
- It is also equipped with buck down converters so that I dont need to connect a buck down which is another external component.
- and other common microcontroller features...

## PCB
<img width="660" height="461" alt="Screenshot 2026-11-15 at 2 46 21 PM" src="https://github.com/user-attachments/assets/1bda5ef2-3ac7-4fbb-845e-68fac6aa16a8" />
This is a render of how the PCB looks like
<img width="894" height="608" alt="Screenshot 2026-11-15 at 2 47 21 PM" src="https://github.com/user-attachments/assets/4df55c0e-fbba-4837-9f3b-dc4d7476dcd8" />
This is the schematic
<img width="629" height="507" alt="Screenshot 2026-11-15 at 2 47 51 PM" src="https://github.com/user-attachments/assets/9df5cfda-49d2-434c-a404-484a36a24fac" />
PCB front layer traces
<img width="684" height="522" alt="Screenshot 2026-11-15 at 2 47 46 PM" src="https://github.com/user-attachments/assets/a1a45d8f-d308-4434-bba9-f80bf24fcaf8" />
PCB back layer traces
