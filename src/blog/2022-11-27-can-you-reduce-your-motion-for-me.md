---
title: Can You Reduce Your Motion for Me?
author: "Paola Ayala Zelaya "
description: A blog giving an overview on the topic about animation and
  accessibility when it comes to using animations on websites
date: 2022-11-27T04:29:24.333Z
tags:
  - post
  - featured
image: /assets/blog/cssanimations.png
imageAlt: "3 shapes that demonstrate how CSS animations happen within different
  styles of them "
---
Woah! The button rotates left and right when it hovers, how cool is that! 

Animations are CSS effects that can be added to an element of a developers choosing when it comes to wanting the site to be more interactive for the user. These animations can emphasize important aspects of what the user should focus on when they visit the site for a particular thing. Animations are brought together using two components: when there’s a style describing the animation and keyframes pinpointing the start and end states of the animation’s style. Animations through CSS have advantages over other ways on how to create animations when they don’t require knowing Javascript, are able to run properly under system loads and have the browser control the sequence in order to optimize performance and efficiency on its end. In the end, animations range from being simple all the way to being very complex. 

To create an animation sequence for an element, it’s using the animate property or its several sub-properties for timing, duration, and other settings and then using the key-frames at-rule for getting the appearance of the animation. Examples of how to get animation sequences are shown below: 

```css
p {
  animation-duration: 4s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
```

The examples styles the "p" element so the text slides in from off the right edge of the browser window. In this case, the animation is going to take 4 seconds to initiate from start to finish using the animation-duration property, and the name of the @keyframes at-rule defines the animation sequence as slidein. If a browser window is large for the animation to happen, then it’s convenient to put the element to be animated within a container and set overflow:hidden on the container.

How to get a text slide animation to move back and forth:

```css
p {
  animation-duration: 4s;
  animation-name: slidein;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%;
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
```

In this case, animation-iteration-count has the slide animation repeating itself over and over again, but with animation-direction: alternate included, the slide animation is able to move back and forth across the browser window. 

Aren’t these animations really cool to include in your project? I agree too, but with animations comes the responsibility of achieving accessibility with them since they can be created to be very complex. Having rapid animations or animations that include too much motion to them will lead for there be accessibility warnings when checking them through dev tools. These warnings signal that for someone who uses accessibility mode to browse a website, they’ll be presented with these animations that are easily distractable to them. Luckily there are ways to follow accessibility when it comes to using animations on websites or anything similar for adding visuality to them.

Use prefer-reduced-motion: 

The prefer-reduced-motion media feature is used when a user requested the system to minimize the amount of non-essential motion it uses. For an animation shown on a webpage, the user can request a slower version of it for their own consideration and look at the animation without any problems. A good example of this media feature being used would be with this code below: 

```css
:root {
  --anispeed: 10s;
}
 
/* Media Query for Reduced Motion */
@media (prefers-reduced-motion) {
  :root {
    --anispeed: 70s;
  }
}
```

This code is from an assignment that I worked on called Mesmerizing where the animation shown on the live server was that of a circle going in a loop and transforming itself to illustrate different designs of it. The speed of the circle animation is going at 10 seconds, whereas in these 10 seconds it’s going super fast and it even blurred my version when focusing on it because of how fast it goes in a short amount of time. A media query is used for prefers-reduced-motion to address the media state where the root of the animation will loop for 70 seconds in that media state and the change in speed is notable when testing out the media state. The circle animation shows how it flows at a relatively good speed and there isn’t much motion included in it. This media state is very reliable for addressing accessibility for a user who of course, prefers reduced motion for an animation sequence that’s notably going super fast.

In general, the Web Content Accessibility Guidelines (WCAG) provide more tactical considerations for making sure that animations seen on websites are accessible to users when needed. Different contexts affect the details of what a developer needs to do to improve accessibility, but thankfully the WCAG addresses recommendations for animated content/interactions. These guidelines consist of play/pause controls when needed, limits on blinking/flashing motions, and in fact, when to use reduced motion options for users. Accessibility is key to being a good web developer in a constantly developing setting when users of all kinds of circumstances frequently view websites on a daily basis.