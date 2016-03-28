---
layout: post
title:  "Mobile manipulation"
category: manipulation
date:   2012-06-01
---
<h3>Load equalization via proprioceptive force feedback</h3>
<p class="intro"><span class="dropcap">O</span>ur latest research with <b>Pepe</b>, our <a href="http://www.willowgarage.com/pages/pr2/overview">PR2</a> robot from <a href="http://www.willowgarage.com">Willow Garage</a>, has focused on manipulating bulky objects for which prehensile grasping strategies may be infeasible: in such cases, we may be able to constrain manipulated objects only <i>unilaterally</i> in some directions.</p>

We recently focused on equalizing bulky loads applied to the PR2's arms, which would be useful for humanoid dynamic balancing and reducing robot energy consumption. Our simple and robust reactive strategy uses proprioceptive force feedback and manipulation with the arms (not the grippers) to yield exceptional performance: the robot never fails to
equalize a load in over 75 experimental trials.

<img src="http://robotics.gwu.edu/positronics/wp-content/uploads/2013/08/pepe-loadbalance.png" alt="" width="100%" />

<center><small>Still from a video of Pepe equalizing a non-rigid load.</small></center><b>Videos:</b>
<ul>
<li><a href="videos/ISER12/equalize-box.wmv">[equalize-box.wmv]</a> (4MB) Equalization of a cardboard box</li>
<li><a href="videos/ISER12/equalize-pipe-variablecom.wmv">[equalize-pipe-variablecom.wmv]</a> (11MB) Equalization of bulky object with changing center-of-mass
<small>We change the center-of-mass using small magnetic weights.</small></li>
<li><a href="videos/ISER12/equalize-pipe-variablecom3.wmv">[equalize-pipe-variablecom3.wmv]</a> (15MB) Equalization of bulky object with changing center-of-mass
<small>We add weight well outside the polygon of support.</small></li>
<li><a href="videos/ISER12/equalize-backpacks">[equalize-backpacks.wmv]</a> (22MB) Equalization of non-rigid loads</li>
</ul>
<b>Relevant publications:</b>
<ul>
<li>Roxana Leontie, Evan Drumwright, Dylan Shell, and Rahul Simha. <a href="papers/iser12.pdf">Load Equalization on a Two-Arm Robot via Proprioceptive Sensing"</a>. <i>Proc. of 13th Intl. Symp. on Experimental Robotics (ISER)</i>. Quebec City, Canada. June, 2012. [<a href="presentations/iser12.pdf">Powerpoint slides</a>]</li>
</ul>
