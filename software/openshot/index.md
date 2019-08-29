Using Openshot to Edit Video
============================

[Openshot](https://www.openshot.org) is a non-linear video editor. This means
that you can load a bunch of
video files into it, select pieces from them, and assemble them into a time
line. Once the time line is ready, you can export it as a single video file.
The original video files are left untouched. You can also insert title cards
and effects such as fading from one shot to another.

As of March 2016 Openshot is still prone to crashing. We wish we could
recommend something better that is cross-platform, but have not found anything
yet. Hopefully the 2.0 version which is now in beta testing will be more
stable.

Exporting Video
---------------

If you export video in h.264 and VP9 format, most browsers will be able to play them.

The following parameters work well for exporting instructional video in h.264 format:

| Target             | MP4 (h.264)         |
| Video Format       | mp4                 |
| Video Codec        | libx264             |
| Video Bitrate      | 1MB/s               |
| Audio Codec        | aac                 |
| Number of Channels | 1                   |
| Sample Rate        | 48000/s             |
| Sample Size        | 16 bits per channel |
| Bitrate            | 64kb/s              |

The video file produced will not work with the HTML 5 &lt;video&gt; tag. It must be reformatted first:

$ MP4Box -inter 500 filename.mp4

The following parameters work well for exporting instructional video in VP9 format:

| Dimensions         | 640x480    |
| Target             | WEBM       |
| Video Coded        | libvpx-vp9 |
| Video Bitrate      | 1MB/s      |
| Audio Codec        | libvorbis  |
| Number of Channels | 1          |
| Bitrate            | 64kb/s     |


