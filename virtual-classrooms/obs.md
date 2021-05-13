# Open Broadcasting Studio

OBS is a program for mixing audio and video for a program which is either broadcast
live over a streaming service or recorded in real time.

## OBS.Ninja

OBJ.Ninja is a website which helps you use WebRTC as a way to bring remote video sources
into OBS Studio. One brings the video and audio into OBS Studio by creating a browser source
and setting it to display a URL from the OBJ.Ninja site.

During a test we performed on a computer with a quad-core 1.4 GHz AMD processor we were unable
to get acceptable performance when running OBS and OBS.Ninja in Chromium on the same machine.
Selecting the H.264 codec improved things somewhat, not enough. The video stream from guests
would fall behind further and further getting to several minutes.

## References

* [OBS Studio Python Scripting Cheatsheet](https://awesomeopensource.com/project/upgradeQ/OBS-Studio-Python-Scripting-Cheatsheet-obspython-Examples-of-API?categoryPage=14)
* [How I stream video with OBS and WebSockets](https://opensource.com/article/20/6/obs-websockets-streaming)
* [Fake Chroma Key for Webinars](https://gitlab.com/gersonjferreira/fake-chroma-key)
* [How to do HLS streaming in OBS (Open Broadcast Studio)](https://obsproject.com/forum/resources/how-to-do-hls-streaming-in-obs-open-broadcast-studio.945/)
* [Virtual Audio Cable for Zoom](https://obsproject.com/forum/threads/virtual-audio-cable-for-zoom.125072/)


