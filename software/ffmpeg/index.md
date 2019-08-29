FFmpeg
==================================

[FFmpeg](https://www.ffmpeg.org) is a command-line program for processing audio and video recordings.
It is widely used to convert files from one format to another or to
recompress them to make them small enough for distribution. It has numerous
options for cropping video, selecting start and end times, and much more.

This program is is not intended as an easy-to-use tool for beginners. But
many easy-to-use tools use FFmpeg to do the work behind the scenes. But it
can be used by non-experts thanks to the numerous recipies available on the
Internet.

## Links

* https://amiaopensource.github.io/ffmprovisr/

## Recipes

Here are some recipes which are likely to be useful to teachers.

### Trim a Video File

These commands both cut an eight-second piece out of movie.mp4 starting three
seconds in and save it as clip.mp4:

    $ ffmpeg -i movie.mp4 -ss 00:00:03 -t 00:00:08 -c copy clip.mp4

    $ ffmpeg -i movie.mp4 -ss 00:00:03 -to 00:00:11 -c copy clip.mp4

The parameters:

    **-i** the name of the input file

    **-ss** the start time of the clip

    **-t** the duration of the clip

    **-to** the end time of the copy

    **-c copy** copy the audio and video information unchanged. This preserves
      the quality and leaves the compression method the same.

### Reencode a Video File

    $ ffmpeg -i movie.mp4 _video options_ _audio_options_ movie_out.mp4 

These video options will produce a high-quality result:

    -c:v libx264 -profile:v high -level 4.1 -preset slow -pix\_fmt yuv420p -crf 25

These audio options are good, but they require an FFmpeg compiled from source:

    -c:a libfdk\_acc -profile:a aac\_he -ar 48000

These options are known to work with the FFmpeg supplied with Ubuntu 18.04:

    -strict experimental -c:a aac -ar 48000

### Scaling

To reduce the resolution of the image, use the scale video filter. For example,
if you have 1280x720 video and want to reduce it to 640x360, add this
filter to the ffmpeg command:

    -vf scale=640:-1



