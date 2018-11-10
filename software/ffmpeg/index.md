FFmpeg is a command-line program for processing audio and video recordings.
It is widely used to convert files from one format to another or to
recompress them to make them small enough for distribution. It has numerous
options for cropping video, selecting start and end times, and much more.

This program is is not intended as an easy-to-use tool for beginners. But
many easy-to-use tools use FFmpeg to do the work behind the scenes. But it
can be used by non-experts thanks to the numerous recipies available on the
Internet.

## Recipies

Here are some recipies which are likely to be useful to teachers.

### Trim a Video File

These commands both cut an eight-second piece out of movie.mp4 starting three
seconds in and save it as clip.mp4:

 $ ffmpeg -i movie.mp4 -ss 00:00:03 -t 00:00:08 -c copy clip.mp4

 $ ffmpeg -i movie.mp4 -ss 00:00:03 -to 00:00:11 -c copy clip.mp4


