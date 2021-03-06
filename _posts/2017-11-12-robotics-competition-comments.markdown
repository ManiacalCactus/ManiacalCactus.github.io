---
layout: post
title:  "Robotics Competition Impressions"
date:   2017-11-12 21:20:49 -0400
categories: project
---
  This weekend my robotics team competed in our second ever competition.  We compete in the Vex Robotics Competition.  This year, the game is called In The Zone.  The goal is to stack up plastic cones on top of larger, heavier cones, referred to as mobile bases, or higher, static cones.  The catch is that your robot has to begin as shorter than 18", which they are incredibly strict about, yet you need to stack ideally at least 3 feet high, meaning you have to build a robot which can expand vertically very well.
  
    ![In the Zone](https://www.vexrobotics.com/media/catalog/product/cache/1/image/9df78eab33525d08d6e5fb8d27136e95/v/r/vrcrender2_1.png)

  This competition, we chose what is referred to as a reverse four bar to four bar design.  Unfortunately, even before the competition, we noticed several issues with our design, mainly that due to the nature of the parts, it would be quite difficult to increase the angle of the parallelograms past a certain point without running into other parts.

  ![Four bar lift](https://challenges.robotevents.com/uploads/0002038_original.jpg)

  ![Robot 2017.1](/assets/images/Robotics/InTheZone2017.1.jpg)

  Upon arriving at the competition, one of the first issues we ran into was size.  All dimensions of the robot must fit within 18".  Our y-axis was built such that the gears of the main lift were sticking out about .25" if even over the build area.  We were forced to remove part of our main claw in order to fit within the build limit.  We also had to file down some of the axles of our main drive assemblies to fit in the x-axis.
  However, my main purpose in this article is not to comment on our engineering design process but how my team can improve ourselves for our next competition.  
  Starting from the ground up, we need to ditch our current drive assemblies.  At the moment, we have a somewhat convoluted six-wheel, geared design.  At the competition, I saw an incredibly elegant set of drive assemblies, which we may attempt to utilize for our next competition. They were direct drive based, meaning they required no gears which could jam and grind, and a minimal number of axles and collars which both fail often.  They also were linked only by standoffs on all four corners of opposing plates, making them perfectly square and sturdy.

  ![Our Assemblies](/assets/images/Robotics/DriveAssemblies2017.1.jpg)

  The next revision to our robot which we want to make is in the lift mechanism for mobile bases.  One of the teams we allied with, 162A, was built with the sole intent of lifting up mobile bases and moving them into scoring zones, an surprisingly effective strategy.  By teaming up with them, we were able to  win our first elimination match and almost pass the first round.  The mechanism which we used for lift mobile bases was a ramming mechanism, which required lots of torque from the motors and jammed on occasion.

  ![Our Mobile Base Scooper](/assets/images/Robotics/MobileBaseScoop2017.1.jpg)

  162A's, on the other hand, had an extremely nice fold-out scoop which moved around a hinge to move only about an inch vertically and backwards to scoop up the mobile base with incredibly high torque, allowing them to pick it up with only one or two motors.  I saw that many of the high ranking teams had a similar designs for this task, so we will likely adopt this.  Unfortunately, I don't have an image of 162A to show.
  Lifting mechanisms in Vex get incredibly complex very quickly.  One of my favorite teams, which we affectionately referred to as the "Scarily Tall Team" had a robot which appeared to basically be a solid block of metal when folded in.  However, when the expanded, it turned from 18" to a monster which was taller than I am.  During one of our rounds, my team teamed up with them.  I genuinely had to back away because I thought it could collapse on me.  I believe what they had is referred to as a reverse four bar to six bar lift which I think then went to a chain lift.  It was much taller than our relatively feeble reverse to forward four bar linkage system.  Perhaps for this next competition we can develop a six bar to reverse six bar linkage with a chain lift at the end.  With that we could potentially get high enough to stack maybe 16 cones high as opposed to our current 4.

  ![Scarily Tall Team](/assets/images/Robotics/VeryTallTeam.jpg)

  The other possible lift mechanism which we could adopt is a scissor lift.  We toyed with the idea of a scissor lift earlier this season but decided against it since it would be so heavy and potentially unstable.  We did see one very good scissor lift team, which I did actually get a full sized picture of.

  ![Scissor Lift team](/assets/images/Robotics/ScissorLiftTeam2017.1.jpg)

  The final part of our robot which I may want to modify is our end effector.  The end effector we chose was a claw with standouts sticking into the inside.  This worked somewhat well, but was also fairly unreliable.  We could potentially modify this claw to be a bit more reliable, or simply ditch it altogether.  The most intriguing alternative to a claw was two sets of gears constantly rotating counter each other in parallel with rubber bands stretched between them to pick up the cones vertically.  It is somewhat related to this roller claw.

  ![Claw](http://curriculum.vexrobotics.com/sites/default/files/styles/large/public/6.10.04_0.JPG)

  Overall, we learned a lot at this competition and will likely be ditching the entirety of our current design and trading it in for what will soon be a much more intimidating robot.
