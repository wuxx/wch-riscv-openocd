# WCH RISC-V Openocd

compile passed currently, but still fail when program the CH32V003(detect succ, program finished but cannot run normally). WIP.

# test command
```
$sudo ./riscv-openocd/src/openocd -f wch-riscv.cfg -c  "init;halt;program blink_250.bin 0x0;reset;exit"
Open On-Chip Debugger 0.11.0+dev-gc287323-dirty (2022-12-14-10:34)
Licensed under GNU GPL v2
For bug reports, read
        http://openocd.org/doc/doxygen/bugs.html
Info : only one transport option; autoselect 'jtag'
Ready for Remote Connections
Info : WCH-LinkE-CH32V307  mod:RV version 2.7
Info : wlink_init ok
Info : This adapter doesn't support configurable speed
Info : JTAG tap: riscv.cpu tap/device found: 0x00000001 (mfg: 0x000 (<invalid>), part: 0x0000, ver: 0x0)
Warn : Bypassing JTAG setup events due to errors
Info : [riscv.cpu.0] datacount=2 progbufsize=8
Info : Examined RISC-V core; found 1 harts
Info :  hart 0: XLEN=32, misa=0x40800014
[riscv.cpu.0] Target successfully examined.
Info : starting gdb server for riscv.cpu.0 on 3333
Info : Listening on port 3333 for gdb connections
Info : JTAG tap: riscv.cpu tap/device found: 0x00000001 (mfg: 0x000 (<invalid>), part: 0x0000, ver: 0x0)
Warn : Bypassing JTAG setup events due to errors
** Programming Started **
Info : device id = 0x730babcd
Info : flash size = 16kbytes
Info : Hart 0 unexpectedly reset!
^[[24~** Programming Finished **
Info : JTAG tap: riscv.cpu tap/device found: 0x00000001 (mfg: 0x000 (<invalid>), part: 0x0000, ver: 0x0)
Warn : Bypassing JTAG setup events due to errors
```
