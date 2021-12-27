# standard-led
A standardized file format for led matrix addressing and animation

## Problem
I have yet to find a standard file format for storing information about led matrix animations, nor an easy way to edit them. `.gled` files exist for glediator, but that project appears to be unmaintained. Other programs exist for windows, I'm on Mac, so that doesn't help me much. 

## Proposal
A cross-file-type format for led matrix addressing and animation frame definition, that can be imported into any language and used in diy projects. This format should be transferrable to different data types (json, yml, etc.) according to your program needs, but should maintain a consistent schema for easy translation to other formats.

### Option 1
The top of the file contains information about the entire project file, whether it loops, the full dimensions of the matrix, the delay between frames, whether the frames overlay or replace entirely.

Below that should contain frame-by-frame definitions of the led location and the hsl value.

#### `.sled`, `.sledy`, `.sledj`, `.sledx`
The file extension for this formation should contain `.sled` (for `s`tandard `led`) to be a part of this standard, with an optional last initial for the type of format being used (`y` for `yml` files, `j` for `json`, `x` for `xml`, etc)
