## Audio Formats

Audio is stored in a computer as a list of **samples**. Each sample is a
measurement of the signal's voltage at a specific moment in time. The signal
will be sampled many thousands of times a second. When the files is played back
these measurements are used to generate the original voltages. The signal is
then smoothed out a little and sent to the speakers or headphones.

Audio recordings can be characterized by the number of bits which are used to
record each voltage measurement, the number of measurements which are recorded
per second, and the number of channels recorded. Telephone-quality audio has
8-bit samples, recorded at the rate of 8000 per second, and a single channel.
CD-quality audio has 16-bit samples, recorded at a rate of 44,100 samples per
second, and two channels.

CD audio is not compressed, but audio files shared on the World Wide Web and
through streaming services are compressed so that they will download more
quickly. Compressing audio involves replacing the original list of samples with
a description of how to reproduce them more or less faithfully.

### Lossless and Lossy Formats

When audio files are highly compressed for distribution on the Internet, some
of the audio information is thrown away. Such compression schemes are called
"lossy".  If an audio file in a lossy format is edited and resaved, even more
detail will be lost, so this should be avoided. You should keep your master
files in a lossless format such as WAV or FLAC and convert them to MP3, M4A, or
OGG as a final step.

### WAV Files (Lossless)

WAV is an audio format developed by Microsoft and IBM. It is a container format
which can have various audio formats inside. Uncompressed WAV files are
frequently used as a master format. While web browsers can play them, it is
better to convert your final recordings to a compressed format such as MP3 or
OGG before including them in your web pages. You should keep the original WAV
file in case you need to make changes and recompress.

### FLAC Files (Lossless)

FLAC files contain audio which has been compressed in a way which allows full
reconstruction of the original audio. Because nothing is thrown away, the space
saving is only about 50%. FLAC is a popular format for high-quality music
collections.  FLAC files are to large for the World Wide Web and are not
supported by all browsers.

### MP3 Files (Lossy)

MP3 stands for "MPEG 1 layer 3 audio". It is one of the options for compressing
the audio track in an obsolete digital video standard called "MPEG 1".

MP3 files compress the audio to about 10% of its original size, depending on the
bitrate chosen. To accomplish this some of the details are thrown away. Voice
recordings can be compressed more than music. If an MP3 file is compressed
to heavily, a ringing noise may be heard behind the speakers voice.

Almost all web browsers can play MP3 files. Playback was covered by patents,
but these are all thought to be expired.

### M4A Files (Lossy)

M4A audio files use one of the compression methods from the MPEG 4 video standard.
Usually the compression method is the Advanced Audio Coding (AAC). Because this
is a newer standard than MP3, the audio quality will be higher for the same file
size or the file size will be smaller for the same quality.

AAC is still covered by patents, so while most all browsers can play it, support
is not quite as high as it is for MP3.

### OGG Files (Lossy)

Because MP3 was covered by patents, a pattent-free alternatives were sought. The
most popular is the OGG container format with the Vorbis codec inside. Most
browsers will play it, but Internet Explorer will not and Safari may not.

Just as AAC is an improvement over MP3, there is a modern improvement over Vorbis
which is known as Opus. Modern web browsers which can play OGG files support
both Vorbis and Opus.

