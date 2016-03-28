---
layout: post
title:  "Dynamic robotic simulation"
category: simulation
date:   2010-01-01
---

<h3>O(n<sup>3</sup>) convex complementarity-free contact model</h3>
Our multi-rigid body
contact model requires time O(n<sup>3</sup>) in
the number of contact points to solve. Using any one of numerous widely
available interior point solvers yields numerical robustness,
true friction cones, and scaling to
thousands of contact points.

<img src="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/grasp.png" alt="" width="100%" />
<small>
Frame from <i>grasp.mp4</i> showing simulated manipulator grasping a
ball (notoriously difficult to simulate) while moving in a sinusoidal
trajectory. Our contact model is employed.
</small>

<b>Videos:</b>
<ul>
<li><a href="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/grasp.mp4">[grasp.mp4]</a> (1.5MB) Robot grasping</li>
</ul>
<b>Relevant publications:</b>
<ul>
<li>Evan Drumwright and Dylan Shell.
<a href="papers/WAFR10.pdf">Modeling Contact Friction and Joint
Friction in Dynamic
Robotic Simulation Using the Principle of Maximum Dissipation</a>.
<i>Proc. of the Ninth Intl. Workshop on the Algorithmic
Foundations of Robotics (WAFR).</i> Singapore, 2010.</li>
<li>Evan Drumwright and Dylan Shell.
"A Robust and Tractable Contact Model for Robotic Simulation".
<i>Proc. of the 24th ACM Symp.
on Applied Computing (SAC).</i> Honolulu, 2009.</li>
</ul>

<hr />

<h3>Advanced penalty method for rigid body simulation</h3>
Our advanced penalty method works by applying forces over the volume
of penetration, rather than applying a force due to only a single,
virtual spring and damper at the point of deepest penetration.
Applying forces at multiple points reduces the
oscillation that emerges from the standard penalty-based approach.
An integrative reduces steady-state error, permitting
less stiff gain constants to be used for the virtual springs and
dampers; the resulting equations of motion are less "stiff".

<img src="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/pile.png" alt="" width="100%" />

<small>A still from a video that demonstrates the ability of the advanced
penalty method to handle a stable pile of objects.</small>

Relevant publication:
<ul>
<li>Evan Drumwright.
<a href="http://robotics.usc.edu/~drumwrig/tvcg.pdf">A Fast
and Stable Penalty Method for Rigid Body Simulation</a>.
<i>IEEE Trans. on Visualization and Computer Graphics</i>.
vol. 14, no. 1, pp. 231-240, January/February, 2008.</li>
</ul>
