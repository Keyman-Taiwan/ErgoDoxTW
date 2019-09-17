# ErgoDoxTW
Change was made based on [ErgoDone v1.5](https://github.com/ktec-hq/ErgoDone/commit/091d1d12327a9dc95b3b4be09c8e6d85ce0d4d30)  

## PCB Preview in KiCad
![pcb preview](https://raw.githubusercontent.com/Keyman-Taiwan/ErgoDoxTW/master/pcb_preview.png)

`IMPORTANT`: v1.2 has not been product and validate.

## Difference with ErgoDone
1. Rollback to use Teensy 2.0 for main controller (same as ErgoDox)
2. Rollback to use MCP23018 for IO expander (same as ErgoDox)
3. USB Type-C connector (only support USB 2.0 due to Teensy 2.0)
4. Support to use Kailh hot plug socket
5. Support to use SMD 1206 component for Resistor and Capacitor
6. **`ONLY`** support 76 keys due to pcb layout change.

## Keypart
* Master branch:
  * Type C Connector: HRO-TYPE-C-31-M-12 (A 16 Pins type c connector)
  * 3.5 mm Audio Jack Connector: PJ-320A or PJ-320L

## Software Requirement
* Kicad 5.1.4

## KiCad library used by ErgoDoxTW
* [ai03-2725/Type-C](https://github.com/ai03-2725/Type-C.pretty): type-C Connector (we use HRO-TYPE-C-31-M-12)
* [daprice/keyswitches](https://github.com/daprice/keyswitches.pretty): Kailh hotplug socket
* [qmk/qmk_hardware](https://github.com/qmk/qmk_hardware/tree/master/components): Kailh hotplug 3d model
* Some components in ErgoDone's library
* Some components in ErgoDox's library

## KiCad Plugin used by ErgoDoxTW
* [NilujePerchut/kicad_scripts](https://github.com/NilujePerchut/kicad_scripts): teardrop pluging

# Lisence
LGPL v3
