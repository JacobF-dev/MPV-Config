# MPV-Config-Windows
My personal MPV config geared towards moderately powered GPUs (>≈ GTX 1060), while still maintaining a simple-ish configuration.

A second config file (lightened, make sure to rename it to just mpv.conf) geared towards low performance laptops/old desktops. (Made for a 2013 i5)
IF your computer struggles with this, using just profile=gpu-hq or even nothing would be the best course of action.

Since the script uses a hardware decoder, this won't work on systems with outdated/unstable/nonexistant video drivers.
If any issues occur during playback, remove the line entirely to disable it.

A word on interpolation:
In both my configs, oversampling (i.e. "Smoothmotion") is used, in which frames that would normally judder are blended with the next.
This does NOT make the video true 60(or whatever your monitor is)fps.
For instance, when watching a 24Hz video on a 60Hz monitor without Smoothmotion, so every 2.5th frame is skipped/dropped, creating that judder in panning shots.
With Smoothmotion enabled (as in the file), each video frame is displayed for 2.5 refreshes, blending that last half with the next half of 2.5 refreshes (next video frame).
Confusing stuff, I know. This is very simplified, I recommend you check out MPV's wiki here: https://github.com/mpv-player/mpv/wiki/Interpolation
