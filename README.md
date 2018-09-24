# PureBeforeAfterSlider
This repo contains an attempt to implement a before / after slider using only HTML and CSS.

![](readme.gif)

It succeeds in a number of ways but there seem to be some major issues that make it unsuitable for most production scenarios:

  * required features not supported in IE / Edge 
  * mobile support is about 50/50 which means you will hear complaints from large number of users
  * mobile browsers supporting such features, do not actually implement them in mobile friendly ways. (e.g. gestures / touch)

# Index

 * [test2](testResize2.html) - this is a div based approach. Supports percentage based scaling
 * [test1](testResize.html) - table based solution, has some major shortcomings especially not supportig percentage sizes
 * [test3](testResize3.html) - look how easy it is to use a third party libray (cocoen)

# Supported browsers
* This solution worked perfectly in chrome. 
* Firefox had some minor visual artifacts (noted below).  

# Issues
The main problem here is around the css resize property. Support by browsers is spotty, and once you get on mobile, the *so called support* does not actually work with gestures and touch events to perform a resize.

On firefox there is an issue with the way z-index is handled (compared to chrome) that leaves some artifacts.

This solution uses some css transform tricks that is arguably an ugly hack so even when / if the other issues are resolved, there is always going to be at least some marginal chance that this solution breaks on some new browser.

Check the readme date, things may change as browser technology develops.

# Alternative
If you came here looking for something like this, i would refer you to [COCOEN](https://github.com/koenoe/cocoen). It implements everything you need in a lightweight, dependency free, ~5KB package. It supports mobile and all the major browsers.

A few of the other solutions i found require jquery, and if you already are loading jquery on your site you might save some bytes using one of these instead:

  * [COCOEN](https://github.com/koenoe/cocoen) - no jquery - 4.9kb
  * [before-after.js](https://github.com/jotform/before-after.js) - require jquery - 1.9kb
  * [imgSlider](https://github.com/kavyasukumar/imgSlider) - requires jquery - 1.7kb
  * [Juxtapose](https://github.com/NUKnightLab/juxtapose) - no jquery - 23kb
