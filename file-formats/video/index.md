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

MPEG-4 was first published in 1996. It provided a moderately-improved picture
format know as the Advanced Simple Profile (ASP).  An addendum known as Part 10
which was published in 1999 defined a new and improved picture format known as
H.264 or the Advanced Video Coding (AVC) which soon displaced ASP.

In 2013 MPEG publish a H.265 or the High Efficiency Video Coding (HEVC) which
is intended to produce picture quality as good as H.264 while compressing it
twice as much.

There are so many patents claimed on MPEG standards that it can be difficult to
determine when they become patent-free. It is thought that patents on MPEG-1
expired in 2003, except for layer 3 (MP3) which expired in 2017. MPEG-2 patents
were probably all expired by 2018. Patents on ASP decoders seem to have expired in
2012. ASP encoder patents may expire in 2022. The last known patent on H.264
does not expire until 2027.

As of 2020 the most popular video format used on the Internet is MPEG-4 with
the picture in H.264 and the audio in AAC. This is one of two key formats used
by Youtube. It is also the format in which must consumer devices such as video
cameras and smartphones record. As of January 2020 this combination will play
in about 95% of web browsers. ASP video and MP3 audio will also likely work.
You should assume that web browsers will not play MPEG-1 or MPEG-2 videos.

### Software Patents

An organization called MPEG LA serves as an agent for holders of about a
thousand patents which supposedly apply to the MPEG standards.

In 1997 MPEG LA charged $4 for an MPEG-2 encoder or decoder and $6 for a device
which needs both. Market forces have pushed prices down. As of 2015 MPEG LA
charged about $0.10 for each H.264 encoder or decoder in a consumer device such
as a video camera or a computer and $0.16 for a device which does both. Paying
$0.16 royalty on a $200 video camera or a $600 iPhone is no big deal. But it is
a serious problem for publishers of free software.

