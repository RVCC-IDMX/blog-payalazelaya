---
title: HSL Values and their power in CSS
author: "By Paola Ayala Zelaya "
description: A blog that gives an overview of how using HSL values for color in
  CSS can be better than using RGB.
date: 2022-10-09T18:58:22.247Z
tags:
  - post
  - featured
image: /assets/blog/gradienta-ix_kudzcczo-unsplash.jpg
imageAlt: A color gradient of various colors on the color wheel that spans from
  left to right
---
F﻿or a web developer who is starting out in web development, they tend to use RGB values for elements such as background colors, borders, etc. It is common for beginners to use RGB values as they are very simple to play around with and it is the standard way of how to remember colors as well.  CSS RGB values allows the developer to refine colors through exact shades or tones as each part of the R, G, or B in RGB affect how light or dark a color is. 

U﻿sing RGB values make colors have shades or tones to them, but it can be a hassle when a developer wants to have colors of higher or lower saturation, a specific hue, or wants to change the lightness of it. This is why web developers are starting to use CSS HSL values when it comes to elements using colors because of how there is more complexity to it. 

Web developers such as Kevin Powell, who is more prominent on Youtube, mention the fact that with using CSS HSL values, it is easier to change values through the color picker integrated within a software such as VSCode. When the color picker is set to HSL values, the color picker will rely on what degree a color is on the color wheel for hue, how saturated a color is, and how bright or dull a color is. 

F﻿or a developer to use CSS HSL values for an element such as background color for the body for example, they would write it like this within the CSS file:

```css
body {
  background: hsl(220 80% 40%);
}
```

T﻿his line of CSS gives the background color of the body to be blue and if the developer wants to make the blue less saturated and lighter, then they would need to decrease the 2nd value and increase the 3rd value. An example of how this new change would look like is shown down below: 

```css
body {
  background: hsl(220 50% 70%);
}
```

N﻿ow the background color of the body a dim light blue color with this new change. 

HSL starts to become reliable when it comes to creating color schemes to a design now that a developer can focus on the hue, saturation, and lightness of a color. With creating a color scheme, a developer can reuse HSL values throughout their CSS file but would change the values they want to change just like the code blocks from above. This makes the colors stand out from one another as there's a certain consistency of color contrast to them too. 

#### E﻿xample of HSL Color Scheme

![HSL Color Scheme](/assets/blog/hsl-color-scheme.png "Color Scheme")

I﻿n terms of how a person perceives color, it is true how hard it is to predict a color through RGB values as it is harder to create variations of a certain color. HSL values on the other hand represent the attributes a person can actually perceive as it's more keen to the human eye, thus why HSL has an advantage over RGB. 

O﻿verall, HSL has the capability of overseeing colors that are visible to the human eye through its values of hue, saturation, and lightness, so it is why it is considered more useful for color in CSS rather than RGB that a beginner web developer starts out in using.