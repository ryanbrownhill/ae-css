#AE to CSS
##Making the transition from animating in After Effects to CSS.

I started my dive into software design a couple years ago by creating demo videos and animating user interfaces. Coming from a Motion Design background After Effects was my baby and I had spent so many years perfecting that craft. I have worked side by side with developers recreating the animations that I had created in After Effects. This process was slow and tedious - there was a need for designer and developer to sit next to each other and hash out the details. I wanted to improve this workflow, so I dove into the research to understand how animations work within development and what the mental model was in which I needed to adapt to. After Effects was my baby but I needed to let it go and understand the new tools at my disposal. Here are some of the key findings I found that an After Effects motion designer needs to understand if their animations will ultimately be in code.

##1. Understand the Limitations
The world of development is constantly changing. As an animator one needs to be up to date on the current web standards and restrictions for animations.

###Understand the Properties at your disposal.
Basic List of Animatable Properties: 

![hello](images/animation-properties.png)

[Examples of Each Property Animated](http://leaverou.github.io/animatable/)

###Consider Performance.
In After Effects you have to consider the render time of your animations. You have to do the same for code - you have to think about the performance of an animations.

Properties that are performat:

* Position
* Scale
* Rotation
* Opacity

Here is a great article by Paul Lewis and Paul Irish about [High Performance Animations.](
http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/)

###Push the limits:

Explore and see what other cool things are possible with animations! One of my biggest finds was SVG Animations.

#####Things you can do with SVG animation:
* Animate on Path
* Trim Stroke
* Change Stroke Weight
* Color
* SVG Filters

[Here is a guide CSS-Tricks created for SVG Animations!](http://css-tricks.com/guide-svg-animations-smil/)

[I mean check this out!](http://codepen.io/lbebber/pen/RNgBPP?editors=110)


##2. Thinking in Percentages vs. Frames

Animations are thought of as a 0 - 100% in the world of development vs. seconds/frames in a timeline. As an animator you need to be able to calculate where keyframes are located within a perecent of an animation vs the frame/timecode its on. 

The best way to prepare for this calculation in After Effects is to animate with a timeline that ends with a multiple of 5 (Ex: 30 frames or 1 second) - this makes it easier to translate your animation into code.

* Licecap gif of a timeline mapped out to percentages


##3. Understanding The Motion Curves of Timing-Functions

This was the trickest part for me to wrap my mind around. Within CSS & many other programing languages there are predefined easing curves.[Here]() The standard ease-in, ease-out,bounce, etc. But as an advanced animator you never want to settle for a standard easy-ease - we like to get fancy and smooth with our easing curves. I mean look at this: 

* insert image of beautiful curves

So how do we recreate this in code?

This is where the power of the cubic-bezier comes in.

% of Animation Over Time vs Property Over Time - Adobting to this mental model took some time.

* this in AE = that in cubic bezier

##4. Understanding the possible changing variables -


Recently I have challenged myself to only animate in CSS. Making this transition had its own challenges but specifically changing my mental model on how animations work in the development world. 

The way I prototype this is by expanding or contracting a group of keyframes. You can do this by selecting all the keyframes then hold Alt(Windows) or Option (Mac OS) and dragthe first or last keyframe to the desired time. This mimics the possible changing time variable within code.




####My process for translating a basic animations into code:

* Map out the keyframes in percentages:
* Map out easing curves between keyframes:
* Map out time the animation takes:
* Done you have an coded animation!


Disclaimer: Most of my research was done about CSS - so when I state "code" I am mostly refering to CSS. 


Resources: 

 [AE Docs - Moving Keyframes](https://helpx.adobe.com/after-effects/using/editing-moving-copying-keyframes.html#move_keyframes_in_time)

http://css-tricks.com/almanac/properties/t/transition-timing-function/

http://www.smashingmagazine.com/2014/04/15/understanding-css-timing-functions/





But with my decision to focus on designing for software there has been a growing need for me to understand the limitations and range of animation within Front-End Development. Its been a difficult transition

development. I had started this by creating very basic websites and animations within CSS & JQuery - this helped me get by with


