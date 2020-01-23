## Video Formats

Digital video formats are the most complicated we discuss here. This is because
they contain a stream of carefully timed images and syncronized audio. So that
the video and audio can be played at the same time while reading through the
file from start to finish, each of these two streams is divided into chunks.
There will be a bit of video, then a bit of audio, then a bit of video again.

Uncompressed video files are huge. Full HD requires about six megabytes per
second, 360 megabytes per minute, 22 gigabytes per hour. Even standard
definition video requires three gigabytes per hour. For this reason, video is
most often compressed.

Video is compress in two ways. First not every frame is fully represented. Only
one frame every few seconds, known as a keyframe or I-frame is given in full.
Frames between keyframes are represented by describing the parts which are
different when compared to a previous or future frame within the same group.

Second, the key frames or the differences between frames are themselves compressed
using techniques which throw away detail. This is similiar to JPEG compression of
photographs. A person creating a compressed video file can adjust the amount of
detail which the program throws away choosing between high quality and small
file size.

Video compressors or encoders have a lot of leeway in how they work. This is because
the standards describe only the commands which they can write for the decompressor,
but do not define which commands they should choose when. As a consequence compressors
for new video formats start out producing poor results and get better over time
as the programmers learn to fully exploit the commands which the new format provides.

Video compressors can make a video file smaller (or the quality higher) by searching
longer for a better solution. They are frequently allowed to take hours to encode
a single hour of video since this pays off in lower data transfer and storage costs.
If a faster computer is used to do the encoding, a more thorough search can be
performed in a reasonable period of time.

The degree of compression achievable without loss of quality is also limited by
the capabilities of the playback device. Reconstructing each frame takes time.
If the instructions for doing so are too convoluted, the player may not complete
them in time and start falling behind causing the video to studder. If we build
the playback device with more computing power, it will cost more, get hotter,
and consume more power. This may not be a problem on a desktop computer, but
on a cell phone, which is battery powered, it is a big problem. If we expect
the video to be played on such devices, we may have to choose less aggressive
compression.

To learn more about the theory of video compression see:
* [Data Compression: Video](https://en.wikipedia.org/wiki/Data_compression#Video) on Wikipedia
* [Video compression picture types](https://en.wikipedia.org/wiki/Video_compression_picture_types) on Wikipedia

### The Motion Picture Experts Group

The video formats most used today were all designed by the
[Motion Picture Experts Group](https://mpeg.chiariglione.org/). This
standard-setting body has since 1988 produced a series of standards for conveying
sound and moving pictures in digital form, that is so say, as a string of numbers.

The first suite of standards is MPEG-1 which was published in 1993. It was used
for video CD's and some early Internet video. The famous MP3 format for
recorded music is part of the MPEG-1 standard. (It is called MP3 because it is
the third audio format described in the MPEG standard.)

MPEG-2 is an improved version of the standard. The first edition was published
in 1996. Some features, such as the Advanced Audio Coding (AAC) were introduced
later. MPEG-2 is used for digital broadcast TV is most of the world. It is also
the format used on DVD. But in many areas, including on computers and the
Internet it is obsolete, having been replaced by MPEG-4.

The MPEG-3 standard was never completed. The good parts where incorporated into
later revisions of the MPEG-2 standard. This is probably just as well, since
it would have been confused with MP3 audio.

MPEG-4 was first published in 1996. It brought provided a moderately-improved
picture format know as the Advanced Simple Profile (ASP).  The Advanced Audio
Coding (AAC) added to the MPEG-2 in 1997 is the dominant format for the audio
track. An addendum known as Part 10 which was published in 1999 defined a new
and improved picture format known as H.264 which soon displaced ASP.

As of 2020 the most popular video format used on the Internet is MPEG-4 with
the picture in H.264 and the audio in AAC. This is one of two key formats used
by Youtube. It is also the format in which must consumer devices such as video
cameras and smartphones record.

### Ogg Theora Video

Because the MPEG standards are each covered by numerous patents, using them can
be expensive and in the case of free software may be impossible. For that
reason a need was perceived for patent free alternatives. A number of
organizations have participated in the effort to produce them.

On2 Technologies performed the initial work to develop video compression
formats while avoiding known patents. In September 2001 they released their VP3
video format for free use. The Xiph.org Foundation used it as the basis for the
Theora video format. Early implementations of Theora had defects which impaired
quality, but by 2009 these had been corrected and Theora was producing results
much closer to those of the best MPEG-4 video format, H.264.

Theora video is usually combined with Vorbis audio in an OGG container. As of
January 2020 this this combination is playable on about 40% of web browsers.

### VP8, VP9, and AV1

On2 Technologies continued to work on improved its video coding formats and
released VP8 in 2008.  In 2009 Google bought On2 Technologies and released VP8
for free use the next year. VP8 produces results so close to those of H.264
that few viewers can tell the difference.

The VP9 video coding format released in 2013 produces results much better than
those of H.264. While Theora and VP8 were niche formats, VP9 is seeing wide use
for streaming video on the Internet starting with Google's own Youtube.

The successor to VP9 is AV1.

VP8 and VP9 video with Opus audio in a Webm container will play on about 90% of
browsers. Because is still very new, AV1 will play on only about 30% of browsers.

