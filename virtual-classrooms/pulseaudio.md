Most Linux distributions use the Pulseaudio sound server.

## Pulseaudio Concepts

A *source* is a real or virtual device from which a program can receive audio input.
There will be a source for each microphone or line-in jack on your computer.

A *sink* is a real or virtual device to which a program can send its audio output.
There will be a sink for the speaker jack on your computer.

Every sink has an accompanying *monitor source*. A program can connect to the
monitor source in order to receive the mixed audio from all the programs currently
playing sound into the sink. For example, the monitor source belonging to the sink
for your headphones or speakers might be used by a video conferencing application
while you were sharing your screen so that the other participants could hear sounds
played by programs on your screen.

## Configuration

There are two main commands for configuring the Pulseaudio server. The first is
**pacmd** which is just a tool for transmitting Pulse CLI commands to the
Pulseaudio server.

The second is **pactl** which implements some of the same commands but with
enhancements such as abbreviated output formats.

## Mixer Control

Desktop environments generally provide a mixer GUI capable of controlling the
Pulseaudio server. You can also use the mixer GUI included with Pulseaudio:

    $ apt install pavucontrol
    $ pavucontrol

## Loading and Unloading Modules

You can use the **pactl** or **pacmd** command to load modules or more
precisely create instances of available modules. You will usually do this to
create virtual devices, filters, and adapters.

The command to load a module is:

    $ pactl load-module *module* *arguments*

If successful, this command will print a number. If you remember this number,
you can use it to identify the module later if you want to unload it:

    $ pactl unload-module *N*

If you want to unload a module, but do not know its ID number, find it
with this command:

	$ pactl list short modules

You can also unload all modules of a particular type in one fell swoop.
For example:

    $ pactl unload-module module-null-sink

There does not seem to be a way to remove a module instance using the
name specified when creating it. This is very strange.

## Pulseaudio Configuration Files

If the Pulseaudio server is running as part of the users session, then
it will get the list of module to load from ~/.config/pulse/default.pa,
if it exists, otherwise from /etc/pulse/default.pa.  

The commands in this configuration file are presumably in the format
accepted by **pacmd**.

## Equalizer

Pulseaudio has a build-in graphic equalizer called **module-equalizer-sink**
which can be inserted into the audio chain. The equalizer provides a new sink
to which can be selected as the output devices. In sends the equalized audio
stream to the original output sink.

To install the Pulseaudio equalizer and start the GUI:

    $ sudo apt install pulseaudio-equalizer
    $ qpaeq

The equalizer GUI loads **module-equalizer-sink**, if it is not loaded already.
You then have to select the equalizer's sink as the output device. You can
do this using your desktop environment's sound settings panel or you can
use **puvucontrol** where the default output is refered to as the "fallback".
Or you can configure an individual program, such as a music player to send
its output to the equalizer's sink.

## Virtual Audio Cables

To patch audio from a source (such as your microphone) through to a sink (such
as your speakers), use the **module-loopback**:

    $ pactl load-module module-loopback

The loopback module pulls audio from the source and sends it to the sink
as if it were an audio recorder with the monitor function turned on.

To understand why this is called loopback, imagine you are looking at the
jacks on the back of your computer. The sound goes in through the microphone
jack, loops back and comes out the speaker jack.

While you can select the source and sink using command line options when
loading the module, it may be easier to just let it pick and then change
the selection using **puvucontrol**.

If instead you want to make the audio output of one program the input of
another, you can use **module-null-sink**:

    $ pactl load-module module-null-sink sink_name=test_null_sink

This is useful for feeding the sound output of OBS Studio into the sound input of
a video conferencing application such as Zoom or Skype. OBS Studio writes to the
null sink and Zoom or Skype reads the corresponding monitor source. Generally
you would set the sink and source in each program.

## References

* [PulseAudio under the hood](https://gavv.github.io/articles/pulseaudio-under-the-hood/)
* [PulseAudio Loopback](https://endless.ersoft.org/pulseaudio-loopback/)


