# TODO list
## Bugs and Issues
* [Hardware]  Even when not driven, the blue color is never really stable and flashes somehow
* [Software][Arbasim] Some pygame/pulseaudio thread burns the CPU ([Mint bug report](https://bugs.launchpad.net/linuxmint/+bug/1451614))
* [arbasdk setup.py] cv2 dependency: installable via pip?

## Missing features
### High priority and/or short-term
* [Software] Centralize X11 events in a shared class of the SDK for non-graphical applications, cf commit 8f9944786315db74180b7f81ca24f062ac18ad4d
* [Arbapp] Clean pygame.event collection and sharing in Arbapp 
* [LightsHero] Extend compatibility of SongReader to other songs, especially by being compatible with variable tempos (SetTempoEvent events)
* [Tetris] Fix joystick by looking for a hat-compatible joystick (Some computers have a fake embeded joystick, that should be ignored)
* [Arbasim/Arbalink/Arbapp] remove all threading systems from the SDK by requiring a loop in Arbapp (like Arduino setup() loop()). Issue: what about the interactive mode?

### Low priority and/or long-term
* [Software] Address non-RGB strips
* [Software] Django-based Web UI for Arbalet for Home
* [Hardware] Add a small TFT screen to display scores and user instructions
* [Spectrum Analyser] compute the max level (= the divider) to scale automatically to weak or loud musics
* [Spectrum Analyser] Add a generic multiformat support (on-the-fly sampling in wave?) and/or plugins for vlc to send music to the table and/or direct analysis from a micro 

## Documentation and community
* IRC channel #arbalet
* Write the "Build your own" wiki page and drawings, some clues for drawings: [Inkscape tracing module 3D->SVG](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/Trace.html)

# Useful related links
[Open source bench homemade with palettes](http://xuv.be/uH-bench-open-source-public-bench.html)

# Done
* [Arbapixel] Save CPU and memory time for operators __mul__ and other [ae02df5fb5a5d8a7d1c0065ce583cf7abe91a108 Could probably do even better]
* [Software] Arbapp: using only the embedded model can lead to some unexpected behaviours when it is currently filled but not yet ready it can be pushed to the table anyway: solution = lock? [b04029fdc14fa486280fe43b79950cdfe267337b]
* [All apps, especially CDemo] The use of time.sleep() in control loops is **very** sensitive to CPU speed, better control loop? [Example](https://github.com/ros/ros_comm/blob/indigo-devel/clients/rospy/src/rospy/timer.py) [1b24df1aaeb669296befadd9681b788f17e4edb9]
* [SpectrumAnalyser] Does not start on RPi due to pygame.init() that never returns in this app only [was not pygame.init() but pyaudio.PyAudio(); pip --update pyaudio did the job]
* Wiki: Comment on OS, realtime OS, microcontroller, fixed rate problem, and same-speed apps on all platforms
* [LightsHero] Count score! +1 for each right played frame, -1 for each wrong played frame, compare with the frames that should have been played and give the score as a ratio% [fbfba91da57462370f8fdeecc517620c6c002f5a]
* [LigthsHero] In class UserHits pygame.events should work even with no window (example: RPi in headless mode; pygame events?) [8f9944786315db74180b7f81ca24f062ac18ad4d]
* [Software] Test Windows support, tag config/devices should depend on the OS [85e9c8282ea13dc3d0d87f3bbe0ddd7ecf689b35 ; Windows support still to be thought about]
* [Tetris] Add keyboard support + use events instead of active polling of joystick, issue: events don't suffice when the key stay pressed [4f517d19cefb3b83535cb3b17f5a1c7c5ee8108f]
