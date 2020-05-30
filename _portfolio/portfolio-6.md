---
title: "Statically Indeterminate Leveling Strategy for Vehicle Leveling System"
excerpt: "This project built a new statically indeterminate leveling strategy for vehicle leveling system in Matlab Simulink.<br/><img src='/images/level_strategy.jpg'>"
collection: portfolio
---

# Overview
The automatic leveling strategy is the technical core of the automatic leveling system. The automatic leveling strategy refers to the automatic control of the sequence and mode of each leg according to the program, and finally reaches the state where the horizontal accuracy of the platform is zero. A good automatic leveling strategy should have the characteristics of high leveling precision, fast leveling, good leveling reliability, and small leveling overshoot. The leveling accuracy, leveling speed and leveling overshoot control can be achieved at the program aspect of the automatic leveling strategy, but the improvement of leveling reliability often needs to be achieved by increasing the number of legs, but according to the principle that three points determine a plane, when the number of legs exceeds three, it will lead to a leg in the state of virtual support, and finally cause the problem of the virtual leg named static indeterminacy. Therefore, it is very important to propose an automatic leveling strategy with high leveling speed, high leveling precision and avoiding virtual leg problems to improve leveling reliability.

# What I Did
The core of the leveling strategy is to use predictive control to chase the highest point to level, through continuous feedback of the angle signal, and finally achieve leveling. Before the leveling begins, the horizontal inclination angle is detected first, and the highest leg is judged. After that, the highest leg is extended by 10 mm firstly, and then the four legs are started to be lifted at the same time. When the angle changes suddenly, all four legs stop lifting, and then lift the diagonal legs of the highest leg until the horizontal inclination of the X or Y axis is 0. After that, judge the horizontal inclination angle according to different horizontal inclination angles and extend the corresponding two legs until the other horizontal inclination angle is also 0. At this time, the leveling ends.

# Results
The conclusion is that the leveling strategy has shorter leveling time and the possibility of virtual legs is small. The X and Y angles of the leveling strategy are also analyzed. The biggest adjustable angles are 5.19° and 3.43°. Then the feasibility of the leveling strategy under various angles is analyzed, and the conclusion is that the leveling strategy is applicable to all angles.

# Codes and Simulink Model
See codes and simulink model [here](https://github.com/ZhishengLin2020/statically-indeterminate-leveling-strategy-for-vehicle-leveling-system).
