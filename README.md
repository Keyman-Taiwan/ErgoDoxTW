# ErgoDoxTW
Change was made based on [ErgoDone v1.5](https://github.com/ktec-hq/ErgoDone/commit/091d1d12327a9dc95b3b4be09c8e6d85ce0d4d30)  

## PCB Preview in KiCad
![pcb preview](https://raw.githubusercontent.com/Keyman-Taiwan/ErgoDoxTW/master/pcb_preview.png)

`IMPORTANT`: v1.3 has not been product and validate.

## Difference with ErgoDone
1. Rollback to use Teensy 2.0 for main controller (same as ErgoDox)
2. Rollback to use MCP23018 for IO expander (same as ErgoDox)
3. USB Type-C connector (only support USB 2.0 due to Teensy 2.0)
4. Support to use Kailh hot plug socket
5. Support to use SMD 1206 component for Resistor and Capacitor
6. **`ONLY`** support 76 keys due to component change and pcb layout change.

## Keyparts
* Common parts for all branch:
  * Hot plug socket: support both Kailh and Gateron 
  * 3.5 mm audio socket: support both PJ-320A (4pins) and PJ-320E (5pins), please check folder ref_data/3.5mm
    * (PJ-320A x2) or (PJ-320E x2) or (PJ-320A x1 + PJ-320E x1)

* Different parts
  * Type C Connector:
    * Master branch: HRO-TYPE-C-31-M-12 (SMD Type, 16 pins)
    * USB_C_DIP branch: UB228-F16S4BR-A_DIP (DIP Type, 16 pins)

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

# Lisence
GPL v3
