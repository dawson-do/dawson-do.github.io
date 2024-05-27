---
layout: post
title:  "About my site theme"
description: Notes on how I made my website theme
date:   2024-05-26 16:42:49 -0400
categories: other
published: true
keywords:
  - Youth With You
  - ywy
  - QCYN
  - Jekyll
  - theme
---
*Feel free to "inspect element" in your browser or view the [repo](https://github.com/dawson-do/dawson-do.github.io) to see how the styling is done. A word of warning, it's pretty disorganized and definitely unoptimized.*

Besides my personal website, the only project where I was heavily involved in the web design was [UMD Puzzlehunt](https://2021.umdpuzzle.club/). I enjoyed playing around with CSS there and thought it was a useful skill, so I had been meaning to learn more. I wanted to share a bit of the process in creating the theme, which is modified from Jekyll's default theme, Minima (v2.5 specifically).

<!--excerpt-->

### Inspiration

Before working on this theme, I had already changed a few things from default Minima---removing the footer, changing the header---but nothing substantial. I had ideas for the new theme for a while, but finally found the time and energy recently.

So one of my favorite TV shows of all time was a Chinese reality series, Youth With You Season 2 (YWY)[^1]. I really liked the graphic design used throughout the show, and figured it'd be a fun project to adapt it to a website theme. I had previously tracked down the design firm's [YWY Behance page](https://www.behance.net/gallery/93881133/YOUTH-WITH-YOU-Season2-2) for a different project (see images below), and the page was, again, an invaluable reference.

| ![Youth With You Season 2 logo built in Terraria](/assets/images/site-theme/ywy-terraria.png)|
|:--:|
| I originally found the Behance page when I was building the YWY logo in Terraria. (Built in Master Mode btw)|

|![Youth With You Season 2 logo built in Terraria during boss fight](/assets/images/site-theme/ywy-terraria-in-action.jpg)|
|:--:|
| The logo serves as a backdrop for my boss arena.|

What I liked most about the YWY design was that it is sleek-yet-retro and the animations gave it a lot of kinetic energy. One of my goals for this redesign was to make my site *not* look like a Web 2.0 "professional website" template---I wanted it to actually look custom made---and these features keep the design from looking too formal. The specific features that I wanted to incorporate into my site were the desktop-window borders and the expanding windows. Of course, I also liked the color scheme.

### Implementation

Most of the elements are pretty straightforward. I was able to implement the 3D-perspective desktop-window border using a few online references (see below) and made the navbar links resemble desktop-window buttons. I interleaved the horizontal bars motif featured in the site header throughout the site by adding the motif to the section headers inside the page content. This feature was inspired by those used in [Galactic Puzzle Hunt 2020](https://2020.galacticpuzzlehunt.com/), which I particularly liked because they automatically filled the horizontal space.

The horizontal bars in the page header themselves were probably the most challenging element to implement. It's probably not the best way to do it, but I utilized a similar technique to the section headers. I used a `:before` pseudo element attached to the navbar, which has variable width depending on the window size and navbar size. This was tricky because at narrow window sizes, the navbar turns into a drop-down menu. I also had to account for the site title ("DAWS"), and attach another pseudo element to continue the bars all the way to the edge.

I couldn't really come up with a practical way to integrate the expanding windows into my page directly, so I incorporated the idea into the hovering effect for the hyperlinks. On my website, I previously used the hyperlink style that I created for UMD Puzzlehunt, which I liked because it makes reference to physical media (underlining and highlighters). A few months after UMD Puzzlehunt, [Hunt 20](https://hunt20.com/) used a similar style which I liked because it added an animated transition. Lastly, the little element denoting a hyperlink was something I picked up from [Practical Typography](https://practicaltypography.com/). I merged all of these ideas together to create the expand-on-hover highlighted hyperlinks for my website.

Naturally, I'll continue to update the site theme (and this post) when I see something that inspires me. For example, some things I want to add are some image motifs and possibly update the font. Ideally, the design will evolve and get more unique over time, and it will all be documented here!

### References

Here are websites with elements I adapted:
* Gradient + Polygonal borders: [CSS-tricks](https://css-tricks.com/gradient-borders-in-css/), [Stack Overflow](https://stackoverflow.com/questions/52461014/how-to-draw-polygon-background-with-css)
* Horizontal space-filling header bars: [Galactic Puzzle Hunt 2020](https://2020.galacticpuzzlehunt.com/rules.html)
* Link hover boxes: [Hunt 20](https://hunt20.com/), [Practical Typography](https://practicaltypography.com/)
* Misc. CSS tricks: [A Single Div](https://a.singlediv.com/)

-----

[^1]: My magnum opus blog post about that is a long wip.
