# ErgoDoxTW
Change was made based on [ErgoDone v1.5](https://github.com/ktec-hq/ErgoDone/commit/091d1d12327a9dc95b3b4be09c8e6d85ce0d4d30)  

## PCB Preview in KiCad
![pcb preview](https://raw.githubusercontent.com/Keyman-Taiwan/ErgoDoxTW/master/full_preview_small.png)
You can find a larger image in the preview folder.

`IMPORTANT`: v1.4 is under validate.

## Difference/Improvement with ErgoDone
1. Rollback to use Teensy 2.0 for main controller (same as ErgoDox)
2. Rollback to use MCP23018 for IO expander (same as ErgoDox)
3. USB Type-C connector (only support USB 2.0 due to Teensy 2.0)
4. Support to use Kailh hot plug socket
5. Support to use SMD 1206 component for Resistor and Capacitor
6. Change TRRS socket to PJ-320A/E, which is more easy to find and cheapper. (please check folder ref_data/3.5mm
)
7. **`ONLY`** support 76 keys due to component change and pcb layout change.

## Branch Description
* master & USB_C_DIP_RightHand: Teensy IC on Right hand (Compatible with ErgoDox-EZ Configurator)
* USB_C_DIP: Teensy IC on Left hand

## Software Requirement
* Kicad 5.1.4

## KiCad library used by ErgoDoxTW
* [ai03-2725/Type-C Connecter](https://github.com/ai03-2725/Type-C.pretty): HRO-TYPE-C-31-M-12
* [daprice/keyswitches](https://github.com/daprice/keyswitches.pretty): Kailh hotplug socket
* Some components in ErgoDone's library
* Some components in ErgoDox's library

## KiCad Plugin used by ErgoDoxTW
* [NilujePerchut/kicad_scripts](https://github.com/NilujePerchut/kicad_scripts): teardrop pluging

## 3D model for preview
* [Kailh Hotplug Socket](https://github.com/qmk/qmk_hardware/tree/master/components): from qmk @ github
* [Cherry MX switch](https://github.com/ConstantinoSchillebeeckx/cherry-mx-switch): from ConstantinoSchillebeeckx @ github
* [Cherry MX Stabilizer](https://grabcad.com/library/cherry-mx-stabilizer-mx-1): from GrabCad
* SMD Diode / Resistor / LED are built-in model in KiCad

## BOM List
|               Item               | Amount |                                                                Comment                                                               |
|:--------------------------------:|:------:|:------------------------------------------------------------------------------------------------------------------------------------:|
| PCB boards                       |    2   | One for each hand                                                                                                                    |
| Teensy 2.0                       |    1   | Maion controller                                                                                                                     |
| MCP23018                         |    1   | I/O expander, Please choose DIP type                                                                                                 |
| 2.54mm Header Pins               |   24   | Unless pre-installed on the teensy board                                                                                             |
| Key switches                     |   76   | Compatible with Cherry MX is fine.                                                                                                   |
| Key Switch Hotplug Socket        |   76   | Kailh or Gateron. This is Optional                                                                                                   |
| Key Caps                         |   76   |                                                                                                                                      |
| 1N4148 diodes                    |   76   | SOD-123 package (SMD Type) or DO-35 (0.3” pitch) (Through-Hole Type)                                                                 |
| 3mm T1 LED                       |    3   |                                                                                                                                      |
| 220 Ω Resistor                   |    3   | Through-Hole Type Or 1206 SMD type (Red, Red, Brown)                                                                                 |
| 2.2k Ω Resistor                  |    2   | Through-Hole Type Or 1206 SMD type (Red, Red, Red)                                                                                   |
| 5.1k Ω Resistor                  |    2   | Through-Hole Type Or 1206 SMD type (Green, Brown, Red)                                                                               |
| 0.1μ F Capacitor                 |    1   | ceramic capacitor (marked “104” for 10*104 picofarad, or 100nF), also supported 1206 smd type. Not strictly necessary but suggested. |
| USB Type C connector             |    1   | 林躍電子 UB228-F16S4BR-A_DIP Or 浙富電子 16P 雙排 DIP                                                                                |
| USB mini B plug with short cable |    1   | Such as H2955. Use for connect type c connector and teensy board                                                                     |
| USB Type C Cable                 |    1   | A male to male cable, for connect keyboard to PC. (A to C) or (C to C) depend on your device.                                        |
| 3.5mm TRRS socket                |    2   | PJ-320A or PJ-320E                                                                                                                   |
| 3.5mm TRRS Cable                 |    1   | A male to male cable, for connect two pcbs.                                                                                          |
| ErgoDoxTW Keyboard case          |    1   | Acrylic Case                                                                                                                         |


# Lisence
GPL v3
