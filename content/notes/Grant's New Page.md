---
title: "Grant's New Page"
tags: 
- test
- test2
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

![](notes/images/IMG_0720.jpg)
<div id="captionbox"> <p class="alignleft">This would be the caption</p> <p class="alignright">📸 <small>Photo by Grant Wilson</small></p> </div>
<div style="clear: both;"></div>

### YouTube Embedding
My notes say that this Hugo shortcode should render the youtube video

![](notes/images/Shortcodes___Hugo.png)

Here goes:
{{< youtube xbILy-bCN4M >}}
