# Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology
1.[Abstract](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/blob/main/Abstract)

2.[Literature Survey](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#Literature-Survey)

3.[Working](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#Working)

**Abstract**
Memories are the crucial blocks in VLSI system 
design. The performance, power, and area of memories should 
be carefully inspected before fabrication of the system. In digital 
processors, we use SRAM cells in the memory cache for faster 
performance and low power consumption. 6T SRAM cell is 
designed with Synopsys Design Compiler using 28nm CMOS 
technology

**Literature Survey**
The number of transistors on an IC becomes twice 
every 18 months, according to Moore's law. For the modern 
System on Chip (SoC) technology, design is essential for
memory circuits with high performance. The critical duty of 
memory is storing data and accessing stored data for reading 
or writing as per demand. Non-volatile memory and volatile 
memory are primary differentiation of memory. When there 
is no power supply, stored data will be lost in volatile memory 
like RAM (Random Access Memory). Static RAM (SRAM) 
and Dynamic RAM (DRAM) are furthermore differentiation 
of RAM. In microprocessors and cache memories, SRAMs 
are widely used. The reason for using SRAM memories is 
that they have a minor power dissipation nature. SRAM's
speed of operation is high. The CMOS IC technology entered
the nanometer regime by scaling size continuously. The 
performance will be improved by decreasing the size of bulk-CMOS as we change to new technology. In modern SOCs,
SRAM has mainly used memory since it can hold data till 
there is a power supply to the cell. SRAM has two cross-coupled inverters. It can perform read and write operations 
without any update even though it occupies more space on 
the chip. In storing a single bit of data using a flip-flop, the 
SRAM cell is beneficial. SRAMs are mainly used as memory 
caches. For high performance and reliability, SRAM cells are 
used. The microprocessor uses SRAMs since it can go 
beyond the speeds of 250MHz. The density of SRAM cells is 
more when compared to DRAM cells. Though meticulously 
designed SRAMs are comparatively a little bit high in cost, 
functionality is cost-effective.

****

Two access transistors and two cross-coupled inverters are 
present in the traditional 6- Transistor SRAM cell. The latch is 
formed with these two cross-coupled inverters. The cross-coupled 
inverters consist of four transistors, each store 1 bit of data in 
SRAM. This latch formed by inverters is shown in Figure 2.1. The
word line (WL) is connected to two gate terminals of access 
transistors. Latch inputs of the SRAM cell are bound to pass 
transistors drain terminals of both sides. The bit line (BL) is 
connected to one pass transistor source, and the bit line bar (BLB) is 
connected to the source terminal of another one. Access transistors 
are ON when WL=1, that is the word line is high, so the bit lines 
will be attached to the latch then operations of read and write will be done. The access transistors are said to be OFF when WL=0; that 
is the word line is low so that the bit lines will be disconnected from
the latch. The bit stored in the latch is in the hold under VDD and 
GND's voltage in this situation. Figure 
![6t sram](https://user-images.githubusercontent.com/85571828/155920389-58ba797e-6a83-481b-9f9b-e767cc3e2cfc.jpg)6T SRAM CELL 

