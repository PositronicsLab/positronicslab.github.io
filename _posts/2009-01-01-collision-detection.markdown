---
layout: post
title:  "Continuous collision detection"
date:   2009-01-01
---
<p class="intro"><span class="dropcap">C</span>ontinuous collision detection (CCD) permits accurate time of contact determination and
computation of contact data (points and normals) in multi-rigid body
simulation. CCD methods are also usable for motion planning algorithms.
Our method works with any type of geometric representation: triangle meshes,
constructive solid geometries (CSGs), primitives, and even fractals.
The CCD method's running time compares favorably to existing
continuous collision detection schemes that only treat triangle meshes.</p>

<img src="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/tunneling.png" alt="" width="100%" />

<small>Still from <i>bullets.mov</i> showing a number of "bullets" fired at
a stationary gun
emplacement (this is a hard problem for <i>discrete</i> collision
detection approaches) using rigid body dynamics. The bullets that
hit the gun emplacement are properly deflected.</small>

<b>Videos:</b>

<a href="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/bullets.mov">[bullets.mov]</a>
<ul>(3 MB) Bullets fired at gun emplacement</ul>
<b>Relevant publications:</b>
<ul>
<li>Dylan Shell and Evan Drumwright.
"Precise Generalized Contact Point and Normal Determination
for Rigid Body Simulation". <i>Proc. of the 24th ACM Symp.
on Applied Computing (SAC).</i> Honolulu, 2009.</li>
</ul>