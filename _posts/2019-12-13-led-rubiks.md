I created this LED Rubik's cube with my partner, Aaron Trujillo, as a final project for my Microprocessor-Based Systems and Design class. We had 5 weeks to design and build the project, and had to use both a microcontroller and an FPGA in a meaningful way. Before diving into the technical aspects of our project, I'll briefly explain the concept behind our LED Rubik's Cube. 

![cube-drawing](/img/cube-drawing.png){: .center-block :}

Unlike a traditional Rubik's Cube, the faces can't rotate. Instead, the user selects a button corresponding to the center color of the face they wish to rotate. Then, they can rotate that face clockwise or counter-clockwise by rotating the rotary encoder, which is a knob on the control panel. The reset button can be used to either scramble or solve the cube, depending on what state it's in. 

![block-diagram](/img/block-diagram.png){: .center-block :}

We used the microprocessor to read in user inputs from buttons and the rotary encoder. Based on this input, the microcontroller performed a rotation to determine the cube's new configuration, and sent this configuration over SPI to the FPGA. The FPGA then programmed the LEDs to their new configuration.

![rubiks-photo](/img/rubiks-photo.png){: .center-block :}

Our cube worked really well! It was harder to solve than a typical cube because users couldn't rely on muscle memory. However, our cube had the advantage of auto-scrambling and solving. If we had more time, it would have been cool to add hints to help the user solve the cube. If you want to read more about our LED Rubik's cube, here's our [final report](https://docs.google.com/document/d/1rmvRuqucuzeL6A910gxYJRkemZ9fJw8w-6kyjTsIOw4/edit?usp=sharing). 



