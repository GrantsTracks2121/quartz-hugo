---
title: "Grant's Testing Captions Page"
tags: [🌿Budding, 🧹Needs_Editing, 🌳Mature, 💡Core_Idea]
---
## Grant's New Page. 

> [!NOTE ] Centering the image and caption together
> Okay I've got the LANDSCAPE pictures centering with the caption centering with them. But damn, now I need to center or constrain the portrait images. The captions don't look right on those.

This page: https://dev.to/bdavidxyz/markdown-center-image-39j1
gives a number of options for centering an image specific to markdown.

I'm obsessing on captions under images, I know, but here's some code that I could combine with what I have to size a caption with the size of the image. This provides the "container" around the image that I know I need.

## Here's an 800 px image - look any different?
Trying to center this one. ***This one centered!!*** It uses the ``#center`` anchor to call some code


![Just hangin around in the bush](notes/images/IMG_0782.jpeg#center)
*This is the caption - let's see what happens with it // 📸 Photo by: Grant Wilson*

***This one has  portrait id attached to the image code.*** It doesn't work.

![Just hangin around in the bush](notes/images/IMG_0782.jpeg#portraitcaption)
<span>*The cache I found after having to bushwhack a bit from the trail "above" it.*</span>



## And here's another landscape version:

![](notes/images/IMG_0768.jpeg#center)
*This is a smaller picture - 800 px vs the 1500 I've been using. //  📸 Photo: Grant Wilson*


### Yet another solution for centering image and caption together

![This is the alt text](notes/images/IMG_0768.jpeg)
*This is an image*

## Here's an attempt at sizing the image with css

### Right 50
The code works, but of course my solution for captions doesn't - it's based on simply appearing under an image that is 100% wide.
![This should be the Alt Text](notes/images/IMG_0709.jpeg#right50 "This should be the title text")

Nullam tristique diam purus, at vestibulum nisi pharetra sed. Quisque et turpis tellus. Integer arcu nulla, venenatis id elit non, ornare euismod tellus. Quisque non est felis. Curabitur ac interdum massa. Vivamus condimentum arcu eu leo hendrerit cursus. Ut accumsan tincidunt erat. Praesent non posuere nunc. Donec eget lorem vitae mi aliquam convallis. Phasellus nisi purus, tristique in vestibulum non, tempus sit amet metus. Ut ante ipsum, lacinia nec erat eu, consequat sodales erat. Phasellus eget rutrum enim. Nunc pretium nunc ac ante laoreet scelerisque. Donec ac quam vitae sapien rutrum convallis. Morbi consectetur porttitor dolor, a faucibus metus placerat vel.


![This should be the Alt Text](notes/images/IMG_0709.jpeg#left50 "This should be the title text")This image is LEFT justified and the text should flow around it. 

This is a new paragraph and here's some more text.

Pharetra sed. Quisque et turpis tellus. Integer arcu nulla, venenatis id elit non, ornare euismod tellus. Quisque non est felis. Curabitur ac interdum massa. Vivamus condimentum arcu eu leo hendrerit cursus. Ut accumsan tincidunt erat. Praesent non posuere nunc. Donec eget lorem vitae mi aliquam convallis. Phasellus nisi purus, tristique in vestibulum non, tempus sit amet metus. Ut ante ipsum, lacinia nec erat eu, consequat sodales erat. Phasellus eget rutrum enim. Nunc pretium nunc ac ante laoreet scelerisque. Donec ac quam vitae sapien rutrum convallis. Morbi consectetur porttitor dolor, a faucibus metus placerat vel.



![This is the alt text for the image](notes/images/IMG_0720.jpg "This is a cool rock I saw during yesterday's stroll near Buena Vista Park in Edmonton")*Doing a timelapse video in the Ministik // 📸 <small>Photo by: <a href="https://commons.wikimedia.org/wiki/File:Shikoku-Pilgerweg_Karte.png">Lencer</a>, <a href="http://www.gnu.org/copyleft/fdl.html">GFDL</a>, via Wikimedia Commons</small>*


### Making an image a link to something else
This syntax is supposed to work for linking an image to something else:

```
[![This is the alt text](notes/images/Img_9606_2022-Oct-30.jpg)](notes/hosting.md)
```

Let's try that out - it WORKS - but the linking part seems to spill over and push the caption down.
This is using the simple "em" tag to do a caption. There's already css to deal with this in Quartz.

[![Buena Vista Bridge](notes/images/IMG_0709.jpeg)](https://google.ca)
*Buena Vista Bridge* // 📸 <small>Photo by Grant Wilson</small>


### Fig Caption 
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


### YouTube Embedding
My notes say that this Hugo shortcode should render the youtube video

![](notes/images/Shortcodes___Hugo.png)

Here goes:
{{< youtube xbILy-bCN4M >}}



> [! Question ] What Is Going On?
> This is the question that we all ask.


Someone's Figure Code Which I Assume Uses the Title as the Caption
```
<figure> <figcaption><p>{{ with .Title }} {{ . | markdownify }} {{ end }} </p></figcaption> <a href="{{ .Destination | safeURL }}" target="_blank"> <img src="{{ replace .Destination ".jpg" ".jpg.small" | safeURL }}" alt="{{ .Text }}" {{ with .Title }}title="{{ . }}"{{ end }}/> </a> </figure>
```



```
<style type="text/css">
#wrap {
    text-align:center;/*center the .caption div*/
    background:#EEF;
}
p {margin:0;}

.caption {
    display:inline-block; /*shrinkwrap the div to fit the image*/
}
p.imgwrap {
    padding:10px 0; /*The padding around the image? - If so, decrease to get the caption closer to the image.*/
}
.caption span {
    display:block;
    margin:0 12%; /*this makes up for the missing 24% of the img width - GSW- what?!? I don't get this*/
    padding: 5px 0;
    font-family: var(--font-body);
    text-align:left;
    background:oldlace;
    border-radius: 10px;
}
.caption img {
    vertical-align:bottom;
    width:50%;
}
p.nav a {
    margin:0 100px 0 0;
}
p.nav a + a {margin:0}
</style>

</head>
<body>

<div id="wrap">
    <div class="caption">
        <p class="imgwrap">
            <img src="https://grantstracks.com/wp-content/uploads/DSCF8654-1-Bluejay-Charron.jpg" alt="">
            <span>Misty woods near Wilton // photo: Fiona Bullivant</span>
        </p>
    </div>
</div>
```

By itself, the above code doesn't render what I want - but the idea was to combine it with the ``#right50`` stuff that I was having some success with.

<div id="wrap">
    <div class="caption">
        <p class="imgwrap">
            <img src="https://grantstracks.com/wp-content/uploads/DSCF8654-1-Bluejay-Charron.jpg" alt="">
          <span><em>Misty woods near Wilton // 📸 Photo: Fiona Bullivant</em></span>
        </p>
    </div>
</div>

