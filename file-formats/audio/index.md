---
author: David Chappell
---

## Audio Formats

Audio is stored in a computer as a list of **samples**. Each sample is a
measurement of the signal's voltage at a specific moment in time. The signal
will be sampled many thousands of times a second. When the files is played back
these measurements are used to generate the original voltages. The signal is
then smoothed out a little and sent to the speakers or headphones.

A digital audio recordings at the moment of digitization is characterized
by the following parameters:

* The number of bits which are used to record each voltage measurement.
  For CD's, video DVD's, and most computer files 16 bits must be recorded.
* The number of "samples" or measurements which are recorded per second.
  8000 samples per second is used for telephone calls. CD's use 44,100
  samples per second. A video DVD's soundtrack (most often) records
  48,000 samples per second.
* The number of channels recorded. Spoken word recordings are generally
  monaural which means that they record one channel. Stereo recordings
  have two channels, one for the left speaker, one for the right.
  Suround sound will have more channels for additional speakers which may
  be in the rear or center or for a subwoofer.

CD audio is not compressed, but audio files shared on the World Wide Web and
through streaming services *are* compressed so that they can be downloaded more
quickly. Audio compression methods can be characterized as either lossless
or lossy.

### Lossless and Lossy Formats

Because digital audio files record thousands of samples per second, they get
big very quickly. Ten minutes of music in CD-quality stereo takes 100
megabytes. 

Audio files, like other digital files can be compressed. A general purpose data
compression algorithm such as DEFLATE could shrink an CD-quality audio file to
80 to 90 percent of its original size. An algorithm such as FLAC which is
designed specifically with the patterns of audio data in mind can shrink it by
50 to 70 percent of its original size. During decompression the original audio
data is reconstructed perfectly. For this reason algorithms such as DEFLATE and
FLAC are described as **lossless**.

Losslessly compressed audio files are still pretty big. Much higher compression
can be achieved if we are willing to accept a slightly less than perfect
reproduction of the original audio. If this is done carefully, the audio
file can be reduced to less than ten percent its original size while sounding
so close to the original that few can hear the difference.

If you are making and distributing audio recordings, it is best to use lossless
formats such as WAV or FLAC for your master copies. When you are ready to
distribute the recordings, you can convert them to a lossy format such as MP3,
AAC, or Ogg so that they will download more quickly. If you later have to
make changes, you should go back to the original lossless masters. If you
edited the lossy file instead and recompressed them, you would lose a little
quality each time.

More information about digital audio concepts and digital audio compression can
be found in the article [Digital audio concepts](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_concepts)
at Mozilla.org.

### LPCM WAV Files (Lossless)

WAV is an audio container format developed by Microsoft and IBM. WAV files with
LPCM format audio inside are frequently used as a master format. These files
are uncompressed, so they can be quite large.

As of January 2020 95% of web browsers can play LPCM WAV files. This is convenient
for testing, but on a public website it is better use MP3, AAC, or Ogg files.

### FLAC Files (Lossless)

FLAC files contain audio which has been compressed in a way which allows full
reconstruction of the original audio. Because nothing is thrown away, the space
saving is seldom more than 50%. FLAC is a popular format for high-quality music
collections.

As of January 2020 over 90% of browsers will play FLAC. FLAC files are smaller
than PCM WAV files, but are still overkill for almost all applications.

### MP3 Files (Lossy)

MP3 stands for "MPEG-1 layer 3 audio". MPEG-1 is a now-obsolete standard for
compressing videos. MP3 is the third of three options for encoding the 
audio track.

MP3 files compress CD-quality audio to about 10% of its original size by
throwing away details which most people cannot hear. The degree of compression
is expressed in bits per second. 128 bits per second produces acceptable music
reproduction. 64 bits per second is frequently used for voice recordings. If an
MP3 file is compressed too heavily, a ringing noise that sounds a bit like
squeaking mice can be heard behind the speaker's voice.

Like many other lossy compression formats, MP3 defines how the file should be
decoded and played, not how it should be encoded. The author of the encoder has
leeway to choose between various possible encodings. MP3 encoders have gotten
better over the years. The opensource [LAME encoder](https://lame.sourceforge.io/)
is widely acknowledge as the best. You can download and use it directly, or
you can use a tool which includes it such as FFmpeg or Audacity.

Like other MPEG standards, MP3 was covered by patents, but it appears the last
of these expired in 2017. This means that this already very popular format can
be deployed everywhere. Though it has been surpassed technically, its ubuquity
gives it a decided advantage. As of January 2020, about 97% of web browsers can
play MP3 files.

### Advanced Audio Coding (Lossy)

The Advanced Audio Coding (AAC) is an MPEG standard which is intended to
replace MP3. The most popular form, AAC-LC, can provide near-CD quality stereo
sound at 128 kbps (about 30% less than MP3 would require). The AAC-HE v1 and
provides medium quality stereo audio (suitable for Internet radio and podcasts)
at around 64 kbps. AAC-HE v2 provides the same at about 32 kbps.

Though AAC is still covered by patents, as of January 2020, about 97% of web
browsers can play AAC audio as long as it is in an MP4 container. Because of
the patents, the Firefox web browser can play AAC only if the underlying
operating system has an AAC decoder it can use.

### OGG Vorbis (Lossy)

When in 1998 it became known that the MP3 was covered by patents, programmar
Christopher Montgomery created and a container format called Ogg and an audio
encoding format called Vorbis. Today the Vorbis specification is maintained by
the Xiph.org Foundation. Thos less popular than MP3, Vorbis is techically
superior and so an Ogg Vorbis file can be smaller than an MP3 file while
keeping the same audio quality.

As of January 2020 about 90% of web browsers will play Ogg files with Vorbis audio.
Internet Explorer will not and Safari may not depending on whether a Ogg Vorbis
decoder is installed in the operating system.

### Opus (Lossy)

Starting in 2010 the Xiph.org Foundation, together with Skype and Mozilla created
a new audio coding standard called Opus. This new format was published as
Internet Engineering Task Force (IETF) standard RFC 6716.

Opus is intended as a successor to Vorbis and Speex, another audio encoding
from the Xiph.org Foundation. Opus produces excellent results in a wide range
of applications from high fidelity surround audio to Internet telephone calls.
As of January 2020 it is considered superior in quality to all other popular
lossy audio codings including MP3, Vorbis, and AAC. A 64 kbps Opus file has
about the same quality as a 128 kbps MP3 file.

Opus is one of the two formats (the other is Vorbis) which may be used in Webm
video files. It is used extensively in videos streamed from Youtube and other
sites.

As of January 2020 about 90% of web browsers will play Ogg files with Opus audio.
About 90% of browsers will also play Opus audio from a Webm video file.

### Quality Comparison

In listening tests with the best encoders the various audio formats are
are frequently ranked in this general by ascending quality:

1. MP3
2. AAC and Vorbis
5. Opus

At bitrates above 128 kbit/s few people can tell the difference.

