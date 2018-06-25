---
layout: post
title:  "Robotics Season in Review"
date:   2018-3-8 3:00:00 -0400
categories: project
---
  Vex team 66640 just finished up our first real season.
  The season started off relatively rocky.  Our first competition could have gotten better.  The design we had for a double reverse 4 bar lift was limited to put it nicely.  
  We won our next competition with the help of Friends Academy team 5059J.  At that competition we had some pretty significant issues with our motors stalling and quitting during the match.
  The reason Vex motors trip is because they have whats called a 'PTC' in order to cut off current when the motor gets too hot.  According to Vex, this is protect the internal circuitry of the cortex and the motors from shorts and overcurrent.  It is my personal belief, as ridiculous as it sounds, that Vex does this to make it harder to actually use the motors.  We tested modding the PTC by simply shorting it and it was easily able to handle the load without shutting down.  However, we soon discovered that this was not a legal modification and had to find a different way to deal with our problems.  
  The general workaround which other teams had of dealing with this problem is what is commonly referred to as "slew motor control" but we took to calling it "triangle ramping" before we heard what the common name was.  Vex motors, and motors in general, spike in current when they have a voltage applied across them.  This spike causes a significant temperature increase in the PTC.  Unfortunately, the PTC cools very slowly (due to being inside a small plastic box) so in order to stop our motors from cutting out, we had to remove this current spike.  In triangle ramping, instead of instantly applying a sudden voltage change across a motor, we apply small increments over time, about 0.8V/mS.  Although this is actually rather fast, it is slow enough to reduce the current spike considerably, keeping our motors running throughout the competitions.
  After some pretty significant revisions to our robot, we came up with a result I'm more than happy with.  
  If I had a chance to restart the season, I would make the following changes.
  For our base, I would motor up all four wheels instead of leaving the front two passive.  I would also switch to high speed motors which would drive up our total current draw but we could likely have afforded it.  I would have liked to put our wheels lower or at least past the front of the bars that hold them so that we could drive over the 10 point bar and drop a mobile goal into the 20 point zone.
  Instead of a scissor lift as a main lift, I would have liked to go with a reverse six bar to four bar lift.  This would have allowed us to get some pretty serious height without adding friction.  The scissor lift was easier to get decent results with, but I believe the ideal robot would have this type of lift.
