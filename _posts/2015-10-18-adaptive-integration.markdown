---
layout: post
title:  "Adaptive Integration for Controlling Speed vs. Accuracy in Multi-Rigid Body Simulation"
date:   2015-10-17
---

<p class="intro"><span class="dropcap">T</span>he speed of time stepping-based, multi-rigid body simulations with contact seems to be reaching a performance asymptote. Wang (2013) profiled such
a simulation (using Gazebo/ODE) modeling multiple robotic scenarios and
found that the bulk of running time goes to processes related to the
constraint (contact, joint limit, and joint equations) solve.</p> 

This process has received considerable attention from both researchers and implementors, and large further improvements seem unlikely, at least in our area of
interest (simulating typical manipulator, legged, and humanoid robots).
*Given that it is unlikely to reduce the computational time to take an integration step, this research sought to find whether larger steps could be taken for simulating typical manipulator, legged, and humanoid robots.*

## Notions of accuracy of dynamic robotic simulations with contact

Our target application presents a particular challenge: the simulation must update at a step size smaller than the inverse of a robot's control loop frequency (we do not wish to restrict control inputs to be smooth).
Typical control loop frequencies for such robots are on the order of 1000 Hz. Such speeds yield small steps and generally low truncation error even with first order integration.


#### What are the practical implications when solution accuracy is not high?

The practical implications of lower differential algebraic equation (DAE) / differential complementarity problem (dCP) solution accuracy on robotics applications is an open problem, even for robots with smooth or mostly smooth dynamics. Instead, we consider a different form of accuracy by working to ensure that nonsmooth events (impacts, for example) occur only at the endpoints of an integration time interval. 

#### We want the fastest simulation speed possible without artifacts

Our paper (Zapolsky and Drumwright, 2015) relaxes the notion of accuracy even further by seeking only to avoid clearly recognizable artifacts that occur with time stepping approaches: objects interpenetrating and objects passing completely through one another (tunneling). We do not *currently* search for transitions between sticking and slipping contact, because we believe that the effects of these transitions on solution accuracy are typically small.   

#### Preventing tunneling and interpenetration

Our simulation approach uses Mirtich's Conservative Advancement technique to prevent  partial interpenetration and tunneling. Our approach extends Mirtich's thesis by no longer requiring bodies in sustained contact to be constantly moving (i.e., no "microcollisions" are necessary).

## Adaptive integration technique

Our research uses the approach described above and standard error control techniques to integrate adaptively. If our argument that DAE/dCP solution accuracy is less important than prevention of artifacts is reasonable and if an interval is free of nonsmooth events, then the main inhibitor of larger steps is stability of the integration algorithm. We avoid implicit integration algorithms: they are both computationally expensive and cannot readily be extended to prevent tunneling. We instead using an adaptive first order integrator with an estimate of the local error in kinetic energy as a proxy for system stability.  

## Our findings

* Local error in system kinetic energy seems to be a reasonable proxy for system stability: if the integration becomes unstable, the kinetic energy will grow exponentially over a small time interval.
* We can get 2x-3x larger step sizes for simulating a walking quadrupedal robot, but are doing 3x as much computation on each step (this can conceivably be reduced to 2x as much work using parallelism). 
* An experiment with a passive dynamic walker (Coleman et al., 2001) indicates that applying higher order integration techniques to simulating robots (modeled with rigid body dynamics and undergoing intermittent contact) is unlikely to be computationally efficient compared to current first-order approaches. 
* As we expected, the symplectic nature of the semi-implicit integrator does not positively impact stability on non-Hamiltonian systems (i.e., most robots).
* We can attain integrate with far larger step sizes stably and without obvious artifacts by removing substantial kinetic energy from the system. Practical and theoretical effects on the generated solution are currently unknown.    

![Trotting stability](http://positronicslab.github.io/assets/img/iros15-walking-stability.png)
<p>Simulation stability (using the proxy of estimated local error in kinetic energy) during a trotting motion of the robot shown below.</p>
![Trotting depiction](http://positronicslab.github.io/assets/img/iros15-walking-depiction.png)


##### Relevant Publications:

Michael J. Coleman, Mariano Garcia, Katja Mombaur, and Andy Ruina. "Prediction of stable walking for a toy that cannot stand." *Phys. Review. E*, 64(2), 2001.

Jielie Wang. "Dynamic grasp analysis and profiling of Gazebo". M.S. Thesis, Rennselaer Polytechnic Institute, 2013.

Samuel Zapolsky and Evan M. Drumwright. "Adaptive Integration for Controlling Speed vs. Accuracy in Multi-Rigid Body Simulation". <i>Proc. of the IEEE/RSJ Intl. Conf. on Intelligent Robots and Systems</i>. Hamburg, 2015. [<a href="http://positronicslab.github.io/assets/pdfs/adaptive-integration-iros-2015.pdf">pdf</a>]

##### Code and data for reproducing experiments:

All code and data for reproducing experiments can be obtained from [this](http://github.com/PositronicsLab) git repository.

*Special thanks to [Michael Sherman](https://simtk.org/home/simbody/) for discussion that has shaped this document.*