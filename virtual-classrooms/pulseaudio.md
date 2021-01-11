Most Linux distributions use the Pulseaudio sound server.

## Pulseaudio Concepts

A *source* is a real or virtual device from which a program can receive audio input.

A *sink* is a real or virtual device to which a program can send its audio output.

Every sink has an accompanying *monitor source* from which a program can read in order
to 'hear' what is being played through it. For example, a video conferencing application
might read from the monitor source of the sound card output sink in order to transmit
program sound during screen sharing.

Virtual devices such as equalizers may provide both a *sink* (input), write their
output to another *sink* and also provide the usual monitor *source* (output).
This makes it possible to insert them into the audio stream or record their
output.

## Configuration

There are two main configuration commands. The first is **pacmd** which
is just a tool for transmitting Pulse CLI commands to the Pulseaudio
server.

The second is **pactl** which implements some of the same commands
but with enhancements such as abbreviated output formats.

## Mixer Control

Desktop environments generally provide a mixer GUI capable of
controlling the Pulseaudio server. You can also use the mixer
GUI included with Pulseaudio:

    $ apt install pavucontrol
    $ pavucontrol

## Loading and Unloading Modules

You can use the **pactl** or **pacmd** command to load modules or more
precisely create instances of available modules. You will usually do
this to create virtual devices, filters, and adapters.

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

Pulseaudio has a build-in graphic equalizer which can be inserted into the
audio chain:

    $ sudo apt install pulseaudio-equalizer
    $ qpaeq

When the equalizer GUI starts it loads **module-equalizer-sink** and connects
its output to an audio devices. It does not necessarily connect anything
to the input. You have to select the equalizer either the the preferences
of a program or by selecting it as the default (called "fallback" in
**puv

The output of the equalizer is connected to an output dev

## Virtual Audio Cables

To patch an source (an input such as your microphone) to a sink (an
output such as your speakers), use the **loopback** module:

    $ pactl load-module module-loopback sink_name=test_loopback

(To understand why this is called loopback, think thing of the jacks on the back
of your computer. The sound does in through the microphone jack, loops back and comes
out the speaker jack.)

To patch a sink (to which you can direct an application's sound output) to a source
(from which another application can receive sound) use a null sink.

    $ pactl load-module module-null-sink sink_name=test_null_sink

This is useful for feeding the sound output of OBS Studio into the sound input of
a video conferencing application such as Zoom or Skype. OBS Studio writes to the
null sink and Zoom or Skype reads the corresponding monitor source.

## References

* [PulseAudio under the hood](https://gavv.github.io/articles/pulseaudio-under-the-hood/)
* [PulseAudio Loopback](https://endless.ersoft.org/pulseaudio-loopback/)


