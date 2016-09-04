# SDL 2 on OS X Mavericks

## Install SDL2

Open the disk image you downloaded. Copy the SDL2.framework bundle to ~/Library/Frameworks for development purposes. For me, it's easiest to use the Terminal. (You can drag and drop the framework bundle onto the Terminal window to fill in its path for the cp command.)

```
mkdir -p ~/Library/Frameworks
cp -R /Volumes/SDL2/SDL2.framework ~/Library/Frameworks/
```

Note: I ran into a problem with the compiled Mac version of SDL that crashed Xcode due to a code signature mismatch. The simple fix is to update the signature right after you install it.

```
codesign -f -s - ~/Library/Frameworks/SDL2.framework/SDL2
```

## Install SDL2 image
```
mkdir -p ~/Library/Frameworks
cp -R /Volumes/SDL2_image/SDL2_image.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_image.framework/SDL2_image
```

## Install SDL2 net
```
mkdir -p ~/Library/Frameworks
cp -R /Volumes/SDL2_net/SDL2_net.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_net.framework/SDL2_net
```

## Install SDL2 mixer
```
mkdir -p ~/Library/Frameworks
cp -R /Volumes/SDL2_mixer/SDL2_mixer.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_mixer.framework/SDL2_mixer
```


## Install SDL2 ttf
```
mkdir -p ~/Library/Frameworks
cp -R /Volumes/SDL2_ttf/SDL2_ttf.framework ~/Library/Frameworks/
codesign -f -s - ~/Library/Frameworks/SDL2_ttf.framework/SDL2_ttf
```
