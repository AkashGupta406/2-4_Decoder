# Implementation of 2:4 Decoder using 28nm CMOS Technology

The 2:4 Decoder is designed using 28nm CMOS technology by using Synopsys Custom Compiler

# Table of Content
- Abstract
- Introduction
- Tools Used
- 2:4 Decoder Circuit Design
- CMOS 1:2 Decoder
- CMOS 2:4 Decoder
- Simulation Result
- Netlist
- Acknowledgement
- Reference

# Abstract
In this paper, I have discussed the designing as well as the implementation of a 2:4 Decoder using the CMOS logic family. Its implementation will be done using the 28nm Synopsis Custom Design Platform. A decoder circuit changes a code into a set of signals. It is called decoder because it does the reverse of encoding. We can verify output using  the waveforms obtained from the circuit. Here we are using the CMOS technology because it has very low static power generation, high density of logicfunctions on chip, small size and good noise immunity.

# Introduction
The fundamental digital module is the decoder which decodes the coded input which is generally used in the all types of memory devices. Most common decoder circuit is an n input to 2^n output binary decoder. In the conventional design the CMOS technology is used to design the logic of any application

![2-to-4-binary-decoder](https://user-images.githubusercontent.com/96524064/156178958-7f741688-3732-4c8a-9c6a-60dfb9089ba4.jpg)
![gate_level_decoder](https://user-images.githubusercontent.com/96524064/156178991-6a893025-9c08-49e6-a525-e0098dd0d116.png)

The binary inputs A0 and A1 determine which output line from D0 to D3 is “HIGH” at logic level “1” while the remaining outputs are held “LOW” at logic “0” so only one output can be active (HIGH) at any one time. Therefore, whichever output line is “HIGH” identifies the binary code present at the input, in other words it “de-codes” the binary input.

# Tool Used
- Synopsys Custom Compiler :  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- Synopsys Primewave :  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- Synopsys 28nm PDK :  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.

# 2:4 Decoder Design
## 1:2 decoder using NOR Gates

![Nor_decoder](https://user-images.githubusercontent.com/96524064/156181455-3aa880ff-618d-4e6f-bc29-9470cef642aa.png)

## Reference Circuit of 1:2 decoder using Static CMOS logic

![DEC_reference](https://user-images.githubusercontent.com/96524064/156185318-e6243486-4526-48ad-879f-99fe04995f16.jpeg)

## 2:4 decoder implementation using 1:2 decoders

![2_4_using_1_2](https://user-images.githubusercontent.com/96524064/156184232-e0c05155-6bd5-4f51-8291-64200e1a1a4d.png)

# CMOS 1:2 Decoder
## Implementation of 1:2 decoder in Synopsys Custom Compiler
- Schematic

- Symbol

- TestBench Symbol

- TestBench Waveform

## Implementation of 2:4 Decoder using 1:2 Decoders in Synopsys Custom Compiler
- Schematic

- Symbol

- TestBench Symbol

- TestBench Waveform





