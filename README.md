# Board Bringup Swiss Knife (WIP)

This repo contains documentation and usage information of commonly used commands in U-boot and utilities in Linux that help during board bringups. This list is a work in progress.

## U-Boot
 * mtest (memorytest) - perform DDR testing.
  ```
mtest - simple RAM read/write test
Usage:                 
mtest [start [end [pattern [iterations]]]]

Usage example:
mtest 0x20000000 0x22000000 0xaabbccdd
```
* gpio - control/configure/read GPIO status

```
gpio <input|set|clear|toggle> <pin>
gpio read <name> <pin>
gpio status [-a] [<bank>|<pin>]
```
* pinmux - dump pinmux state
```
pinmux list
pinmux dev [pincontroller-name]
pinmux status [-a | pin-name]
```
* dm - dump device status/tree
```
dm compat
dm devres
dm drivers
dm static
dm tree [-s][-e] [uclass name]
dm uclass [-e] [udevice name]
```
## Linux

* memtester - ensure that the DDR is stable
```
memtester 1G
```
