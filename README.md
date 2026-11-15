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

## Components BOM
| Part Number | Type | LCSC Part # | Provided By | Designator | Qty | Link | Total Price |
| :--- | :--- | :--- | :--- | :--- | :---: | :--- | ---: |
| `PH2.0-8P-LT` | Extended | `C722766` | System | CN2 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C722766) | $0.3685 |
| `TS-1088-AR02016` | Basic | `C720477` | System | S1, S2 | 10 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C720477) | $0.5160 |
| `0805W8F5102T5E` | Basic | `C17737` | System | R4 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C17737) | $0.0335 |
| `0805W8F270JT5E` | Extended | `C17594` | System | R5, R6 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C17594) | $0.0580 |
| `0402WGF330JTCE` | Basic | `C25105` | System | R12 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C25105) | $0.0055 |
| `CL21A226MAQNNNE` | Basic | `C45783` | System | C12, C19 | 10 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C45783) | $1.0840 |
| `WJ127-5.0-02P-14-00A` | Extended | `C3703` | Customer | J3 | 6 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C3703) | $0.7992 |
| `0402WGF1002TCE` | Basic | `C25744` | System | R9 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C25744) | $0.0050 |
| `XT60-M.` | Extended | `C98733` | System | U4 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C98733) | $1.7590 |
| `CC0603KRX7R9BB104` | Basic | `C14663` | System | C18 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C14663) | $0.0520 |
| `SY8120B1ABC` | Extended | `C88474` | System | U5 | 6 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C88474) | $0.9852 |
| `SWPA4030S3R3MT` | Extended | `C15269` | System | L3 | 9 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C15269) | $0.5499 |
| `2.54-1*4` | Extended | `C5116483` | Customer | 3.3V, GND, VSYS | 16 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C5116483) | $0.4032 |
| `0402CG270J500NT` | Extended | `C1557` | System | C10, C11 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C1557) | $0.0440 |
| `X322512MSB4SI` | Basic | `C9002` | System | X1 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C9002) | $0.4770 |
| `CL05A475MP5NRNC` | Basic | `C23733` | System | C17, C21, C22, C23 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C23733) | $0.2260 |
| `MBR120VLSFT1G` | Extended | `C223608` | System | D1 | 7 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C223608) | $1.5365 |
| `CL05A105KA5NQNC` | Basic | `C52923` | System | C14, C15 | 10 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C52923) | $0.0570 |
| `KT-0603YG` | Extended | `C2289` | System | LED1 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C2289) | $0.2120 |
| `0402WGF1001TCE` | Basic | `C11702` | System | R11, R2 | 10 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C11702) | $0.0130 |
| `CL05B104KO5NNNC` | Basic | `C1525` | System | C1, C13, C2, C20, C... | 55 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C1525) | $0.1320 |
| `0402WGF5101TCE` | Basic | `C25905` | System | R7, R8 | 10 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C25905) | $0.0140 |
| `SMDRI127-100MT` | Extended | `C9904` | System | L2 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C9904) | $1.1520 |
| `RP2354A` | Extended | `C41378174` | System | U6 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C41378174) | $6.2420 |
| `0603WAF680JT5E` | Extended | `C27592` | System | R10 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C27592) | $0.0260 |
| `AP2112K-3.3TRG1` | Extended | `C51118` | System | U3 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C51118) | $0.8335 |
| `CL05B103KB5NNNC` | Basic | `C15195` | System | C24 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C15195) | $0.0185 |
| `USB-TYPE-C-018` | Extended | `C2927038` | System | USB1 | 7 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C2927038) | $0.4445 |
| `XT30UPB-M` | Extended | `C428721` | System | CN1 | 5 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C428721) | $1.3180 |
| `1RC0402F3743` | Extended | `C54530857` | System | R3 | 20 | [JLCPCB Parts](https://jlcpcb.com/partdetail/C54530857) | $0.0360 |
| **Components Subtotal** | | | | | **336** | | **$19.4010** |
| **Assembly Cost** | | | | | | | **$48.6900** |
| **PCB Manufacturing Cost** | | | | | | | **$4.0000** |
| **Shipping** | | | | | | | **$10.0000** |=
| **Grand Total** | | | | | | | **$82.0910** |
