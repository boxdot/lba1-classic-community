# Little Big Adventure build guide

## Prerequisites

* [DOSBox] - DOS emulator we will use to compile the game inside.
* [4DOS] - Some commands in DOSBox are not supported. So we will need another DOS interpreter.
* Watcom 10 compiler - For compiling C files and running MAKEFILEs
* MASM (Microsoft Macro Assembler) 6.0 - For compiling ASM files

[4DOS]: https://www.4dos.info/v4dos.htm#751
[DOSBox]: https://www.dosbox.com/

## Getting prerequisites

DOSBox and 4DOS are freely available. For getting Watcom 10 and MASM 6.0, you need to search the
internet. Note that I did not manage to build the game with Open Watcom. Also, the MASM 6.11
compiler did run very slowly in the DOSBox, so it was basically unusable.

All directories and files will be placed into the `~/lba-hacking` directory on your host machine. We
will mount this directory to `C:` in DOSBox.

Extract Watcom and MASM installers into

DOSBox is most likely distributed by your Linux distribution. Or, it can be installed directly
from their website.

## Dosbox configuration

```
[autoexec]
mount C ~/lba-hacking

PATH c:\watcom\binw;c:\masm\bin;%PATH%
set INCLUDE=c:\watcom\h;c:\lba\lib386
set WATCOM=c:\watcom
set EDPATH=c:\watcom\eddat
set WIPFC=c:\watcom\wipfc

f:
cd f:\lba
```
