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

## BOM
| Comment | Designator | Footprint | JLCPCB Part # | LCSC Link |
|---|---|---|---|---|
| PH2.0-8P-LT | CN2 | CONN-SMD_PH2.0-8P-LT | C722766 | [C722766](https://www.lcsc.com/product-detail/C722766.html) |
| TactileButton,160gf | S1,S2 | SW_TS-1088-AR02016 | C720477 | [C720477](https://www.lcsc.com/product-detail/C720477.html) |
| 51kΩ | R4 | R_0805 | C17737 | [C17737](https://www.lcsc.com/product-detail/C17737.html) |
| 27Ω | R5,R6 | R_0805 | C17594 | [C17594](https://www.lcsc.com/product-detail/C17594.html) |
| 33Ω | R12 | R_0402 | C25105 | [C25105](https://www.lcsc.com/product-detail/C25105.html) |
| 22uF | C12,C19 | C_0805 | C45783 | [C45783](https://www.lcsc.com/product-detail/C45783.html) |
| Screw_Terminal_01x02 | J3 | Altech_AK100_1x02_P5.00mm | C3703 | [C3703](https://www.lcsc.com/product-detail/C3703.html) |
| 10kΩ | R9 | R_0402 | C25744 | [C25744](https://www.lcsc.com/product-detail/C25744.html) |
| XT60 | U4 | CONN-TH_XT60 | C98733 | [C98733](https://www.lcsc.com/product-detail/C98733.html) |
| 100nF | C18 | C_0603 | C14663 | [C14663](https://www.lcsc.com/product-detail/C14663.html) |
| SY8120B1ABC | U5 | SOT-23-6_L2.9-W1.6-P0.95-LS2.8-BL | C88474 | [C88474](https://www.lcsc.com/product-detail/C88474.html) |
| SWPA4030S3R3MT | L3 | IND-SMD_L4.0-W4.0_SMNR4012 | C15269 | [C15269](https://www.lcsc.com/product-detail/C15269.html) |
| Conn_01x04_Pin | 3.3V,GND,VSYS | PinSocket_1x04_P2.54mm_Vertical | C5116483 | [C5116483](https://www.lcsc.com/product-detail/C5116483.html) |
| 27pF | C10,C11 | C_0402 | C1557 | [C1557](https://www.lcsc.com/product-detail/C1557.html) |
| X322512MSB4SI | X1 | CRYSTAL-SMD_4P-L3.2-W2.5-BL | C9002 | [C9002](https://www.lcsc.com/product-detail/C9002.html) |
| 4.7uF | C17,C21,C22,C23 | C_0402 | C23733 | [C23733](https://www.lcsc.com/product-detail/C23733.html) |
| MBR120VLSFT1G | D1 | SOD-123F_L2.8-W1.8-LS3.7-RD | C223608 | [C223608](https://www.lcsc.com/product-detail/C223608.html) |
| 1uF | C14,C15 | C_0402 | C52923 | [C52923](https://www.lcsc.com/product-detail/C52923.html) |
| XL-0603QYGC | LED1 | LED0603-RD | C2289 | [C2289](https://www.lcsc.com/product-detail/C2289.html) |
| 1kΩ | R11,R2 | R_0402 | C11702 | [C11702](https://www.lcsc.com/product-detail/C11702.html) |
| 100nF | C1,C13,C2,C20,C3,C4,C5,C6,C7,C8,C9 | C_0402 | C1525 | [C1525](https://www.lcsc.com/product-detail/C1525.html) |
| 5.1kΩ | R7,R8 | R_0402 | C25905 | [C25905](https://www.lcsc.com/product-detail/C25905.html) |
| SMDRI127-100MT | L2 | IND-SMD_L12.3-W12.3_SMDRI127 | C9904 | [C9904](https://www.lcsc.com/product-detail/C9904.html) |
| RP2354A | U6 | QFN-60-1EP_7x7mm_P0.4mm_EP3.4x3.4mm | C41378174 | [C41378174](https://www.lcsc.com/product-detail/C41378174.html) |
| 68Ω | R10 | R_0603 | C27592 | [C27592](https://www.lcsc.com/product-detail/C27592.html) |
| AP2112K-3.3TRG1 | U3 | SOT-25-5_L2.9-W1.6-P0.95-LS2.8-BL | C51118 | [C51118](https://www.lcsc.com/product-detail/C51118.html) |
| 10nF | C24 | C_0402 | C15195 | [C15195](https://www.lcsc.com/product-detail/C15195.html) |
| USB-TYPE-C-018 | USB1 | USB-C_SMD-TYPE-C-31-M-12 | C2927038 | [C2927038](https://www.lcsc.com/product-detail/C2927038.html) |
| XT30UPB-M | CN1 | CONN-TH_XT30UPB-M | C428721 | [C428721](https://www.lcsc.com/product-detail/C428721.html) |
| 374kΩ | R3 | R_0402 | C54530857 | [C54530857](https://www.lcsc.com/product-detail/C54530857.html) |
