---
layout: post
title: Phase Change Memory Research
tags: design, simulation, analog circuits
---

I spent the summer of 2018 researching phase change memory (PCM), which is an emerging memory technology. PCM is promising memory technology because it is high density and low cost. To store data, PCM uses a phase change material, which switches between a low-resistance crystalline state and a high-resistance amorphous state. A short, high temperature pulse rearranges the crystal lattice into its high-resistance state, while a long, low temperature pulse allows the material to recrystallize into its low-resistance state. To apply these temperatures, we give the cells voltage pulses of different magnitudes and durations. To read memory, a low current is applied through the cells and the voltage of the bitlines is measured. 

*photo

In order to prevent current from flowing in undesired directions, we add a "selector" in series with the phase change memory cell. Transistors or diodes could be used to "select" the direction of current flow. Transistors are much larger than diodes, and would therefore take away from PCM's high density. Thus, we used a selector diode to prevent unwanted currents. However, these diodes are not perfect and still allow some current to flow in undesired directions, called "sneak paths." The effect of sneak paths worsens as the array gets larger, so I simulated PCM arrays to determine at what size the array begins to break down because of sneak paths.

*photo

Over the course of the summer, I improved both the selector diode and phase change material models to adhere to experimental data. I found that a very (unrealistically) good diode is needed to prevent sneak paths at even small array sizes. Since that summer, I've been continuing this research alongside my courses.

*photo
