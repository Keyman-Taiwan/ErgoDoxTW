# ErgoDoxTW
Change was made based on [ErgoDone v1.5](https://github.com/ktec-hq/ErgoDone/commit/091d1d12327a9dc95b3b4be09c8e6d85ce0d4d30)  

## Differencce with ErgoDone
1. Rollback to use Teensy 2.0 for main controller (same as ErgoDox)
2. Rollback to use MCP23018 for IO expander (same as ErgoDox)
3. USB Type-C connector (only support USB 2.0 due to Teensy 2.0)
4. Support to use Kailh hot plug socket
5. Support to use SMD 1206 component for Resistor and Capacitor
6. **`ONLY`** support 76 keys* due to pcb layout change.

## Kicad library used by ErgoDoxTW
* [ai03-2725/Type-C](https://github.com/ai03-2725/Type-C.pretty): type-C Connector (we use HRO-TYPE-C-31-M-12)
* [daprice/keyswitches](https://github.com/daprice/keyswitches.pretty): Kailh hotplug socket

# Lisence
GPL v3
