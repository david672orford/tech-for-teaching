# How to Embed Video in Web Pages

Embedding videos in web pages can be complicated, but it is getting easier.

## Flash Player

There was a time when video on the World Wide Web required the Shockwave (later
Adobe) Flash player plugin. But all the major browesers have been able to play
video without plugins for several years now, so there is no reason for you to
use Flash. What is more, Flash has never worked on iPads and iPhones, is seldom
installed on Android tablets, and support for it is being dropped from web
browsers. You should not use Flash for your videos.

## The `<video>` Tag

Nowadays we have the HTML `<video>` tag which is used to embed a video
player in a page in much the same way we embed images using the `<img>`
tag. It can be as simple as this:

```html
<video src="myvideo.mp4" style="width: 640px; height: 360px" controls>
</video>
```

Which produces:

<video src="myvideo.mp4" style="width: 640px; height: 360px" controls>
</video>

Provided the browser has the proper decoders for myvideo.mp4, this will work.
There are two video formats on the web today: MP4 and Webm. Most browsers (as
of 2019) support both, but if you want to be sure at least 99% of your visitors
can view your video, you should provide both and let the browser pick which
one to play:

```html
<video style="width: 640px; height: 360px" controls>
 <source src="myvideo.webm" type="video/webm">
 <source src="myvideo.mp4" type="video/mp4">
</video>
```

Which should look the same, but play most anywhere:

<video style="width: 640px; height: 360px" controls>
  <source src="myvideo.webm" type="video/webm">
  <source src="myvideo.mp4" type="video/mp4">
</video>

## Responsive Video Player

But there is a problem with the players above. If the screen is narrow,
as it might be on a smartphone, the right-hand side of the picture will
be cut off. We really want the picture to get smaller while maintaining
the same aspect ratio. We can do this, but we have to wrap the `<video>`
tag in three `<div>` tags and style them:

```html
<div style="width:auto">
  <div style="width:640px; max-width:100%">
    <div style="padding-top:56.25%; position:relative">
      <video style="position:absolute; top:0; left:0; width:100%; height:100%" controls>
        <source src="myvideo.webm" type="video/webm">
        <source src="myvideo.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>
```

This looks complecated. Let's take it one step at a time starting from
the outermost `<div>`:

1. The outermost `<div>` has its width set to "auto" (which is the default).
   It will fill all of the horizontal space between the margins. (Setting
   it to "100%" not always work since that means "100% of the parent's width
   which would be too wide if the parent has padding enabled.) This `<div>`
   serves to create a context in which "100%" means "the space between
   the left and right margins".
2. The next `<div>` sets the width. It is 640 CSS pixels, up to the full
   width of the first `<div>`.
3. The third `<div>` establishes the height of our player. For layout purposes
   this `<div>` is empty (since we are going to use absolute positioning on the
   `<video>` tag which will take it out of the flow). It's height is established
   by its top padding which we have set to "56.25%" (360 divided by 640 and
   multiplied by 100). This is 56.25% of the *width* of the parent `<div>`,
   so this establishes the desired aspect ratio. Finally
4. Finally we 

And we get this:

<div style="width:auto">
  <div style="width:640px; max-width:100%">
    <div style="padding-top:56.25%; position:relative">
      <video style="position:absolute; top:0; left:0; width:100%; height:100%" controls>
        <source src="myvideo.webm" type="video/webm">
        <source src="myvideo.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</div>

## Encoding the Video

You can encode your videos for the web using a video editor such as
Shotcut. Or you can use a video tool such as FFmpeg. Here are the
commands we used to encode our sample video:

```bash
ffmpeg -i myvideo_original.mp4 \
  -c:v libx264 -profile:v high -level 4.1 -preset slow -pix_fmt yuv420p -crf 30 \
  -strict experimental -c:a aac -ar 48000 \
  -vf scale=640:-1 \
  myvideo.mp4

 ffmpeg -i myvideo_original.mp4 \
  -c:v libvpx-vp9 -speed 1 -pix_fmt yuv420p -crf 35 \
  -c:a libopus -ar 48000 \
  -vf scale=640:-1 \
  myvideo.webm
```

