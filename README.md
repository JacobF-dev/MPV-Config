# Personal MPV Config
My personal MPV config geared towards moderately powered GPUs (>≈ GTX 1070).

A second config file (lightened, make sure to rename it to just mpv.conf) geared towards laptops/older desktops. (Made for a ~2015 i5 iGPU or greater for 1080p)
IF your computer struggles with this, using just profile=gpu-hq or even nothing would be the best course of action.

Since the script does not use a hardware decoder, this won't work on systems with lower power CPUs.
If any issues occur during playback, remove the hwdec=no line and uncomment the one below it. (this will enable hardware decoding)

A word on interpolation:
In both my configs, oversampling (i.e. "Smoothmotion") is used (among other algorithms), in which frames that would normally judder are blended with the next.
This does NOT make the video true 60(or whatever your monitor is)fps.
For instance, when watching a 24Hz video on a 60Hz monitor without Smoothmotion, so every 2.5th frame is skipped/dropped, creating that judder in panning shots.
With Smoothmotion enabled (as in the file), each video frame is displayed for 2.5 refreshes, blending that last half with the next half of 2.5 refreshes (next video frame).
Confusing stuff, I know. This is very simplified, I recommend you check out MPV's wiki here: https://github.com/mpv-player/mpv/wiki/Interpolation

The usage of gpu-next:
gpu-next uses rewritten kernels to deliver greater quality at a hopefully less performance hit. However, it is still in the experimental phase and can hinder some settings. Use with caution.
