# How to Embed Video in Web Pages

Embedding videos in web pages can be complicated, but it is getting easier.

## Flash Player

There was a time when video on the World Wide Web required the Shockwave (later
Adobe) Flash player plugin. But all the major browesers have been able to play
video without plugins for several years now, so there is no reason for you to
use Flash. What is more, Flash has never worked on iPads and iPhones, is seldom
installed on Android tablets, and support for it is being dropped from web
browsers. You should not use Flash for your videos.

## The &lt;video&gt; Tag

Nowadays we have the HTML &lt;video&gt; tag which is used to embed a video
player in a page in much the same way we embed images using the &lt;img&gt;
tag. It can be as simple as this:

  &lt;video src="myvideo.mp4" style="width: 640px; height: 360px" controls&gt;
  &lt;/video&lt;

Which produces:

  <video src="myvideo.mp4" style="width: 640px; height: 360px" controls>
  </video>

Provided the browser has the proper decoders for myvideo.mp4, this will work.
There are two video formats on the web today: MP4 and Webm. Most browsers (as
of 2019) support both, but if you want to be sure at least 99% of your visitors
can view your video, you should provide both and let the browser pick which
one to play:

  &lt;video style="width: 640px; height: 360px" controls&gt;
    <source src="myvideo.webm" type="video/webm">
    <source src="myvideo.mp4" type="video/mp4">
  &lt;/video&gt;

Which should look the same, but play most anywhere:

  <video style="width: 640px; height: 360px" controls>
    <source src="myvideo.webm" type="video/webm">
    <source src="myvideo.mp4" type="video/mp4">
 </video>

## Responsive Video Player

You will want to set the size of your video player, as we did in the
examples above, otherwise it will be given some arbitrary small size.
With a little more effort, the player can be made responsive, that
is, it can be made to grow and shrink according to the size of the
viewer's screen.

## Encoding the Video

You can encode your videos for the web using a video editor such as
Shotcut. Or you can use a video tool such as FFmpeg. Here are the
commands we used to encode our sample video:

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

