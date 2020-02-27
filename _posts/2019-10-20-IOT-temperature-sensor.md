---
layout: post
title: IOT Temperature Sensor
tags: [microprocessor, IOT, C, oscilloscope]
---

For my microprocessor-based systems class, I had one week to create a website that displayed the temperature reading of a thermometer. I used a microcontroller, which communicated with the temperature sensor via SPI and a Wifi module via UART.

While I had access to libraries for UART and other peripherals of the microcontroller, I had to read the microcontroller's data sheet to understand how to use the SPI peripheral and write a library for it. Additionally, I had to read the temperature sensor's datasheet to learn how to configure it and interpret its readings sent over SPI. To debug the system, I used a logic analyzer, which allowed me to see the MISO, MOSI, chip select, and clock signals. 

![la](/img/logic-analyzer.png){: .center-block :}

If you want to read more about this project, here's my page-long [report](https://docs.google.com/document/d/1eg0gZg9qPaul1MorkwRDgC_HZFQ_hzjwUpu6XFahmQA/edit?usp=sharing).
