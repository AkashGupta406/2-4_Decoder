# Implementation of 2:4 Decoder using 28nm CMOS Technology

The 2:4 Decoder is designed using 28nm CMOS technology by using Synopsys Custom Compiler

# Table of Content
- [Abstract](#Abstract)
- [Introduction](#Introduction)
- [Tools Used](#Tools_Used)
- [2:4 Decoder Circuit Design](#2-4_Decoder_Circuit_Design)
- [CMOS 1:2 Decoder](#CMOS_1:2_Decoder)
- [CMOS 2:4 Decoder](#CMOS_2:4_Decoder)
- [Netlist](#Netlist)
- [Acknowledgement](#Acknowledgement)
- [References](#References)

# Abstract
In this paper, I have discussed the designing as well as the implementation of a 2:4 Decoder using the CMOS logic family. Its implementation will be done using the 28nm Synopsis Custom Design Platform. A decoder circuit changes a code into a set of signals. It is called decoder because it does the reverse of encoding. We can verify output using  the waveforms obtained from the circuit. Here we are using the CMOS technology because it has very low static power generation, high density of logicfunctions on chip, small size and good noise immunity.

# Introduction
The fundamental digital module is the decoder which decodes the coded input which is generally used in the all types of memory devices. Most common decoder circuit is an n input to 2^n output binary decoder. In the conventional design the CMOS technology is used to design the logic of any application

![2-to-4-binary-decoder](https://user-images.githubusercontent.com/96524064/156178958-7f741688-3732-4c8a-9c6a-60dfb9089ba4.jpg)
![gate_level_decoder](https://user-images.githubusercontent.com/96524064/156178991-6a893025-9c08-49e6-a525-e0098dd0d116.png)

The binary inputs A0 and A1 determine which output line from D0 to D3 is “HIGH” at logic level “1” while the remaining outputs are held “LOW” at logic “0” so only one output can be active (HIGH) at any one time. Therefore, whichever output line is “HIGH” identifies the binary code present at the input, in other words it “de-codes” the binary input.

# Tools_Used
- Synopsys Custom Compiler :  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Primewave :  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK :  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# 2-4_Decoder_Circuit_Design
## 1:2 decoder using NOR Gates

![Nor_decoder](https://user-images.githubusercontent.com/96524064/156181455-3aa880ff-618d-4e6f-bc29-9470cef642aa.png)

## Reference Circuit of 1:2 decoder using Static CMOS logic

![DEC_reference](https://user-images.githubusercontent.com/96524064/156185318-e6243486-4526-48ad-879f-99fe04995f16.jpeg)

## 2:4 decoder implementation using 1:2 decoders

![2_4_using_1_2](https://user-images.githubusercontent.com/96524064/156184232-e0c05155-6bd5-4f51-8291-64200e1a1a4d.png)

# CMOS_1:2_Decoder
## Implementation of 1:2 decoder in Synopsys Custom Compiler
### Symbol

![12dec_symbol](https://user-images.githubusercontent.com/96524064/156190303-af1799f3-33f7-4f0f-81e5-c1fdd7b48d8c.jpeg)

### Schematic

![12dec_schematic](https://user-images.githubusercontent.com/96524064/156190358-aa06c35e-cd9d-453b-8f3d-7a8f8dd73971.jpeg)

### TestBench Symbol

![12dec_tb](https://user-images.githubusercontent.com/96524064/156190493-e54f01e2-9c82-4f99-ad66-38d1daff0efb.jpeg)

### TestBench Waveform

![12dec_waveform](https://user-images.githubusercontent.com/96524064/156190508-5ae79575-1b15-4873-a20e-e7c67f7eee5b.jpeg)

# CMOS_2:4_Decoder
## Implementation of 2:4 Decoder using 1:2 Decoders in Synopsys Custom Compiler
### Symbol

![24_dec_symbol](https://user-images.githubusercontent.com/96524064/156191189-45e5f8fd-f5d8-430a-93e4-a09342ee18bc.jpeg)

### Schematic

![24_dec_schematic](https://user-images.githubusercontent.com/96524064/156191215-edc88fa9-7d54-41c2-b8e4-00945ed8b279.jpeg)

### TestBench Symbol

![24_dec_tb](https://user-images.githubusercontent.com/96524064/156191248-abeb8311-6835-48aa-a818-acb2d6a24ed2.jpeg)

### TestBench Waveform

![24_dec_waveform](https://user-images.githubusercontent.com/96524064/156191271-6d95254a-81ce-4f8f-a596-15e32dcdac5a.jpeg)

# Netlist
## Netlist for 1:2 Decoder
*  Generated for: PrimeSim
*  Design library name: 2_1_Decoder
*  Design cell name: 2_1_dec_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 02:51:07 2022

.global gnd!
********************************************************************************
* Library          : 2_1_Decoder
* Cell             : 2_1_dec
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _2_1_dec gbar s vdd vss y0 y1
xm8 net46 s vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm3 y1 net46 net13 vdd p105 w=0.1u l=0.03u nf=1 m=1
xm2 y0 s net9 vdd p105 w=0.1u l=0.03u nf=1 m=1
xm1 net13 gbar vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm0 net9 gbar vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm9 net46 s vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm7 y1 net46 vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm6 y1 gbar vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm5 y0 s vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm4 y0 gbar vss vss n105 w=0.1u l=0.03u nf=1 m=1
.ends _2_1_dec

********************************************************************************
* Library          : 2_1_Decoder
* Cell             : 2_1_dec_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 net11 vin net7 gnd! vout0 vout1 _2_1_dec
v1 net7 gnd! dc=5
v3 net11 gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 5u 10u )
v2 vin gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 5u 10u )
c5 vout0 gnd! c=1p
c4 vout1 gnd! c=1p








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(vin) v(vout0) v(vout1)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

## Netlist for 2:4 Decoder
*  Generated for: PrimeSim
*  Design library name: 2_1_Decoder
*  Design cell name: 2_4_decoder_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 09:24:43 2022

.global gnd!
********************************************************************************
* Library          : 2_1_Decoder
* Cell             : 2_1_dec
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _2_1_dec gbar s vdd vss y0 y1
xm8 net46 s vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm3 y1 net46 net13 vdd p105 w=0.1u l=0.03u nf=1 m=1
xm2 y0 s net9 vdd p105 w=0.1u l=0.03u nf=1 m=1
xm1 net13 gbar vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm0 net9 gbar vdd vdd p105 w=0.1u l=0.03u nf=1 m=1
xm9 net46 s vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm7 y1 net46 vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm6 y1 gbar vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm5 y0 s vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm4 y0 gbar vss vss n105 w=0.1u l=0.03u nf=1 m=1
.ends _2_1_dec

********************************************************************************
* Library          : 2_1_Decoder
* Cell             : 2_4_decoder
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _2_4_decoder a b d0 d1 d2 d3 gbar vdd vss
xi2 gbar a vdd vss net15 net13 _2_1_dec
xi1 net13 b vdd vss d2 d3 _2_1_dec
xi0 net15 b vdd vss d0 d1 _2_1_dec
.ends _2_4_decoder

********************************************************************************
* Library          : 2_1_Decoder
* Cell             : 2_4_decoder_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 vin0 vin1 vout0 vout1 vout2 vout3 net39 net41 gnd! _2_4_decoder
v24 net41 gnd! dc=5
v26 vin0 gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 5u 10u )
v5 net39 gnd! dc=0 pulse ( 0 1.05u 0 0.1u 0.1u 5u 10u )
v27 vin1 gnd! dc=0 pulse ( 0 1.05 0 0.1u 0.1u 10u 20u )
c31 vout3 gnd! c=5p
c30 vout2 gnd! c=5p
c29 vout1 gnd! c=5p
c28 vout0 gnd! c=5p








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(vin0) v(vin1) v(vout0) v(vout1) v(vout2) v(vout3)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

# Acknowledgement
- Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
- Synopsys, India
- VLSI System Design(VSD) Corporation Private Limited India
- Indian Institute of Technology, Hyderabad
- Cloud Based Analog IC Design Hackathon
- Sameer Durgoji, NIT Karnataka
- Chinmay panda, IIT Hyderabad
# References
1. DimitriosBalobas and Nikos Konofaos, “Design of Low- Power High Performance 2-4 and 4-16 Mixed-Logic Line decoders”, IEEE J. Circuits and Systems, vol.64, no. 2, Feb.2017.
2. Weste and D. M. Harris, CMOS VLSI Design, a Circuits and Systems Perspective 4th ed Boston, MA, USA: AddisonWesley,2011







