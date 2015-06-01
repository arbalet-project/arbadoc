# TODO list
## Bugs and Issues
* [Hardware]  Even when not driven, the blue color is never really stable and flashes somehow
* [Software][Arbasim] Some pygame/pulseaudio thread burns the CPU ([Mint bug report|https://bugs.launchpad.net/linuxmint/+bug/1451614]) 
* [Software] Arbapp: using only the embedded model can lead to some unexpected behaviours when it is currently filled but not yet ready it can be pushed to the table anyway: solution = lock?

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


## Documentation and community
* IRC channel #arbalet
* Write the "Build your own" wiki page and drawings, some clues for drawings: [Inkscape tracing module 3D->SVG|http://tavmjong.free.fr/INKSCAPE/MANUAL/html/Trace.html]

# Useful related links
[Open source bench homemade with palettes http://xuv.be/uH-bench-open-source-public-bench.html]

