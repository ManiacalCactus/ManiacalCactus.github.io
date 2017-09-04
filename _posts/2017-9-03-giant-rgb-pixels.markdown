---
layout: post
title:  "Giant RGB LED Pixels"
date:   2017-09-03 21:20:49 -0400
categories: project
---
  For my first project on this new blog i decided that what I make should be a learning experience for me as it would help me better convey what will become the general tone of this site.

  Thusly, I decided that it was time I finally learn how to design and order pcbs.  I have been interested in hobby electronics for several years now, but the extent of my production has all been homebrew.  Such is why I decided I should create something which I can't manufacture in my workshop, in this case because it would simply be too large of a task.  Since I wanted to focus on learning the process and not the electronics itself, I went with a super simple design, two leds on a board.  Naturally, I still wanted this to serve some purpose, so I decided I would make these boards modular and linkable using headers.  Below are my first sketches of the idea.
  ![First Sketches]({{ kopitslabs.com }}/assets/images/GiantPixelsSchematic.JPG)
  After the initial sketches, I took some time to formalize the design in Fritzing, software made for this purpose.  Although I have made efforts in the past to use Eagle to design pcbs, I have never been successful due largely to the arguably overly complex system and lack of sufficient resources.  So I settled for easier to use CAD tools.
  ![Fritzing]({{ kopitslabs.com }}/assets/images/GiantPixelsDesign.png)
  After creating the boards, I used Fritzing's integrated service to order my pcbs.  Although I could probably have moved the production to China for much cheaper, I wanted the simplest possible experience for my first run of pcbs, so I want with Aisler.  The first time I uploaded my designs I placed to traces slightly too close to each other, which resulted in them being contiguous.  Luckily I caught this mistake before I spent 50 pounds and two weeks on non functional pcbs.
  ![Aisler]({{ kopitslabs.com }}/assets/images/GiantPixelsAisler.png)
  ![Bare Boards]({{ kopitslabs.com }}/assets/images/GiantPixelsBare.JPG)
  When the 15 boards came two weeks later I spent about 3 hours populating all of them with their leds and headers.  However, on my first test using three potentiometer outputs hookup up to the first three legs of the led and ground on the fourth, I could never get one color to show up, and changing the value of its respective potentiometer would dim the led as a whole.  After some debugging, I realized the reason for this was that when creating the boards I assumed that the farthest out leg would naturally be ground.  This however was not the case; the third and longest leg was ground, so the solution was simply swapping two inputs.
  After testing, I began to write code to cycle through all of the possible colors using an arduino.
  {% highlight c %}
int red, green, blue;
int *current, *next;
int pinRed = 4, pinGreen = 5, pinBlue = 6;
int maximum = 255;
int delayAmt = 3;

void setup() {
  red = maximum;
  green = 0;
  blue = 0;
  current = &red;
  next = &green;
}

void loop() {
  while(*next < maximum){
    *next = *next + 1;
    *current = *current - 1;
    updateLED();
    delay(delayAmt);
  }
  current = next;
  if(next == &red){
    next = &green;
  }else if(next == &green){
    next = &blue;  
  }else if(next == &blue){
    next = &red;  
  }
}

void updateLED(){
  analogWrite(pinRed, red);
  analogWrite(pinGreen, green);
  analogWrite(pinBlue, blue);
  delay(delayAmt);
}

{% endhighlight %}  
  However, I this code resulted in some very strange behavior: the led would increase wildly for the color green and oscillate while the color blue was much less than it should have been.  I initially assumed that this was an issue with my code, but even after working with a second revision the problem persisted.  I then assumed it was a problem with the leds, or perhaps an overcurrent issue.  However, after retrying the system using mosfets to deliver the power from a 9 volt, I ruled out overcurrent.  Next, I switched the leads of different colors to no avail.  Some further research lead me, strangely enough, to color theory.

  ![Color Absorption Curves](https://upload.wikimedia.org/wikipedia/commons/c/cc/Absorption_Curves.JPG)
  By Arturomoncadatorres (Own work) [CC BY-SA 3.0 (http://creativecommons.org/licenses/by-sa/3.0)], via Wikimedia Commons

  It turned out that the fault was not with my materials nor method of using them, but with my eyes.  As seen in this chart, green colors are most easily detected, then red, and then blue.  This perfectly explained my problem; green was the brightest, then red, then blue.  I quickly changed my code to reflect minimums and maximums for each color.  This resulted in the my final product.
  ![Final]({{ kopitslabs.com }}/assets/images/GiantPixelsFinal.JPG)
  Thanks for reading this far.  I had fun with this project, and I hope you took away from it as much as I did.
