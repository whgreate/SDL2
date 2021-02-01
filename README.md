# Basic guide of compiling SDL2 from source on OSX for newbies 👾
![shooter demo](https://www.parallelrealities.co.uk/images/tutorials/shooter/shooter05.png)

+ (including SDL2, SDL2 Mixer, SDL2 Image, and SDL2 TTF) 

# Why I'm writing this
+ I'v already installed SDL2 libaray compiled from source on Mac
+ when I'm following this [shooter tutorial](https://www.parallelrealities.co.uk/tutorials/shooter/shooter1.php) and type `make`, it comes this error:`ld: library not found for -lSDL2_mixer`
+ I checked makefile.txt , `LDFLAGS += `sdl2-config --libs` -lSDL2_mixer -lSDL2_image -lSDL2_ttf -lm` , I know those libs(SDL2_mixer SDL2_image SDL2_ttf) need to be installed.
+ I'm a newbie and I'm interested in compiling from source.


# Compile SDL2 (2.0.14 if you havn't already)
+ [installation reference](https://wiki.libsdl.org/Installation#Mac_OS_X)
+ [installation reference](your_sdl2_download_postision/doc/README-macos.md)
+ download [gcc-fat.sh](https://hg.libsdl.org/SDL/raw-file/a8e6474302ea/build-scripts/gcc-fat.sh)
+ ` cd your_sdl2_download_postision/;mkdir build ; cd build ; CC=/your_gcc_fat_sh_download_postision/gcc-fat.sh ../configure ; make; make install`
+ Then check your installed sdl2 lib in your MacOS:`ls /usr/local/lib/libSDL2*`

# Compile SDL2_image-2.0.5
+ [Download](https://www.libsdl.org/projects/SDL_image/release/SDL2_image-2.0.5.zip) 
+ `cd SDL2_image-2.0.5 & mkdir build & cd build & ../configure & make & sudo make install`

# Compile SDL2_mixer-2.0.4
+ [Download](https://www.libsdl.org/projects/SDL_mixer/release/SDL2_mixer-2.0.4.zip)
+ `cd SDL2_mixer-2.0.4 & mkdir build & cd build & ../configure & make & sudo make install`

# Compile SDL2_ttf-2.0.15
+ [Download](https://www.libsdl.org/projects/SDL_ttf/release/SDL2_ttf-2.0.15.zip) 
+ `cd SDL2_ttf-2.0.15 & mkdir build & cd build & ../configure & make & sudo make install`
+ issue: `The freetype-config script installed by FreeType 2 could not be found.`. solution:`brew install freetype`


# BOOM! You can build your shoot tutorials!
+ [shooter tutorial 01](https://www.parallelrealities.co.uk/tutorials/shooter/shooter1.php) 
+ `cd shoot01 && make && ./shooter01 `

# Other REF
+ [Setting up SDL 2 on iOS with XCode 9.2](https://lazyfoo.net/tutorials/SDL/52_hello_mobile/ios_mac/index.php)
