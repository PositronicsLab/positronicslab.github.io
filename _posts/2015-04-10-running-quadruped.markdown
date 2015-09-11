---
layout: post
title:  "Running with a simulated quadruped"
date:   2014-08-01
---

<p class="intro"><span class="dropcap">W</span>e use <a href="http://github.com/PositronicsLab/Pacer">Pacer</a> to make a simulated robot run while using:
    joint error-feedback (PID) control (unilateral contact with friction)
    inverse dynamics (unilateral contact with friction)
    inverted pendulum error-feedback (PID) stabilization (compressive and frictional ground reaction forces)

The direction that the robot heads is determined online using human inputs.  The robot runs toward a waypoint 10 meters in front of its starting position.

Running at 0.5 m/s (1.1 mph):

<a href="http://www.youtube.com/watch?feature=player_embedded&v=OKvNG_Zudw0
" target="_blank"><img src="http://img.youtube.com/vi/OKvNG_Zudw0/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="400" border="10" /></a>

Running at 1 – 1.5 m/s (2.2 - 3.3 mph):

<a href="http://www.youtube.com/watch?feature=player_embedded&v=B3z7lRnhmzU
" target="_blank"><img src="http://img.youtube.com/vi/B3z7lRnhmzU/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="400" border="10" /></a>

Scaling the R. Links robot up to the size of Big Dog (Boston Dynamics) or HyQ (IIT)—both are roughly 1 meter in length— is equivalent to a 10 mph run.

Performed using **Pacer**.

Project page:
<a title="https://github.com/PositronicsLab/Pacer" href="https://github.com/PositronicsLab/Pacer">https://github.com/PositronicsLab/Pacer</a>


