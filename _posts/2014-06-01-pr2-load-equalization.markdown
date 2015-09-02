---
layout: post
title:  "Load equalization via proprioceptive force feedback"
date:   2014-06-01
---

<p class="intro"><span class="dropcap">P</span>revious research with <b>Pepe</b>, our <a style="color: #226ac1;" href="http://www.willowgarage.com/pages/pr2/overview">PR2</a> robot from <a style="color: #226ac1;" href="http://www.willowgarage.com/">Willow Garage</a>, was focused on manipulating bulky objects for which form or
force closure strategies may be infeasible: in such cases, we may be able to constrain manipulated objects only <i>unilaterally</i> in some directions.</p>
<!-- img class="aligncenter" src="http://robotics.gwu.edu/~positronics/wp-content/uploads/2013/08/pepe-loadbalance.png" alt="" width="637" height="357" / -->
<p style="color: #5a5a5a;">We recently focused on equalizing bulky loads applied to the PR2′s arms, which would be useful for humanoid dynamic balancing and reducing robotenergy consumption. Our simple and robust reactive strategy uses proprioceptive force feedback and manipulation with the arms (not the grippers) to yield exceptional performance: the robot never fails to equalize a load in over 75 experimental trials.</p>

##Videos:
###Equalization of a cardboard box:
<iframe src="//www.youtube.com/embed/oZJ8nvMtSyw" width="420" height="420" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
<h4><span style="color: #5a5a5a;">Equalization of bulky object with changing center-of-mass</span><br style="color: #5a5a5a;" /><small style="color: #5a5a5a;">We change the center-of-mass using small magnetic weights.</small></h4>
<iframe src="//www.youtube.com/embed/un7Ggl5ujPU" width="420" height="420" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
<h4><span style="color: #5a5a5a;">Equalization of non-rigid loads</span></h4>
<iframe src="//www.youtube.com/embed/T2GxcVxjN3g" width="420" height="420" frameborder="0" allowfullscreen="allowfullscreen"></iframe>