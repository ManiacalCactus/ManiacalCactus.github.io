---
layout: post
title:  "TDCS Experiments"
date:   2017-09-24 11:50:00 -0400
categories: project
---
  I've had the idea of building a proper tDCS rig in the back of my mind since seventh grade.  That year, I had a science research project, and my first serious project idea was to attempt to perform and test the effects of tDCS on mice.  Unfortunately my instructor wisely decided that this would be too difficult of a project for a seventh grader, not even mentioning the ethical ramifications of testing a seventh grader's electronics project on living creatures.
  Despite this, the concept of tDCS has been in the back of my mind for quite some time.  There's something incredibly attractive about the concept of being able to improve your own body with nothing more than a couple of well placed sponges and some electronics.  This summer I started my first real experiments in the area.
  I began with a simple circuit I found in <a href="http://brmlab.cz/project/brain_hacking/tdcs">this</a> paper
  This resulted in my first control board
  <img src="/assets/images/tDCS/Old.JPG"/>
  I also spent some time researching sponges and decided to make my own using some packing foam and washers to spread a more even voltage.
  <img src="/assets/images/tDCS/Electrode.JPG"/>
  However, after some research and testing this circuit proved unreliable, so I graduated to a new one of my own design
  <img src="/assets/images/tDCS/CustomSchematic.png"/>
  The basic principle of this circuit is that the negative feedback of the op-amp causes the current through RLOAD to be limited to the non-inverting input voltage divided by the reference resistance.  This allows a constant current source of 2mA or less.
  <img src="/assets/images/tDCS/CustomBoard.JPG"/>
  I have only begun testing this board.  I will post updates as I begin to learn it better.  For now I will be using it to study language and perhaps to train my muscles while running.  Thanks for reading.
