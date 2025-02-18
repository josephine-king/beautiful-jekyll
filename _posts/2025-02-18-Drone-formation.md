# State Estimation for Multi-Agent Drone Formation  

**February 2025**  

For this project, my teammate and I worked on state estimation for a multi-agent drone formation system. Given a set of drones that need to move into a predefined formation, we aimed to estimate their positions from noisy relative measurements and control their movement accordingly. This project was entirely simulation-based and implemented in Python.  

## The Problem  

In an ideal world, we would know the exact positions of all drones at every time step. In reality, however, we only have access to noisy measurements of their relative distances. Our goal was to estimate each drone’s absolute position as accurately as possible, allowing them to navigate smoothly to their target locations.  

## The Approach  

Our project was based on the master’s thesis *Edge State Kalman Filtering for Distributed Formation Control Systems* by Martijn van der Marel ([link](https://repository.tudelft.nl/record/uuid:705740b7-6349-42fd-a5f2-f9e8e2280290)). We implemented and compared four different estimators:  

- **Least Squares (LS):** Computes the best-fit solution by minimizing squared measurement errors.  
- **Best Linear Unbiased Estimator (BLUE):** A weighted least squares approach that incorporates measurement noise covariance.  
- **Averaging Estimator:** Computes multiple LS estimates over time and averages them.  
- **Kalman Filter:** A recursive estimator that updates state predictions over time using new measurements.  

## The Results  

All estimators successfully guided the drones to their target positions, but their performance varied. The Kalman filter produced the smoothest drone trajectories and required the least control input, making it the most efficient option. However, it was also the most computationally expensive. The LS and BLUE estimators were simpler and still significantly improved trajectory smoothness compared to having no estimator at all.  

## Key Takeaways  

This project demonstrated the importance of state estimation in multi-agent systems, particularly when working with noisy measurements. While simple estimators like LS can work well in many cases, the Kalman filter’s ability to incorporate past state estimates made it the most effective for minimizing noise effects.  

For more details, check out our full [report](https://josephine-king.github.io/2025-02-18-Drone-formation-report/) and [code](https://github.com/josephine-king/ET4386_drone_formation).  

