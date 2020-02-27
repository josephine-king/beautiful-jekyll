---
layout: post
title: MPC Path Planning
tags: [robotics, MATLAB]
---

For our final project in Optimization Techniques in Engineering, my partner and I chose to create an MPC controller in MATLAB. We chose to simulate a bicycle, but to simplify the project we did not take into account the bicycle's vertical rotation or stability. (This would be a cool extension of the project though!) We used MATLAB's nonlinear MPC toolbox and added our own system model, constraints, and cost function. 

To get the bicycle to move along the path, we created a cost function that would minimize the bicycle's deviation from the path and cause it to move at a constant speed. Our biggest challenge was creating the path from a set of waypoints. While we could have created a bicycle that moves straight from one waypoint to another, this would have resulted in an oddly angular path, and we wanted our robot to be as smooth and natural as possible. To create the path, we fit a polynomial to the bicycle's next three waypoints using MATLAB's curve fitting toolbox. However, polynomial fitting presented many challenges. If the next three waypoints were not well-fit, the bicycle would veer away from the waypoints and off to infinity, never to be seen again. As a result, our bicycle was better at following some paths than others. To fix this problem, we could have put waypoints closer together, which would have resulted in more linear and easily-fitted curves. Or, we could have created a more intelligent curve fitter altogether. In the gifs below, you can see that the bicycle actually completes the figure eight quite nicely, but struggles with the hexagon. To read more about this project, here's our [final report](https://drive.google.com/file/d/1xEwR4SH4WZNW4BjL8p1rl1gfJRZ_duRR/view?usp=sharing). 

![fig-eight](/img/figure_eight.gif){: .center-block :}

![hex](/img/hexagon.gif){: .center-block :}