Let us take the Firefox web browser as an example. In 2010, the last year from
which I could find statistics, Firefox was [download on average 1.5 million
times a day](https://gigaom.com/2010/05/27/firefox-downloads-active-user-metrics/).
So if Firefox were to include an H.264 decoder, the royalties would be $150,000
per day with no way to pay them.

This situation has caused considerable consternation. An important reason the
Internet was able to rise from an obscure network in the 1990's to the world's
network is that the core technologies are in the public domain. Nobody needed
to seek permission and persuade a corporation to license its technology on
favorable terms before they could create a web site or a new web browser.
Now giant companies such as Google, Amazon, and Yahoo were started as hobby
projects or small businesses in college dorm rooms and garages.

Many saw it as a serious problem that such a basic feature of the 21st century
Internet as streaming video was not available under the free and open terms which
had made the Internet great. They argued that this made MPEG unsuitable as the
standard video format for the Internet.

MPEG LA was aware of this delicate situation. If they charged to much or if
they charged people who had no way to pay, such as hobbiests running web sites,
MPEG might be rejected by Internet users. So they made the royalty very low and
promised not to charge for the first 100,000 encoders and decoders per year.
They also waived the per-video charge in cases where videos were distributed
for free. This was enough for MPEG video to become the dominate format on the
Internet despite misgivings.

Neverthless there remains a desire in many quarters to find a completely
royalty free alternative to MPEG-4. There is also a certain amount of
resentment about the patents themselves. Software patents as a class are viewed
by computer programmers with almost universal contempt. To qualify for a
patent, an "invention" has to go beyond what we would expect a competent
practitioner to come up with in the ordinary course of doing his job. Software
patents seldom actually meet this legal standard.

Junk software patents can be manufactured at will without having to invent
anything. Company lawyers interview programmers and write up the ordinary
solutions they used. Harried patent examiners approve these trivial patents.
Companies collect them as legal-defense ammunition. If a competitor sues them
for patent infringment, they can sue right back. The very vagueness and
triviality of these patents makes it a forgone conclusion that the competitor
is violating several of them. At this point both sides agree to "cross
license" their patents which is a face-saving way of dropping the whole thing.

We can safely assume that very few of the 1000 patents which supposedly must be
licensed in order to use MPEG video actually describe valuable inventions which
anyone, given the choice, would choose to license. But once the things they
describe are required by a popular standard, then everyone has to license them
or risk being sued. The Motion Picture Experts Group could have weighted the
cost of licensing various patents when which techniques to incorporate into
the standard, but did not. In a few cases MPEG members are suspected of getting
algorithms of dubious value mandated by the standard so that they could collect
royalties on their use.

The situation with patents on MPEG video has deteriorated with the introduction
of the new H.265 standard for which about ten thousand patents are claimed.  As
before, some can be licensed from the MPEG LA for $0.10 per device.  Some more
can be licensed from a new organization, HEVC Advance, which announced that
they would be charging $2.80 per device and be taking a share of the revenue of
video service which use HEVC, though they have made some concessions since.
Nor is it clear whether a license from these two companies will cover all of
the patents. H.265 was expected to become the dominant standard, replacing
H.264, but the patent fiasco has thrown its future into doubt.

At first glance it would seem that users of any competing standard would have
to license most of these patents too if they wanted their standard to be any
good, but this is not necessarily the case. First, the patents on earlier
versions of the MPEG standards have expired or will expire soon. Second, many
of the remaining patents are so narrow and arbitrary that they can be
circumvented simply by selecting a slightly different solution. Third, if the
royalties become too onerous, large organizations may start fighting back in
the courts and bring their own defensive patent portfolios to bear.

### Ogg Theora Video

One company which attempted to produce a patent free video coder is On2 Technologies.
Their programers studied the known video encoding patents and avoided doing what
was described in them. In September 2001 they released their VP3 video format for
free use and the Xiph.org Foundation (which had already produced the OGG Vorbis and FLAC
audio formats) developed it furthur into the Theora video format. Though early
implementations of Theora had defects which impaired quality, but by 2009 these had
been corrected and Theora was producing results comparable to those of the first
MPEG-4 format, ASP.

Early drafts of the HTML5 standard required that web browsers be able to play
Theora video Vorbis audio in an OGG container. Advocates of a free and open
Internet spoke elequently in its favor. They argued that web site operators
should have at least royalty-free video format of acceptable quality which they
could be confident would play on all devices. However this proposal faced
opposition, particularly from Apple which had already committed to H.264 and
had no problem paying a $0.10 fee for each iPhone. They had already spent the
effort to create special hardware to play H.264 without draining the battery
to quickly and did not want to repeat that work for a format with lower
picture quality. The requirement to support Vorbis was eventually dropped from
the HTML5 standard.

As of January 2020 only about 40% of web browsers can play Ogg Theora video.

### VP8 and VP9

But that was not the end of the matter. On2 Technologies continued to work on
improving its video coding formats and released VP8 in 2008. In 2009 Google,
clearly sick of the whole video patent thing, bought On2 Technologies and
released VP8 for free use the next year. VP8 produced results approximately
equal to those of H.264.

The MPEG LA announced that they would identify patents which covered VP8 and
sell licenses, but this drew unfavorable attention from the United States
Department of Justice on anticompetitive grounds. Google got involved and the
matter was dropped. Nokia sued HTC and Google in Germany and lost.

The VP9 video coding format released in 2013 produces results nearly as good as
those of H.265 (HEVC). VP9 is seeing wide use for streaming video on the
Internet starting with Google's own Youtube.

VP8 and VP9 video is usually combined in a Webm container with Opus audio. As
of January 2020 these Webm video combinations will play on about 90% of web
browsers.

### AOMedia Video 1 (AV1)

Google started work on VP10, but then decided to join forced pool its efforts
with Xiph.org (Mozilla) and Cisco which had also been working on open video
standards. They were joined by Amazon, Apple, ARM, Facebook, IBM, Intel,
Microsoft, Netflix, Nvidia, Samsung, and Tencent in the Alliance for Open Media.

The AV1 standard was released in January 2019. It provides about the same level
of compression and picture quality as H.265 (HEVC). As of January 2020 about
30% of web browsers can play AV1 video. A number of online video services,
including Youtube and Vimeo, are experimenting with it.

### Recomendations

As of January 2020 we recommend that when embedding videos in a web site you encode
them twice, in the following formats:

* MPEG-4 with H.264 video and AAC audio
* Webm with VP9 video and Opus audio

If you use this combination, nearly 100% of visitors will be able to play your video.
See our tutorial [How to Embed Video in Web Pages](../howto/embed-video/) for instructions.


