---
layout: post
title:  "Reducing Human Fall Injuries using a Mobile Manipulator"
date:   2015-10-02
---

<p class="intro"><span class="dropcap">A</span>t the Positronics lab, we have been investigating the use of Robots to perform elderly care and assistance tasks. One of the first tasks we were interested in was using robots to prevent falls and reduce injuries when falls do occur. One of the major challenges with this type of research is executing experiments safely. For this reason, we decided to initially pursue the research in simulation.</p>

<p>One of the surprising discoveries of our early research was the lack of a publicly available, computationally fast, human model. To address this gap, we developed a 20-DOF rigid body model (shown below) based on Dempster’s research on human body anthropometry. That study provides effective link lengths, 3-DOF joint limits, relative masses, and center-of-mass positions for links. We plan to release the source code for this model so that it can be used by other researchers.

![Humanoid](../assets/img/humanoid.png)
<p>Screen capture of the humanoid in a standing configuration selected to show the joint locations and degrees of freedom.

<p>We next developed a series of scenarios to assess whether the robot, the PR2, would be able to arrest the fall. Below, you can see a video showing several trials of the humanoid falling alone, along with attempts by the robot to arrest the fall using one of these strategies:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=OKvNG_Zudw0
" target="_blank"><img src="http://img.youtube.com/vi/OKvNG_Zudw0/0.jpg" 
alt="Video of Humanoid Falls" width="400" border="10" /></a>

<b>Relevant Research:</b>

Joshua Lurz and Evan M. Drumwright. "Reducing Human Fall Injuries using a Mobile Manipulator". <i>Proc. of the IEEE-RAS Intl. Conf. on Humanoid Robotics</i>. Seoul, Korea, 2015. [<a href="assets/pdfs/humanoids-2015.pdf">pdf</a>]
