# MPV-Config-Windows
My personal MPV config geared towards moderately powered GPUs (>≈ GTX 1060), while still maintaining a simple-ish configuration.

A second config file geared towards low performance laptops/old desktops. (Made for a 2013 i5)

Since the script uses Direct3D 11 as a hardware decoder, this won't work on anything older than Windows 8.
To enable accelerated output on any other OS, simply change hwdec=d3d11va to hwdec=auto-safe.
If any issues occur during playback, remove the line entirely to disable it.

A word on interpolation:
In both my configs, oversampling (i.e. "Smoothmotion") is used, in which frames that would normally judder are blended with the next.
This does NOT make the video true 60(or whatever your monitor is)fps.
For instance, when watching a 24Hz video on a 60Hz monitor without Smoothmotion, so every 2.5th frame is skipped/dropped, creating that judder in panning shots.
With Smoothmotion enabled (as in the file), each video frame is displayed for 2.5 refreshes, blending that last half with the next half of 2.5 refreshes (next video frame).
Confusing stuff, I know. This is very simplified, I recommend you check out MPV's wiki here: https://github.com/mpv-player/mpv/wiki/Interpolation
