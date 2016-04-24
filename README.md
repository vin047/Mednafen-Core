# Mednafen-Core
OpenEmu Core plugin with Mednafen with hacks to the PSX core for better graphics.

#### Extra features included in this fork
* 2x upscaling (ported from https://github.com/libretro/beetle-psx-libretro)
* Black borders reduced for PAL games

#### Known bugs - pull requests welcome!
* Deinterlacing is broken, hence the boot screen is messed up. 
Not an issue for mostgames though could make cutscenes and videos look bad.

#### Notes
* Upscaling can cause graphical glitches and so will reduce the accuracy of the game.
* Upscaling is hardcoded. Would be nice to dynamically load from a config file in future.
* Upscaling is done on the host CPU and IS CPU intensive! Would be nice to offload this to the host GPU in future.
* Reduction of PAL black borders changes the aspect ratio of the game. 
For NTSC games poorly converted to PAL (i.e. most games) this should actually make the game look better 
and more true to the original release as intended by the developers - i've tried to tweak it so that the 
aspect ratio is the same as NTSC resolution. On the other hand, original or properly converted PAL games 
will have incorrect aspect ratio and may even have edges of the screen cut off. If you notice any PAL games
with this let me know and we'll see if we can tweak the numbers further.
