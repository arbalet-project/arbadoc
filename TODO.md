# TODO list
## Bugs and Issues
* [Hardware]  Even when not driven, the blue color is never really stable and flashes somehow
* [Software][Arbasim] Some pygame/pulseaudio thread burns the CPU ([Mint bug report](https://bugs.launchpad.net/linuxmint/+bug/1451614))
* [Software] Arbapp: using only the embedded model can lead to some unexpected behaviours when it is currently filled but not yet ready it can be pushed to the table anyway: solution = lock?
* [Arbapixel] Save CPU and memory time for operators __mul__ and other
* [All apps, especially CDemo] The use of time.sleep() in control loops is **very** sensitive to CPU speed, better control loop? [Example](https://github.com/ros/ros_comm/blob/indigo-devel/clients/rospy/src/rospy/timer.py)
* [SpectrumAnalyser] Does not start on RPi

## Missing features
### High priority and/or short-term
* [Software] Test Windows support, tag config/devices should depend on the OS
* [LightsHero] Extend compatibility of SongReader to other songs, especially by being compatible with variable tempos (SetTempoEvent events)
* [LightsHero] Count score! +1 for each right played frame, -1 for each wrong played frame, compare with the frames that should have been played and give the score as a ratio%
* [Tetris] Fix joystick by looking for a hat-compatible joystick (Some computers have a fake embeded joystick, that should be ignored)
* [Tetris] Add keyboard support

### Low priority and/or long-term
* [Software] Address non-RGB strips
* [Software] Django-based Web UI for Arbalet for Home
* [Hardware] Add a small TFT screen to display scores and user instructions
* [Spectrum Analyser] compute the max level (= the divider) to scale automatically to weak or loud musics
* [Spectrum Analyser] Add a generic multiformat support (on-the-fly sampling in wave?) and/or plugins for vlc to send music to the table and/or direct analysis from a micro 

## Documentation and community
* IRC channel #arbalet
* Write the "Build your own" wiki page and drawings, some clues for drawings: [Inkscape tracing module 3D->SVG](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/Trace.html)
* Wiki: Comment on OS, realtime OS, microcontroller, fixed rate problem, and same-speed apps on all platforms

# Useful related links
[Open source bench homemade with palettes](http://xuv.be/uH-bench-open-source-public-bench.html)

