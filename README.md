# Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology
1.[ABSTRACT](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#ABSRACT)

2.[LITERATURE SURVEY](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#LITERATURE-SURVEY)

3.[WORKING](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#WORKING)

4.[DESIGN](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#DESIGN)

5.[NETLIST](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#NETLIST)

6.[WAVEFORMS](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#WAVEFORMS)

7.[ACKNOWLEDGEMENT](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#ACKNOWLEDGEMENT)

8.[REFERENCES](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/edit/main/README.md#REFERENCES)

**ABSRACT**

Memories are the crucial blocks in VLSI system 
design. The performance, power, and area of memories should 
be carefully inspected before fabrication of the system. In digital 
processors, we use SRAM cells in the memory cache for faster 
performance and low power consumption. 6T SRAM cell is 
designed with Synopsys Design Compiler using 28nm CMOS 
technology

**LITERATURE SURVEY**

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
**WORKING**


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
GND's voltage in this situation.

**DESIGN**

**6T SRAM CELL** 

![6t sram](https://user-images.githubusercontent.com/85571828/155920389-58ba797e-6a83-481b-9f9b-e767cc3e2cfc.jpg) 
                                                                                                 

**Shematic Representation of SRAM CELL**

![SRAM_CELL_SCHEMATIC](https://user-images.githubusercontent.com/85571828/155921219-55d5698b-ae1d-4b50-847b-e86b8e0566f4.JPG)

**Symbol representation of SRAM CELL**

![SRAM_CELL_SYMBOL](https://user-images.githubusercontent.com/85571828/155921283-46a531c4-b11f-4c63-ba91-731433131cc1.JPG)


**Schematic Represenation of Read Operation**

![READ SCHEMATIC](https://user-images.githubusercontent.com/85571828/155921387-5bd706a7-57f7-4538-be47-18fa45c40746.JPG)

Read operation of 6T SRAM CELL will be done by making the word line high. By making the WWL high the two access transistors will be turned on. Both the BITLINE and BITLINE -BAR has to be pre-charged to observe the data which is stored in storage latch. If the storge node Q is high, then the capacitor connected to BITLINE will remain same and at the same time the capacitor connected to BITLINE-BAR will be discharged. By observing this we can find the stored data.


**Schematic Represenation of Write Operation**

![WRITE _SCHEMATIC](https://user-images.githubusercontent.com/85571828/155921457-b0c4e9d0-06ca-4fbd-8036-314bba2b5017.JPG)

Write operation of 6T SRAM CELL will be performed by making the word line is high. If storage node Q is 0, then pre-charge BL to logic high and BLB to logic zero. Access transistors will be turned on by making the word line high. Storage node Q charges through the access transistor and flips the data stored in Q. Storage node QB will be discharged through the access transistor N4 via bit line bar and changes the stored data from 1 to 0. In the other scenario BL has to precharged to zero and BLB to logic high.

**NETLIST** 

[NETLIST](https://github.com/prasanthmandadi/Design-of-6T-SRAM-Cell-at-28nm-CMOS-Technology/tree/main/Netlist)

**WAVEFORMS**

**Waveform of read Operation**

![Read waveform](https://user-images.githubusercontent.com/85571828/155921617-c51a0400-c33a-4c4d-b319-009fa9e74dc7.JPG)

In this Read operation Transient analysis waveform we can observe whenever the WWL is high, BL and BLB are changing. The logic 1 at storage node Q is charging the capacitor connected to BL and logic 0 at storage node Q is discharging the capacitor connected to BLB (vice versa). BL and BLB are also opposite to each other. BL is following Q and BLB is following the QB.

**Waveform of Write Operation**

![write Waveform](https://user-images.githubusercontent.com/85571828/155921677-254a6cc9-87a8-4354-bd78-bbe57cf539fc.JPG)

In this Write operation Transient analysis waveform we can observe whenever the WWL is high, Q and QB are changing. Input pulse waves are given to BL and BLB and observed both storage nodes Q and QB. The BL logic high making storage node Q as logic 1 and BLB logic low making storage node QB as logic 0 (vice versa). Q and QB are opposite to each other

**ACKNOWLEDGEMENT**

1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd
2. https://hackathoniith.in/ 

**REFERENCES**
[1] P. Chodankar, I. Suryavanshi, and A. Gangad, "Low power SRAM 
design using independent gate FinFET at 30nm technology," 2014 First 
International Conference on Computational Systems and 
Communications (ICCSC), Trivandrum, 2014, pp. 52-56.

[2] Sanjana S R, Balaji Ramakrishna s, Smaiksha, Roohila Banu, Prateek 
Shubham "Design and performance analysis of 6T SRAM cell in 22nm 
CMOS and FinFET technology Nodes" DOI 10.1109/ICRAECT, 2017.

[3] H. Afzali-Kusha, A. Shafaei, and M. Pedram, "A 125mV 2ns-accesstime 16Kb SRAM design based on a 6T hybrid TFET-FinFET cell," 
2018 19th International Symposium on Quality Electronic Design 
(ISQED), Santa Clara, CA, USA, 2018, pp. 280-285, doi: 
10.1109/ISQED.2018.8357301.

[4] A. Bhaskar, "Design and analysis of low power SRAM cells," 2017 
Innovations in Power and Advanced Computing Technologies (iPACT), 2017, pp. 1-5, doi: 10.1109/IPACT.2017.8244888.
[5] Rohit kumar shah, Inamul Hussain, Manish Kumar “Performance 
analysis of 6T SRAM Cell in 180nm CMOS Technology"









