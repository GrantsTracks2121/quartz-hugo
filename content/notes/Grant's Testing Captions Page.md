---
title: "Grant's Testing Captions Page"
tags: 
- 🌱 Seedling
- 🧹 Needs Editing
---
## Grant's New Page
![This is the alt text for the image](notes/images/IMG_0720.jpg "This is a cool rock I saw during yesterday's stroll near Buena Vista Park in Edmonton")*Doing a timelapse video in the Ministik || <small>Photo by: <a href="https://commons.wikimedia.org/wiki/File:Shikoku-Pilgerweg_Karte.png">Lencer</a>, <a href="http://www.gnu.org/copyleft/fdl.html">GFDL</a>, via Wikimedia Commons</small>*


### Making an image a link to something else
This syntax is supposed to work for linking an image to something else:

```
[![This is the alt text](notes/images/Img_9606_2022-Oct-30.jpg)](notes/hosting.md)
```

Let's try that out - it WORKS - but the linking part seems to spill over and push the caption down.
This is using the simple "em" tag to do a caption. There's already css to deal with this in Quartz.

[![Buena Vista Bridge](notes/images/IMG_0709.jpeg)](https://google.ca)
*Buena Vista Bridge* // 📸 <small>Photo by Grant Wilson</small>


### Figcaption 
By itself - it's meh. But perhaps I can css it.

Let's try again using the figcaption HTML tag. I haven't had any luck in the past with it, but let's try again from the info [here](https://thesynack.com/posts/markdown-captions/).

The syntax is:

```
![Big Red Train](/path/to/image)

<figcaption>

The [ABC Train](https://example.com) is *very* big and red.

</figcaption>
```

![Buena Vista Bridge](notes/images/IMG_0709.jpeg)
<figcaption>

The [Buena Vista Bridge ](https://google.ca) is *very* big and and well made.

</figcaption>

### This is the one that works
I put it in an enclose p tag and use css to float the two sections (caption and attribute) to the left and right respectively.
![This would be the alt text](notes/images/IMG_0720.jpg)
<p class="captionbox"> <span class="alignleft">Here's a big rock I saw near Buena Vista Park. </span> <span class="alignright">📸 <small>Photo by Grant Wilson</small></span> </p><p style="clear: both;"></p>
<p class="captionbox"> <span class="alignleft">This is the caption.</span> <span class="alignright">📸 <small>Photo by Grant Wilson</small></span> </p>


Here's the same example and the attribution is in with the caption.
***This worked very well! I'm going to use this, an hope it helps in the future.***
![This would be the alt text](notes/images/IMG_0720.jpg)


### YouTube Embedding
My notes say that this Hugo shortcode should render the youtube video

![](notes/images/Shortcodes___Hugo.png)

Here goes:
{{< youtube xbILy-bCN4M >}}
