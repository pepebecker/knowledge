# SDL2 on OS X Mavericks

## Downloads
| Framework  | Download Link                                              |
|------------|------------------------------------------------------------|
| SDL2       | [Download](http://libsdl.org/release/)                     |
| SDL2_image | [Download](http://libsdl.org/projects/SDL_image/release/) |
| SDL2_mixer | [Download](http://libsdl.org/projects/SDL_mixer/release/) |
| SDL2_net   | [Download](http://libsdl.org/projects/SDL_net/release/)   |
| SDL2_ttf   | [Download](http://libsdl.org/projects/SDL_ttf/release/)   |


## Create the ~/Library/Frameworks Directory

```
mkdir -p ~/Library/Frameworks
```

## Install SDL2

Copy SDL2.framework into the ~/Library/Frameworks directory

```
cp -R /Volumes/SDL2/SDL2.framework ~/Library/Frameworks/
```

Codesign the SDL2.framework 

```
codesign -f -s - ~/Library/Frameworks/SDL2.framework/SDL2
```

## Install SDL2 image
```
cp -R /Volumes/SDL2_image/SDL2_image.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_image.framework/SDL2_image
```

## Install SDL2 net
```
cp -R /Volumes/SDL2_net/SDL2_net.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_net.framework/SDL2_net
```

## Install SDL2 mixer
```
cp -R /Volumes/SDL2_mixer/SDL2_mixer.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_mixer.framework/SDL2_mixer
```

## Install SDL2 ttf
```
cp -R /Volumes/SDL2_ttf/SDL2_ttf.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_ttf.framework/SDL2_ttf
```

[Go Back](README.md)