# OSI_BASIC
An analysis of the Ohio Scientific 8K BASIC ROM

## About
Ohio Scientific produced a range of 6502-based computers for business and
personal use in the late 1970s and these are all well documented at various
sites, one of the better ones is here:

[Dave's OSI page](https://osiweb.org/)

A while back I had a personal project to recreate my first computer (an OSI
Superboard II) in a low-end Lattice iCE40UP5k FPGA:

(https://github.com/emeb/up5k_basic)
(https://github.com/emeb/up5k_vga)

I started with the combined ROM binary from here:

[ROM binary](https://osiweb.org/misc/OSI600_RAM_ROM.zip)

The original BASIC user manual contained a bit of information on entry points
and assembly interfacing, but in general was pretty sparse. Over the years
however it's been pretty thoroughly analyzed and there are a lot of resources
with tidbits of information on what's going on - see especially many of the
files collected at the "Daves's OSI page" site mentioned earlier. The complete
source listings from which these ROMs were built are also available from several
places:

(https://www.pagetable.com/?p=46)
(https://github.com/mist64/msbasic)
(https://github.com/brajeshwar/Microsoft-BASIC-for-6502-Original-Source-Code-1978)

Note that the original Microsoft source was common for many of their customers
target computers, so there are built-time macros that customise the output for
different features. Since I was mainly interested in the OSI variant this meant
that simply looking for address offsets wasn't helpful and a detailed analysis
and comparison against the source was required to make any changes to support
the FPGA version. That analysis is here in the file basic_rom_disassembled.txt

