---
author: David Chappell
---

## How to Trim and Reencode Video Files

Here are FFmpeg commands which we have found useful for making clips
from video files. We also show you how to reencode the video. You may
need to do this in order to make the smaller or to get the video into
a format which your player can play.

### Trim a Video File

These commands both extract an eight-second piece out of movie.mp4 starting three
seconds in and save it as clip.mp4:

    $ ffmpeg -i movie.mp4 -ss 00:00:03 -t 00:00:08 -c copy clip.mp4

    $ ffmpeg -i movie.mp4 -ss 00:00:03 -to 00:00:11 -c copy clip.mp4

Here is what each parameter means:

**-i** the name of the input file

**-ss** the start time of the clip

**-t** the duration of the clip

**-to** the end time of the copy

**-c copy** copy the audio and video information unchanged. This preserves
      the quality and leaves the compression method the same.

Because the command above does not reencode the video, it has to include
additional material at both the start and the end until it reaches the next
keyframe. It then inserts instructions telling the player not to show this
material. This hidden material may be several seconds long. If you need to make
sure nobody can possibly see this extra material or you will be using a player
which does not handle this situation properly, you will need to reencode the
video.

### Reencode a Video File (H.264 codec)

As of January 2020, one of the most popular video formats is MPEG-4 with the
H.264 video codec and the AAC audio codec. This will play on most computers,
smartphones, and inexpensive standalone devices which play video from a thumbdrive.

The general form of the command to convert video to this format is:

    $ ffmpeg -i movie_in.mp4 _video options_ _audio_options_ movie_out.mp4 

Here are some video options which will produce a high-quality result:

    -c:v libx264 -profile:v high -level 4.1 -preset slow -pix_fmt yuv420p -crf 25

Here is what each parameter means:

**-c:v** use the H.264 video codec.

**-profile:v high -level 4.1** tells the H.264 encoder it is ok to use
advanced compression methods, our player can deal with it.

**-preset slow** tells the H.264 encoder to take its time and do a good job.
It may take a few hours to encode an hour-long video. If you cannot wait,
change this to **-preset fast**.

**-pix_fmt yuv420p** tells FFMpeg how to encode the color information.
If you leave this out, and the input file uses some other encoding,
some hardware players may be unable to play the file produced.

**-crf 25** sets the level of compression. Higher numbers mean more
compression and more loss of detail. Noticable smearing sets in around 35.

H.264 video is usually paired with AAC audio. These audio options are good,
but they require an FFmpeg compiled from source:

    -c:a libfdk_acc -profile:a aac_he -ar 48000

These options are known to work with the FFmpeg supplied with Ubuntu 18.04:

    -strict experimental -c:a aac -ar 48000

### Reencoding a Video File (VP9 codec)

VP9 is a newer codec from Google. It will play in recent releases of VLC
and in most web browsers, but not on most standalone hardware devices.
VP9 video is usually combined with Opus audio in a Webm container.

The general form of the command to produce a Webm file is:

    $ ffmpeg -i movie_in.mp4 _video options_ _audio_options_ movie_out.webm 

These video options will produce a high-quality result:

    -c:v libvpx-vp9 -speed 1 -pix_fmt yuv420p -crf 35

And here are reasonable audio options:

	-c:a libopus -ar 48000

### Reencoding a Video File (MPEG-4 Part 2)

On a typical desktop computer circa 2018 encoding a video using the H.264 codec
as described above will take about two minutes for every minute of video. The
VP9 codec can take even longer. During this time the computer is working hard
searching for a way to make the file as small as possible while preserving
quality. This is important when you will be distributing your videos on disks
or on the Internet since more of them fit and they can be downloaded more
quickly.

But sometimes you need a video encoded right away such as to show at a class
which will start in a few minutes. At these times you can use an obsolete
codec from when computers were less powerful.

A good choice for this is the MPEG-5 Part 2 codec.  These video options are a
good starting point:

	-c:v mpeg4 -qscale:v 7

On a modern computer this will encode an hour-long video in about 15 minutes.
It will be nearly twice as large as the same video in H.264, but that is the
price you pay for speed.

**qscale:v** sets the level of compression. A lower number gives higher quality
video, a higher number produces smaller files.

While in the past MPEG-4 Part 2 video was often paired with MP3 audio, for this
application it is reasonable to pair it with AAC audio and put them in an MP4
container like with did for H.264. See above for the AAC options.

### Scaling the Video

To reduce the resolution of the image, use the scale video filter. You may
want to do this if you now that the video will be played in a small window
or on a device with limitted resolution. Cutting the resolution will allow
the file to be much smaller and it may play more smoothly on old devices.

For example, if you have 1280x720 video and want to reduce it to 640x360,
add this filter to the ffmpeg command:

    -vf scale=640:-1

Here we specify the target width and allow FFmpeg to computing the
cooresponding new height. You can add this option to any of the commands above.

