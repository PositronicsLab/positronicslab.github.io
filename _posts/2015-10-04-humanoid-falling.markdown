---
layout: post
title:  "Reducing Human Fall Injuries using a Mobile Manipulator"
date:   2015-10-02
---

<p class="intro"><span class="dropcap">A</span>t the Positronics lab, we have been investigating using robots to help prevent falls and to help reduce injuries when falls do occur. We initially pursued this research using multi-rigid body simulation to avoid possible harm to humans during experimentation.</p>

<p>One of the surprising discoveries of our early research was the lack of a publicly available, computationally fast, human model. To address this gap, we developed a 20-DOF rigid body model (shown below) based on Dempster’s research on human body anthropometry. That study provides effective link lengths, 3-DOF joint limits, relative masses, and center-of-mass positions for links. We plan to release the source code for this model so that it can be used by other researchers.

![Humanoid](http://positronicslab.github.io/assets/img/humanoid.png)

Screen capture of the humanoid in a standing configuration selected to show the joint locations and degrees of freedom.

We next developed a series of scenarios to assess whether a mobile manipulator robot, the PR2, would be able to arrest the fall. Below is a video showing several trials of the humanoid falling alone, along with attempts by the robot to arrest the fall using one of these strategies:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=UOkgcJ5eZDk
" target="_blank"><img src="http://img.youtube.com/vi/UOkgcJ5eZDk/0.jpg" 
alt="Video of Humanoid Falls" width="400" border="10" /></a>

<b>Relevant Research:</b>

Joshua Lurz and Evan M. Drumwright. "Reducing Human Fall Injuries using a Mobile Manipulator". <i>Proc. of the IEEE-RAS Intl. Conf. on Humanoid Robotics</i>. Seoul, Korea, 2015. [<a href="http://positronicslab.github.io/assets/pdfs/humanoids-2015.pdf">pdf</a>]
