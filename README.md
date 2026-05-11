Spout
=====

Spout is a simple caveflying game. The aim is to get as high as
possible, avoiding or destroying obstacles.

Controls
--------

Left:      Rotate left  
Right:     Rotate right  
Space:     Thrust  
Esc:       Pause  
Shift-Esc: Quit

History
-------

From Nick White:

Spout was originally written for a handheld by kuni, and soon
afterwards was ported to Windows using cygwin and sdl and released
under the MIT license.

In 2004 a 'unix version' was released, which mostly just slapped
autotools into the windows version and infringed the license.

This is a new unix version, based on the original Windows code by
kuni, which aims to add useful features and simplify the code.

**From me:**

Then, I changed some types in the code to work on 64 bit systems. The original code comes from [here](https://njw.name/spout/ "Nick White's Website").

To compile this, you need SDL 1.2. On Arch, you can get the correct package by using
```bash
pacman -S sdl12-compat
```
Then, you can just run
```bash
make
```
as normal, and that should compile everything. You'll see there are some macros at the top of `spout.c`:
```c
#define FRAMERATE 50 // how fast the game runs
#define MAX_GRAIN 500 // 500 is default
#define MAX_SPEED 256 // max speed, default is 256
#define SPEED_FACTOR 128 // less is faster, keep to powers of 2, default is 128
#define GRAIN_FACTOR 1 // default is 1. scales how much grain comes out
```
Try messing with them and see how the game plays with different values.
