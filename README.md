# ErgoDoneTW
Change was made based on [ErgoDone v1.5](https://github.com/ktec-hq/ErgoDone/commit/091d1d12327a9dc95b3b4be09c8e6d85ce0d4d30)  

## PCB Preview in KiCad
![pcb preview](https://raw.githubusercontent.com/Keyman-Taiwan/ErgoDoneTW/master/pcb_preview.png)

`IMPORTANT`: v1.4 has not been product and validate.

## Difference with ErgoDone
1. Rollback to use Teensy 2.0 for main controller (same as ErgoDox)
2. Rollback to use MCP23018 for IO expander (same as ErgoDox)
3. USB Type-C connector (only support USB 2.0 due to Teensy 2.0)
4. Support to use Kailh hot plug socket
5. Support to use SMD 1206 component for Resistor and Capacitor
6. **`ONLY`** support 76 keys due to component change and pcb layout change.

## Branch Description
* master: IC on LEFT hand, use SMD usb type c connector
* USB_C_DIP: IC on LEFT hand, DIP usb type c connector
* USB_C_DIP_RightHand: IC on Right hand, DIP usb type c connector (Compatible with ErgoDox Configurator)

## Keyparts
* Common parts for all branch:
  * Hot plug socket: support both Kailh and Gateron 
  * 3.5 mm audio socket: support both PJ-320A (4pins) and PJ-320E (5pins), please check folder ref_data/3.5mm
    * (PJ-320A x2) or (PJ-320E x2) or (PJ-320A x1 + PJ-320E x1)

* Different parts
  * Type C Connector:
    * Master: HRO-TYPE-C-31-M-12 (SMD Type, 16 pins)
    * USB_C_DIP: 林躍電子 UB228-F16S4BR-A_DIP or 浙富電子 16P 雙排 DIP (DIP Type, 16 pins)
    * USB_C_DIP_RightHand: 林躍電子 UB228-F16S4BR-A_DIP or 浙富電子 16P 雙排 DIP (DIP Type, 16 pins)

## Software Requirement
* Kicad 5.1.4

## KiCad library used by ErgoDoneTW
* [ai03-2725/Type-C Connecter](https://github.com/ai03-2725/Type-C.pretty): HRO-TYPE-C-31-M-12
* [daprice/keyswitches](https://github.com/daprice/keyswitches.pretty): Kailh hotplug socket
* Some components in ErgoDone's library
* Some components in ErgoDox's library

## KiCad Plugin used by ErgoDoneTW
* [NilujePerchut/kicad_scripts](https://github.com/NilujePerchut/kicad_scripts): teardrop pluging

## 3D model for preview
* [Kailh Hotplug Socket](https://github.com/qmk/qmk_hardware/tree/master/components): from qmk @ github
* [Cherry MX switch](https://github.com/ConstantinoSchillebeeckx/cherry-mx-switch): from ConstantinoSchillebeeckx @ github
* [Cherry MX Stabilizer](https://grabcad.com/library/cherry-mx-stabilizer-mx-1): from GrabCad
* SMD Diode / Resistor / LED are built-in model in KiCad

## BOM List
* 2x PCB boards (one for each hand)
* 1x Teensy USB Board, Version 2.0
* 24x Teensy header pins, male (unless pre-installed)
* 1x MCP23018-E/SP I/O expander
* 76x Cherry MX switches (or compatible to Cherry MX style key switch)
* 76x MX Keycaps
* 76x 1N4148 diodes, SOD-123 package (Surface mount) or DO-35 (0.3” pitch) (through hole)
* 3x 3mm T1 LEDs
* 3x 220 Ω resistors, or match to LED. (red, red, brown) (through hole or 1206 smd type)
* 2x 2.2k Ω resistors (red, red, red) (through hole or 1206 smd type)
* 2x 5.1k Ω resistors (green, brown, red) (through hole or 1206 smd type)
* 5x Short jumpers (You can also use the clipped off legs from your resistors)
* 1x 0.1 μF (100nF) ceramic capacitor (marked “104” for 10*104 picofarad). Not strictly necessary but suggested (also supported 1206 smd type)
* 1x USB Type C connector (UB228-F16S4BR-A_DIP)
* 1x USB mini B plug with short cable (such as H2955)
* 1x USB cable: a male Type A to Type C or a male Type C to Type C (depend on your host)
* 2x 3.5 mm TRRS sockets (PJ-320A or PJ-320E)
* 1x Cable with two 3.5 mm TRRS plugs
* 1x Ergodox Keyboard case
* Kailh or Gateron Hot Plug Socket for key switches (optional)

# Lisence
GPL v3
