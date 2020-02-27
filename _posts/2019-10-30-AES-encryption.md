---
layout: post
title: AES Encryption
tags: [FPGA, SystemVerilog, encryption]
---

For my microprocessor-based systems class, I had one week to write a hardward accelerator to perform 128-bit AES encryption. First, I had to learn about AES from the Federal Information Processing Standards (FIPS) documentation. After reading their description of AES, I implemented it in SystemVerilog to run on a Cyclone IV FPGA. I had to implement the system efficiently so that it would fit on the FPGA. A block diagram of the encryption logic is shown below:

*picture*

The completed system used both a microcontroller and FPGA. First, the microcontroller sent over a message and key from one of FIPS's known answer tests over SPI. The FPGA then encrypted the data and sent it back over SPI. The microconroller checked the encrypted message to ensure that it matched up with the known answer, and lit up a green LED to indicate that the encryption was correct. Before testing the completed system, however, I simulated my System Verilog using ModelSim.

If you want to read more about this project, here's my page-long [report](https://docs.google.com/document/d/1tOqIiKSgTtSrEarCyQiouib9EoZr7X_IT_qe3KH0FcQ/edit?usp=sharing).
