# Pure Data patches

## Various audio and MIDI utilites for Pd environment

### About Pure Data

[Pure Data](http://msp.ucsd.edu) is a visual programming language/environment
for multimedia programming, created as a research into
further development of [MAX/MSP](https://cycling74.com/) concepts.

It became a widely accepted tool for a cross-platform
MIDI and audio programming framework, akin to CSound,
but using a visual "patch" paradigm, and, like its'
commercial brother, MAX/MSP, offers a variety of graphical
"runtime" control elements.

Being a free program, it also has a large [community contributed](https://puredata.info/) extension library, with extensions for OpenGL, video processing,
specialised GUI controls, etc., some of which have become
widely adopted as standard.

<strike>It also supports a textual interchange patch format, which
can be used to port patches to MAX/MSP, and vice versa.</strike>
The updated format for Pure Data patches is now textual and
interchangable (although Pd is still aware of the old style
extensions).

With the commerical adoption of MAX/MSP, for example, as
[Max for Live](https://www.ableton.com/en/live/max-for-live/) in
Ableton Live, its' potential has become more than evident.

On top of all this, it is cross-platform (based on Tk framework),
supporting ASIO, portaudio, Jack, ALSA, etc.

### About the patches

My patches are divided into Pure Data patches (under [pd/](./pd/)) and their
general-use patch dependencies, called "abstractions"
(under [pd/externals/](./pd/externals/)).

In order to execute patches that use other patches (abstractions),
the Pd environment needs to be told where to find them, otherwise
it expects the submodules to be in the same directory as the
top level patch. The folder hierarchy I employed highlights the
relation between main modules and submodules, which are essentially
"libraries".

Check out the [web page](https://chainjazz.github.io/puredatapatches)
for more info on particular patches.

### Real world application

Although Pure Data is a self sufficient audio/video "runtime", meaning you
create patches and then use them within Pd for creative purposes, you can
also very easily integrate Pd into other environments, due to existence of
"loopback" MIDI ports. My favorite one is [loopMIDI](http://www.tobias-erichsen.de/software/loopmidi.html) which is part of
a larger [rtpMIDI (virtual) driver](http://www.tobias-erichsen.de/software/rtpmidi.html) that implements Apple CoreMIDI RTP on 
Windows OS.

### Distribution
Since you will need the Pd environment (pretty much self-contained) to
run the patches, I've made [my own signed 32-bit build for Windows](https://drive.google.com/drive/folders/1Fn-sp9pZsP7rSD6SxID2r7sPU6FRVnxV?usp=sharing), but
I highly recommend using one of the [official builds](https://puredata.info/downloads/pure-data), since mine is under
adaptation still.

Other uses might include
* porting Pd patches to Max/MSP using minimum effort search and replace text 
editing
* using Pd's built-in networking "classes"
* importing/exporting data in "offline" files
* using additonal extensions
* etc.

